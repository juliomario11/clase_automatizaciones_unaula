# Prompts para construir FlowCentinela en Power Automate

> `PROMPT_COPILOT.md` sirve para **evaluar y diseñar** (alcance, riesgos, pruebas, guion) — ya se usó y esa fue la base de este archivo. Este archivo es para la fase de **construcción**: los prompts que se pegan directamente en "Describe para diseñar" dentro de Power Automate para que Copilot arme el flujo.

## Importante antes de empezar

Un flujo de nube en Power Automate solo admite **un disparador**. Por eso "FlowCentinela" no se construye como un único flujo con tres mecanismos, sino como **tres flujos separados**:

| Flujo | Disparador | Para qué |
|---|---|---|
| **B — Demo manual** | Manual (`Manually trigger a flow`) | El que se ejecuta en vivo en clase, con datos de entrada controlados |
| **A — Monitoreo diario** | Recurrence diario | El flujo de "producción": consulta Supabase de verdad |
| **C — Reporte semanal** | Recurrence semanal (lunes) | Opcional si falta tiempo — no es crítico para la exposición |

**Orden recomendado de construcción: B → A → C.** El Flujo B no depende de que Supabase tenga datos reales por debajo del umbral en ese momento, así que es el más rápido de dejar funcionando y el que valida la conexión de Outlook y las dos plantillas — justo lo que necesitas para la demo. Construye A después, y deja C para el final (o sáltalo) si el tiempo aprieta.

---

## Flujo B — Demo manual (construir primero)

Pega esto en "Describe para diseñar" al crear un flujo de nube **instantáneo**:

```text
Crear un flujo de nube instantáneo llamado "FlowCentinela - Demo manual".

Disparador: Manually trigger a flow, con estas entradas:
- Escenario (texto, valores esperados: STOCK o EPP)
- Bodega (texto)
- Material (texto)
- StockActual (número)
- StockMinimo (número)
- Trabajador (texto)
- Elemento (texto)
- DiasRestantes (número)

Agregar una condición: Escenario es igual a "STOCK".

Si es verdadero, enviar un correo con Office 365 Outlook - Send an email (V2) a
mario.perez6361@unaula.edu.co con:

Asunto: ⚠ Stock bajo — [Bodega] — [Material]

Cuerpo:
Se detectó un nivel de stock por debajo del mínimo definido.

Bodega: [Bodega]
Material: [Material]
Stock actual: [StockActual]
Stock mínimo: [StockMinimo]

Por favor gestionar la reposición con el proveedor correspondiente.

Si es falso, enviar un correo con Office 365 Outlook - Send an email (V2) a
mario.perez6361@unaula.edu.co con:

Asunto: ⏰ EPP por vencer — [Trabajador] — [Elemento]

Cuerpo:
Se detectó un elemento de protección personal próximo a vencer su vida útil.

Trabajador: [Trabajador]
Elemento: [Elemento]
Días restantes: [DiasRestantes]

Por favor programar la reposición antes de la fecha indicada.
```

**Después de construirlo:** ejecútalo manualmente al menos dos veces antes de la clase — una con `Escenario = STOCK` y otra con `Escenario = EPP` — para autorizar la conexión de Outlook y confirmar que ambos correos llegan a `mario.perez6361@unaula.edu.co`.

---

## Flujo A — Monitoreo diario (construir segundo)

Pega esto al crear un flujo de nube **programado**. Reemplaza `TU-PROYECTO`, la API key, y los nombres de tabla/columnas (`materiales_stock`, `epp`) por los reales de tu esquema de Supabase — los que aparecen aquí son solo un ejemplo ilustrativo:

