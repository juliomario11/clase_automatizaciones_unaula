# Súper prompt — Copilot en Power Automate (proyecto: FlowCentinela)

Prompt específico para el proyecto final elegido (Opción 5 de `ENTREGAS.md`): FlowCentinela, una automatización de alertas para la plataforma de inventario de FSCR Ingeniería S.A.S. Pégalo tal cual en Copilot (Microsoft 365 Copilot / Copilot de Power Automate).

## El prompt

```text
Actúa como un consultor experto en automatización de procesos con Microsoft Power Automate,
con dominio del ciclo de vida completo de una automatización (identificación → diseño →
evaluación → construcción → entrega/documentación).

CONTEXTO:
Soy estudiante de la Especialización en Analítica de Datos (UNAULA) y debo construir y
exponer (mínimo 8 minutos) una automatización propia en Power Automate para el proyecto
"FlowCentinela", siguiendo el ciclo de vida de automatización visto en el curso.

PROCESO A AUTOMATIZAR:
Mi empresa, FSCR Ingeniería S.A.S., tiene una plataforma interna (NestJS + Angular + Supabase/
PostgreSQL) para administrar Materiales, Equipos, EPP y Bodegas de las brigadas que operan la
red de un cliente de telecomunicaciones. Hoy nadie recibe una alerta automática si el stock de
un material cae bajo el mínimo en una bodega, o si un elemento de protección personal (EPP) está
por vencer su vida útil — alguien tendría que entrar a revisarlo manualmente. Quiero un flujo de
Power Automate que:

1. Todos los días, consulte (solo lectura, vía API REST de Supabase) el stock de materiales por
   bodega y la vida útil de EPP por trabajador.
2. Si un material está bajo el mínimo, o un EPP está a menos de X días de vencer, genere una
   alerta y envíe un correo usando la PLANTILLA correspondiente al tipo:

   PLANTILLA "Stock bajo":
   Asunto: ⚠ Stock bajo — {Bodega} — {Material}
   Cuerpo:
   "Se detectó un nivel de stock por debajo del mínimo definido.

   Bodega: {Bodega}
   Material: {Material}
   Stock actual: {StockActual} {Unidad}
   Stock mínimo: {StockMinimo} {Unidad}

   Por favor gestionar la reposición con el proveedor correspondiente."

   PLANTILLA "EPP por vencer":
   Asunto: ⏰ EPP por vencer — {Trabajador} — {Elemento}
   Cuerpo:
   "Se detectó un elemento de protección personal próximo a vencer su vida útil.

   Trabajador: {Trabajador}
   Elemento: {Elemento}
   Días restantes: {DiasRestantes}

   Por favor programar la reposición antes de la fecha indicada."

3. Además del disparador diario (Recurrence), necesito un SEGUNDO disparador manual
   ("Manually trigger a flow") con entradas de tipo texto/número — Escenario, Bodega, Material,
   StockActual, StockMinimo, Trabajador, Elemento, DiasRestantes — para poder ejecutar el flujo
   a demanda EN CLASE y demostrar que el correo llega de verdad, sin depender de que en ese
   momento exista un caso real por debajo del umbral en la base de datos.
4. Para la demo en clase, TODOS los correos (de ambas plantillas) deben llegar a
   mario.perez6361@unaula.edu.co (en producción irían al encargado real de cada bodega, pero
   eso queda fuera del alcance de la demo).
5. Un reporte semanal (los lunes) consolidado a dirección: bodegas bloqueadas, equipos en
   mantenimiento prolongado, EPP pendiente de reposición.

LO QUE NECESITO QUE HAGAS:
1. Evalúa si este diseño es un buen candidato para Power Automate y qué recortarías del
   alcance para que sea viable en pocos días.
2. Propón el diseño del flujo paso a paso para AMBOS disparadores (el diario y el manual de
   demo): conectores (HTTP/Supabase REST, Office 365 Outlook), condiciones, y los puntos donde
   más probablemente falle (autenticación contra Supabase, formato de fechas, autorización de
   la conexión de Outlook antes de la clase).
3. Redacta, en un bloque de código aparte, las instrucciones en lenguaje natural listas para
   pegar en el asistente Copilot de Power Automate ("Describe para diseñar") y generar un
   primer borrador de ESTE flujo concreto, con sus dos disparadores y sus dos plantillas.
4. Indica qué pruebas debería hacer ANTES de la clase, incluyendo casos borde (stock justo en
   el umbral, EPP sin fecha de vencimiento registrada, ambas condiciones a la vez) y la prueba
   de que el correo efectivamente llega a mario.perez6361@unaula.edu.co.
5. Redacta un guion breve (mínimo 8 minutos hablados) para la exposición de "FlowCentinela":
   qué hace, cuánto tiempo ahorra, qué evita, qué mejora, la demo en vivo (disparo manual →
   correo real) y el cierre. Enfócate en el proyecto y su beneficio, sin entrar en detalles de
   seguridad ni de cómo estaba construida la plataforma antes.

FORMATO DE RESPUESTA:
- Un encabezado por cada uno de los 5 puntos anteriores.
- El prompt del punto 3 en su propio bloque de código, listo para copiar y pegar.
- Respuestas concisas; no satures con teoría ya vista en el curso.
```
