# Súper prompt — Copilot en Power Automate (proyecto: FlowCentinela)

Prompt específico para el proyecto final elegido (Opción 5 de `ENTREGAS.md`): automatización de alertas para la plataforma de inventario de FSCR Ingeniería S.A.S. A diferencia de la versión anterior de este archivo, aquí no hay placeholders que completar — pégalo tal cual en Copilot (Microsoft 365 Copilot / Copilot de Power Automate).

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
Mi empresa, FSCR Ingeniería S.A.S., desarrolla una plataforma interna (NestJS 11 + Angular 21
+ Supabase/PostgreSQL, arquitectura hexagonal por dominio) para administrar Materiales,
Equipos, EPP (elementos de protección personal) y Bodegas de las brigadas que operan la red
de un cliente de telecomunicaciones. Los dominios Materiales, Equipos y Bodegas ya están
implementados; EPP está en definición. Hoy NO existen alertas automáticas de stock bajo de
materiales por bodega, ni de vencimiento de vida útil de EPP por trabajador, ni un reporte
periódico consolidado a dirección — alguien tendría que entrar al sistema y revisarlo
manualmente para detectarlo. Quiero que Power Automate cubra ese hueco, SIN reemplazar la
plataforma ni su lógica de negocio:

1. Un flujo programado (diario) que consulte, vía la API REST de Supabase con un rol de
   SOLO LECTURA (nunca la llave de servicio, para respetar el mismo principio de "toda
   escritura pasa por el backend" que ya rige la plataforma), el libro mayor de materiales
   y la vida útil de EPP por trabajador.
2. Si un material cae bajo un umbral de stock en una bodega, o un EPP está próximo a vencer,
   debe generar una alerta (correo/Teams) al encargado de esa bodega.
3. Si hace falta registrar que la alerta ya se envió (para no duplicar avisos), debe llamar
   a un endpoint propio del backend NestJS en vez de escribir directo en una tabla.
4. Un reporte semanal consolidado a dirección: bodegas bloqueadas, equipos en mantenimiento
   prolongado, EPP pendiente de reposición.

LO QUE NECESITO QUE HAGAS:
1. Evalúa si este diseño es un buen candidato para Power Automate (¿por qué encaja mejor
   aquí que programarlo a mano dentro de NestJS?) y qué recortarías del alcance para que sea
   viable en pocos días.
2. Propón el diseño del flujo paso a paso: disparador(es), conectores (HTTP/Supabase REST,
   Outlook/Teams), condiciones, y los puntos donde más probablemente falle (autenticación
   contra Supabase, formatos de fecha de vencimiento de EPP, alertas duplicadas).
3. Redacta, en un bloque de código aparte, las instrucciones en lenguaje natural listas para
   pegar en el asistente Copilot de Power Automate ("Describe para diseñar") y generar un
   primer borrador de ESTE flujo concreto.
4. Indica qué pruebas debería hacer para validarlo, incluyendo casos borde (stock justo en
   el umbral, EPP sin fecha de vencimiento registrada, bodega sin encargado asignado).
5. Redacta un guion breve (mínimo 8 minutos hablados) para la exposición de "FlowCentinela":
   el problema (falta de alertas automáticas), el diseño, la demo con datos reales o de
   prueba, y el beneficio (tiempo de reacción ante quiebres de stock o EPP vencido).

FORMATO DE RESPUESTA:
- Un encabezado por cada uno de los 5 puntos anteriores.
- El prompt del punto 3 en su propio bloque de código, listo para copiar y pegar.
- Respuestas concisas; no satures con teoría ya vista en el curso.
```
