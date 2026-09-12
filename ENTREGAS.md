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

## Súper prompt sugerido — Copilot en Power Automate

Pensado para el asistente Copilot ("Describe para diseñar") de Power Automate, aplicando el ciclo de vida del curso. Completa el bloque `[PROCESO A AUTOMATIZAR]` con tu caso real antes de usarlo.

```text
Actúa como un consultor experto en automatización de procesos con Microsoft Power Automate,
con dominio del ciclo de vida completo de una automatización (identificación → diseño →
evaluación → construcción → entrega/documentación).

CONTEXTO:
Soy estudiante de la Especialización en Analítica de Datos (UNAULA) y debo construir y
exponer (8 minutos) una automatización propia en Power Automate, siguiendo ese ciclo de
vida. No necesita ser compleja: el ejemplo de referencia del curso fue un flujo simple
que consulta el valor del dólar y lo reporta.

PROCESO A AUTOMATIZAR:
[Describe en 3-5 líneas: qué se hace hoy manualmente, quién lo hace, con qué herramientas
(Excel, correo, SharePoint, Forms, carpetas, etc.), cada cuánto se repite, y por qué crees
que es repetitivo y basado en reglas fijas.]

LO QUE NECESITO QUE HAGAS:
1. Evalúa si el proceso descrito es un buen candidato para automatizar (repetitivo, basado
   en reglas, volumen suficiente) o si primero debería optimizarse antes de automatizar.
2. Propón el diseño del flujo paso a paso: disparador, conectores, acciones, condiciones,
   y los puntos donde más probablemente falle.
3. Redacta, en un bloque de código aparte, las instrucciones en lenguaje natural listas
   para pegar en el asistente Copilot de Power Automate y generar un primer borrador del flujo.
4. Indica qué pruebas debería hacer para validar el flujo, incluyendo casos borde.
5. Redacta un guion breve (máximo 8 minutos hablados) para la exposición: el proceso, el
   beneficio cuantificado (p. ej. tiempo ahorrado) y la demo del flujo.

FORMATO DE RESPUESTA:
- Un encabezado por cada uno de los 5 puntos anteriores.
- El prompt del punto 3 en su propio bloque de código, listo para copiar y pegar.
- Respuestas concisas; no satures con teoría ya vista en el curso.
```
