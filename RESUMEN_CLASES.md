# Resumen de las clases

> Última actualización: 2026-09-11. Resumen de contenidos a partir de las transcripciones completas en cada `Clase N/ClaseN.md`. Para las conclusiones breves ver `README.md`; para tareas y entregas ver `ENTREGAS.md`.

## Clase 1 — Fundamentos de la automatización

**Temas cubiertos:**
1. Presentación del profesor (Jonatan Andrés Londoño Taborda, EPM) y de los estudiantes.
2. Plan del curso: 6 clases en 3 semanas — Power Automate (nube), Power Automate Desktop, AI Hub, LangChain/LangGraph, y proyecto final.
3. Qué es la automatización de procesos; diferencia entre RDA (automatización robótica de datos) y RPA (automatización robótica de procesos).
4. Beneficios de automatizar y, sobre todo, cuándo **NO** conviene automatizar: reglas que cambian mucho, criterio subjetivo involucrado, volumen bajo de casos, sistemas legados o con restricciones de seguridad.
5. Glosario técnico (orquestador, conector, OCR, agente de IA, etc.) y panorama de mercado — cuadrante Gartner con UiPath, Automation Anywhere y Microsoft.
6. Licenciamiento de Power Automate y árbol de decisión para elegir herramienta según el caso.
7. **Ciclo de vida de una automatización** (identificación → diseño → evaluación → construcción → entrega) — el eje que se usa durante todo el curso.
8. Taller práctico: diligenciar la plantilla del ciclo de vida y configuración inicial de Power Automate.

**Conclusión clave:** la regla de oro repetida es *"no automatizar ineficiencias"* — primero se optimiza el proceso manual y solo después se automatiza, y únicamente si es repetitivo, basado en reglas y de volumen suficiente.

**Tareas/avisos mencionados:** la evaluación del curso es construir una automatización completa siguiendo el ciclo de vida (individual o en grupos de hasta 4), con Power Automate, para presentar en la Clase 6. Ese mismo día se debía empezar a diligenciar la plantilla del ciclo de vida (opcional) y dejar Power Automate instalado y logueado con la cuenta institucional antes de la clase siguiente.

---

## Clase 2 — Power Automate (flujos en la nube)

**Temas cubiertos:**
1. Recorrido por Microsoft Power Platform: Power BI, Power Apps, Power Automate, Copilot Studio, Power Pages, Dataverse/AI Builder.
2. Qué es y para qué sirve Power Automate.
3. Recorrido por la interfaz: tipos de flujo, plantillas, entornos, licenciamiento, colas de trabajo/concurrencia.
4. Construcción práctica de dos automatizaciones en vivo:
   - Lista de SharePoint "Solicitud de permisos" + flujo que envía un correo al crearse un elemento nuevo.
   - Formulario de Microsoft Forms → SharePoint → aprobación (Approvals) → condición → correo y actualización de estado — con depuración en vivo de errores típicos (valores de aprobación en inglés vs. español, correo vacío, formulario limitado a una sola respuesta).

**Conclusión clave:** el contenido dinámico de un flujo solo expone datos de acciones ya ejecutadas antes; los valores internos de las opciones de aprobación siempre llegan en inglés aunque la interfaz esté en español (fuente típica de errores en las condiciones). Power Automate Desktop (RPA local) se vería en la clase siguiente.

**Tareas/avisos mencionados:**
- Ocultar el campo "Aprobación" del formulario (sin fecha puntual).
- **Trabajo final del curso:** construir una automatización propia en Power Automate. Debían inscribirse en un Excel compartido en Teams (pestaña "Equipos") para formar grupos; sin fecha de entrega fijada todavía en ese momento.
- Ejercicio no alcanzado por tiempo: guardar en OneDrive los adjuntos de un correo, validando la palabra "Visitas" (individual o en equipo).

---

## Clase 3 — Power Automate Desktop

> **Nota:** resumen basado en el PDF de apoyo (`Introducción Power Automate Desktop.pdf`, 32 diapositivas). El video de esta clase se subió el 2026-09-11 y su transcripción se está generando localmente con IA (whisper); esta sección se ampliará con el contenido real del video en cuanto esté lista.

