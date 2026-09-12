# Entregas y tareas del curso

> Última actualización: 2026-09-11. Documento vivo: se actualiza a medida que se confirman fechas y alcances exactos.

## 🔴 Entrega más próxima (mañana, 2026-09-12) — Power Automate

**Estado: enunciado exacto sin confirmar todavía.**

Se revisó el minuto 02:30-02:45 de los subtítulos de la Clase 4 (donde se creía que estaba mencionada), pero ese tramo trata sobre tokenización y embeddings, sin relación con ninguna entrega. La única mención real a "entregar algo" en la Clase 4 está en el minuto ≈02:15-02:20 y se refiere a la **exposición final del curso** ("dentro de 8 días" desde esa clase — ver sección siguiente), no a algo puntual para mañana.

La hipótesis más probable es que la entrega de mañana sea un ejercicio práctico de **Power Automate Desktop** asignado al cierre de la Clase 3 (coincide en tema con "debe ser con Power Automate"). Esa transcripción se generó con IA a partir del video subido el 2026-09-11 y se está integrando en `Clase 3/Clase3.md` — revisa ese archivo o este documento de nuevo cuando esté listo, o confírmame el enunciado directamente si ya lo tienes a mano (por ejemplo, desde Teams o el PDF de la clase) para dejarlo aquí con precisión.

## Trabajo final del curso

- **Qué:** construir una automatización propia completa, aplicando el ciclo de vida visto en la Clase 1 (identificación → diseño → evaluación → construcción → entrega), usando Power Automate.
- **Modalidad:** individual o en equipos de hasta 4 personas.
- **Alcance esperado:** no tiene que ser un proyecto grande — el ejemplo de referencia dado en clase fue el flujo simple que consulta el valor del dólar.
- **Inscripción:** pestaña "Registro de equipos" del equipo de Teams del curso (nombre del proyecto + integrantes). Al cierre de la Clase 4 había 10 estudiantes todavía sin registrar.
- **Exposición:** 8 minutos por persona/equipo — describir brevemente el proceso automatizado, el beneficio (p. ej. tiempo ahorrado) y mostrar el flujo (funcione o no en vivo). Algunos estudiantes expondrán el viernes y el resto el sábado (última clase).
- **Fecha:** mencionada en la Clase 4 como "dentro de 8 días" desde esa clase — falta confirmar la fecha calendario exacta (depende de cuándo se dictó la Clase 4).

## Otras tareas o pendientes menores mencionados en clase

- (Clase 1) Instalar y dejar Power Automate logueado con la cuenta institucional.
- (Clase 1) Diligenciar `Clase 1/Plantilla_Ciclo_Vida_Automatizacion.docx` pensando en un proceso candidato para el proyecto final.
- (Clase 2) Ocultar el campo "Aprobación" del formulario de Microsoft Forms del ejercicio (sin fecha puntual dada).
- (Clase 2) Ejercicio no alcanzado por tiempo: guardar en OneDrive los adjuntos de un correo, validando que contenga la palabra "Visitas" (individual o en equipo).

## Nombre del proyecto (formulario "Registro de equipos")

Propuesta principal: **AutomatIA** (fusiona "Automatización" + "IA", los dos pilares del curso). Alternativas: *FlowMind*, *NeuroFlow*, *FlowForge*. Pendiente de confirmar cuál se usó finalmente en el formulario.

## Opciones de proceso a automatizar (elegir 1 de 4)

Las tres usan material que ya se generó en clase, para que la exposición de 8 minutos tenga una demo real que mostrar y no solo teoría.

### Opción 1 — Triage automático de correos (soporte/PQR)

- **Manual hoy:** alguien lee cada correo entrante, decide si es queja/pregunta/sugerencia, responde con una plantilla y anota el caso en una hoja de control.
- **Automatizado:** Power Automate se dispara al llegar un correo → un modelo de AI Builder clasifica el texto (misma técnica que las facturas de Clase 4, aplicada a texto) → según la categoría, responde con la plantilla correcta → registra remitente/categoría/fecha en Excel o SharePoint → si es "queja", avisa por Teams.
- **Para los 8 min:** mandas 3-4 correos de prueba en vivo, se ve la clasificación, la respuesta automática y la fila que aparece en Excel — hay mucho que mostrar.

