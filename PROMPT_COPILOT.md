# Súper prompt — Copilot en Power Automate

Prompt pensado para el asistente Copilot ("Describe para diseñar") de Power Automate, aplicando el ciclo de vida de automatización visto en la Clase 1 (identificación → diseño → evaluación → construcción → entrega).

## Cómo usarlo

1. Elige uno de los 3 procesos candidatos (ver `ENTREGAS.md`) o describe el tuyo propio.
2. Completa el bloque `[PROCESO A AUTOMATIZAR]` de abajo con 3-5 líneas describiendo ese proceso.
3. Pega el prompt completo en Copilot (Microsoft 365 Copilot / Copilot de Power Automate) para obtener el análisis, diseño y guion de exposición.
4. El punto 3 de la respuesta te dará, en un bloque aparte, el texto exacto para pegar en el Copilot de diseño de Power Automate ("Describe para diseñar") y generar el flujo.

## El prompt

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
5. Redacta un guion breve (mínimo 8 minutos hablados) para la exposición: el proceso, el
   beneficio cuantificado (p. ej. tiempo ahorrado) y la demo del flujo.

FORMATO DE RESPUESTA:
- Un encabezado por cada uno de los 5 puntos anteriores.
- El prompt del punto 3 en su propio bloque de código, listo para copiar y pegar.
- Respuestas concisas; no satures con teoría ya vista en el curso.
```