**Temas cubiertos según el material de apoyo:**
1. Power Automate Desktop como herramienta RPA de Microsoft, con tres capacidades clave: automatización de UI de escritorio, automatización web/scraping, y manipulación de archivos.
2. El entorno de desarrollo y la creación de flujos.
3. Ejemplo guiado con Excel: crear instancia, escribir en una celda, guardar.
4. Ejemplo extenso de automatización web: abrir Chrome, buscar el valor del dólar en Google, capturarlo en una variable y mostrarlo en un mensaje.
5. Selectores y XPath.
6. Acciones de archivos.
7. Controles de flujo (If/Else, bucles).
8. Invocación de un flujo de escritorio desde un flujo de nube (función Premium).

**Sobre `OrganizadorFullspath.xlsx`:** es una hoja auxiliar que usa el profesor para limpiar y dar formato a rutas XPath copiadas del inspector del navegador, para pegarlas en los selectores de Power Automate Desktop — es parte de la demostración, no una tarea del estudiante.

**Tareas/fechas mencionadas en el PDF:** ninguna; el documento es puramente instructivo.

---

## Clase 4 — AI Hub y fundamentos de IA

**Temas cubiertos:**
1. **Power Automate:** ampliación del flujo del valor del dólar con variables de entrada/salida, registro de la máquina (Machine Runtime), y un flujo de nube programado que invoca el flujo de escritorio en modo atendido.
2. **AI Hub / AI Builder:** creación guiada de un modelo personalizado de extracción de información de facturas (definición de campos, colección de documentos, etiquetado, entrenamiento) y su consumo desde un flujo de Power Automate (acción *Process Document*).
3. **Fundamentos de IA (teoría):**
   - Historia: Turing (1950), Dartmouth (1956), Deep Blue (1997), AlexNet (2012), Transformers (2017), ChatGPT (2022+).
   - Arquitectura Transformer y el mecanismo de atención.
   - Tokenización y su costo económico (cobro por millón de tokens, entrada vs. salida, caché).
   - Embeddings y espacio vectorial (similitud/distancia entre palabras).
   - Temperatura del modelo.
   - Prompting: estructura Rol-Tarea-Contexto-Formato, system prompt vs. user prompt, zero-shot/few-shot, chain-of-thought, ReAct.
   - RAG (Retrieval-Augmented Generation).

**Propósito del ejercicio con las facturas:** datos de práctica ficticios para entrenar un modelo de IA que extrae automáticamente campos de facturas en PDF (empresa, fechas, montos, ítems), consumido después desde un flujo de Power Automate — un caso guiado antes del proyecto final.

**Aviso:** la carpeta `Facturas/` solo contiene 15 de los 20 PDFs esperados (faltan `factura_6` a `factura_10`).

**Tareas/fechas mencionadas:**
- **Exposición final del curso "dentro de 8 días"** desde esta clase: 8 minutos por persona/equipo (máx. 4 integrantes), individual o grupal. Se debe describir brevemente el proceso automatizado, el beneficio (p. ej. tiempo ahorrado) y mostrar el flujo funcionando (aunque falle, se debe mostrar el intento). No se espera un proyecto ambicioso — el ejemplo de referencia es el flujo simple del dólar.
- Inscripción en la pestaña "Registro de equipos" de Teams (nombre del proyecto + modalidad); al cierre de esta clase había 10 estudiantes sin equipo registrado.
- Algunos estudiantes expondrán el viernes en vez del sábado (última clase), por disponibilidad.
- Próxima clase (no vista aún): notebook práctico de Python con un ejemplo de sistema multiagente.

---

## Conclusión general del curso

El curso construye, clase a clase, el mismo ciclo de vida de automatización presentado en la Clase 1: primero con herramientas *low-code* en la nube (Power Automate), luego en el escritorio (Power Automate Desktop/RPA), y finalmente incorporando IA (AI Builder, LLMs y prompting) como un componente más del flujo. Todo converge en el **proyecto final**, individual o en equipo: automatizar un proceso real y sencillo, documentando su ciclo de vida completo y exponiéndolo en 8 minutos.