### Opción 2 — Lector automático de facturas para control de gastos

- **Manual hoy:** cada factura en PDF se revisa a mano para copiar proveedor, fecha y total a una hoja de Excel.
- **Automatizado:** extiende directo el modelo de AI Builder que ya entrenaron con las 15 facturas de la Clase 4 → se dispara al subir un PDF a una carpeta → acción *Process Document* extrae los datos → escribe la fila en Excel → si el total supera un umbral, alerta por correo/Teams.
- **Para los 8 min:** subes una factura en vivo, se ve la fila llenarse sola y disparar (o no) la alerta — es la demo más "vistosa" de las tres porque ya tienen el modelo entrenado.

### Opción 3 — Organizador automático de carpetas (Power Automate Desktop)

- **Manual hoy:** ordenar a mano los PDFs/Excel/videos que se van acumulando en una carpeta (como esta misma de Descargas o la del curso).
- **Automatizado:** un flujo de escritorio (Clase 3: acciones de archivos, bucles) mueve cada archivo a la subcarpeta según su tipo o el patrón del nombre, invocado a diario por un flujo de nube programado (igual que el flujo del dólar con Machine Runtime, Clase 4).
- **Para los 8 min:** corres el flujo en vivo sobre una carpeta desordenada y se ve ordenarse sola; es la opción más simple de construir si queda poco tiempo.

### Opción 4 — Gestión automática de incidentes de red (ServiceNow + regiones + monitoreo)

- **Manual hoy:** al crearse un incidente (INC) en ServiceNow por una falla de red, alguien debe revisarlo, clasificar impacto/urgencia, avisar a la región encargada, buscar manualmente si ya hubo un caso similar en ese nodo, y hacer seguimiento del avance en Salesforce Field Service hasta el cierre.
- **Automatizado (diseño propuesto):**
  1. **Disparador:** se crea un INC en ServiceNow → el flujo se dispara (o, en su defecto, detecta una fila nueva en Supabase/CSV que simula la cola de incidentes) y envía un correo de notificación inicial.
  2. **Clasificación:** con los campos de impacto y urgencia del INC calcula la prioridad (matriz Impacto × Urgencia) y el número de clientes afectados.
  3. **Alerta y enrutamiento regional:** genera una alerta y notifica al encargado de la región correspondiente entre las 5 regiones (ANDINA, SUR, BOGOTÁ, ORIENTE, COSTA), según la zona/nodo del incidente.
  4. **Histórico de soluciones:** consulta en Supabase (o el CSV) si existen soluciones previas para ese mismo tipo de problema o ese mismo nodo, diferenciando tecnología HFC (nodo) o GPON (ARPON), y las adjunta como referencia.
  5. **Monitoreo simulado:** simula una consulta a CACTI (si es HFC) o a ZABBIX (si es GPON) para anexar el estado de red del nodo/ARPON afectado.
  6. **Seguimiento periódico:** cada cierto intervalo consulta el avance del caso en Salesforce Field Service y reenvía el estado a los interesados; si el caso ya aparece resuelto en Salesforce, marca el incidente como "OK" y cierra el seguimiento.
- **Para los 8 min:** es la opción más completa de las cuatro — se puede mostrar el ciclo entero con un INC de prueba (fila en Supabase/CSV): clasificación automática de prioridad, alerta a la región, consulta del histórico por nodo, respuesta simulada de Cacti/Zabbix, y cierre automático al "resolverse" en Salesforce.
- **Nota de alcance:** integra 5-6 sistemas (ServiceNow, Supabase/CSV, correo, Cacti/Zabbix, Salesforce), bastante más que las otras 3 opciones. Para que sea viable en el tiempo disponible, conviene simular con datos de prueba las integraciones que no se puedan conectar de verdad (el profesor solo pidió mostrar el flujo funcionando con un caso de prueba, no una integración productiva) y aclararlo así en la exposición.

### 👉 Elegida

*(Marca aquí cuál escogiste: Opción 1 / 2 / 3, y cualquier ajuste que le hagas al alcance.)*

## Súper prompt para Copilot

Se movió a su propio archivo: [`PROMPT_COPILOT.md`](./PROMPT_COPILOT.md).