```text
Crear un flujo de nube programado llamado "FlowCentinela - Monitoreo diario".

Disparador: Recurrence, frecuencia Daily, hora 07:00.

Acción 1: HTTP - GET a https://TU-PROYECTO.supabase.co/rest/v1/materiales_stock?select=*
Headers:
  apikey: [tu API key de solo lectura de Supabase]
  Authorization: Bearer [la misma API key]

Acción 2: Parse JSON sobre el cuerpo de la respuesta anterior. Genera el esquema pegando
una respuesta de ejemplo real de esa API (no lo escribas a mano).

Acción 3: Apply to each sobre los elementos del Parse JSON.
  Condición dentro del ciclo: StockActual es menor que StockMinimo.
  Si es verdadero, enviar un correo con Office 365 Outlook - Send an email (V2) a
  mario.perez6361@unaula.edu.co con la misma plantilla de "Stock bajo" del Flujo B,
  usando los valores del elemento actual del ciclo (Bodega, Material, StockActual,
  StockMinimo).

Acción 4: HTTP - GET a https://TU-PROYECTO.supabase.co/rest/v1/epp?select=*
Headers: iguales a la Acción 1.

Acción 5: Parse JSON sobre esa respuesta.

Acción 6: Apply to each sobre los elementos.
  Si FechaVencimiento viene vacía o nula, omitir ese registro sin generar error.
  Calcular DiasRestantes como la diferencia entre FechaVencimiento (formato YYYY-MM-DD)
  y la fecha de hoy.
  Condición: DiasRestantes es menor o igual a 30.
  Si es verdadero, enviar correo con la plantilla de "EPP por vencer" del Flujo B, a
  mario.perez6361@unaula.edu.co, usando los valores del elemento actual del ciclo.
```

---

## Flujo C — Reporte semanal (opcional, construir al final)

```text
Crear un flujo de nube programado llamado "FlowCentinela - Reporte semanal".

Disparador: Recurrence, frecuencia Weekly, los lunes, hora 08:00.

Acción 1: HTTP - GET a la API de Supabase para bodegas bloqueadas (ajustar el endpoint
y el filtro al esquema real).
Acción 2: HTTP - GET para equipos en mantenimiento prolongado.
Acción 3: HTTP - GET para EPP pendientes de reposición.
Acción 4: Create HTML table por cada uno de los tres resultados anteriores.
Acción 5: Enviar un correo con Office 365 Outlook - Send an email (V2) a
mario.perez6361@unaula.edu.co con:

Asunto: 📊 Reporte Semanal FlowCentinela

Cuerpo: las tres tablas HTML generadas, cada una con su propio subtítulo
(Bodegas bloqueadas / Equipos en mantenimiento / EPP pendiente).
```

---

## Solución rápida a errores comunes

| Error | Causa probable | Solución |
|---|---|---|
| `401 Unauthorized` en el HTTP GET | API key incorrecta o mal puesta en el header | Prueba la URL y los headers en Postman antes de pegarlos en Power Automate |
| El `Parse JSON` falla o marca error de esquema | El esquema se escribió a mano y no coincide | Genera el esquema desde una respuesta real (botón "Generar desde ejemplo") |
| Fechas de EPP no calculan bien los días restantes | Supabase entrega `DD/MM/YYYY` y Power Automate espera `YYYY-MM-DD` | Normaliza el formato de fecha desde Supabase, o conviértelo con una expresión antes de restar |
| Falta autenticación de Outlook al ejecutar en clase | La conexión nunca se autorizó | Ejecuta el flujo manualmente al menos 2 veces antes de la clase |
| El flujo diario falla con un EPP sin fecha de vencimiento | `FechaVencimiento` nula | Ya cubierto en el Flujo A: se omite el registro en vez de fallar |

## Pruebas antes de la clase

1. `StockActual = 5`, `StockMinimo = 10` → debe llegar correo de stock bajo.
2. `StockActual = 5`, `StockMinimo = 5` (igual) → **no** debe llegar correo.
3. `DiasRestantes = 15` → debe llegar correo de EPP por vencer.
4. `DiasRestantes = 90` → **no** debe llegar correo.
5. Un caso con stock bajo **y** EPP por vencer a la vez → deben llegar **dos** correos.
6. Ejecutar el Flujo B con `Escenario = STOCK` y confirmar que el correo llega a `mario.perez6361@unaula.edu.co` — esta es la prueba que vas a repetir en vivo frente al salón.
