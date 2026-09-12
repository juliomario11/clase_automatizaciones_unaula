# Curso de Automatización — UNAULA

Repositorio de apuntes y entregas del curso de **Automatización** (Especialización en Analítica de Datos, UNAULA). Profesor: Jonatan Andrés Londoño Taborda (EPM). El curso recorre Power Automate (nube), Power Automate Desktop (RPA de escritorio), AI Builder/AI Hub y fundamentos de IA generativa, y cierra con un proyecto final de automatización.

> Última actualización: 2026-09-11.

## Estructura del repositorio

| Carpeta | Contenido |
|---|---|
| `Clase 1/` | Introducción a la automatización, RPA vs. RDA, ciclo de vida de una automatización, licenciamiento de Power Automate. |
| `Clase 2/` | Power Platform y Power Automate (flujos en la nube): SharePoint + correo, Forms + Approvals. |
| `Clase 3/` | Power Automate Desktop (RPA de escritorio): Excel, automatización web, selectores/XPath. |
| `Clase 4/` | AI Hub / AI Builder (extracción de facturas) y fundamentos de IA (tokens, embeddings, prompting, RAG). |
| `Clase 5_NO_VISTA/` | Clase no dictada; solo contiene un enlace de referencia externo, no es material propio del curso. |

Cada carpeta de clase contiene:
- El material de apoyo original entregado en clase (PDF, plantillas, datasets de ejemplo).
- `ClaseN.vtt` — subtítulos automáticos originales de la grabación (no se sube el video: pesa varios cientos de MB/GB y excede los límites de GitHub, ver `.gitignore`).
- `ClaseN.md` — esos subtítulos convertidos a una transcripción limpia y legible, usada como contexto de este repositorio.

> **Estado de la Clase 3:** el video se subió el 2026-09-11. No traía subtítulos incrustados, así que la transcripción se generó localmente con IA (whisper vía ffmpeg) y se está integrando en `Clase 3/Clase3.md`. Si al leer esto el archivo todavía trae solo el resumen del PDF de apoyo, la transcripción completa sigue en proceso.

## Conclusiones por clase

### Clase 1 — Fundamentos de la automatización
Presentación del curso (6 clases en 3 semanas: Power Automate Cloud, Desktop, AI Hub, LangChain/LangGraph y proyecto final). Se define qué es automatización de procesos, la diferencia entre RDA y RPA, cuándo automatizar y cuándo NO hacerlo (reglas que cambian mucho, criterio subjetivo, bajo volumen, sistemas legados/seguridad), glosario técnico, panorama de mercado (UiPath, Automation Anywhere, Microsoft) y licenciamiento de Power Automate.

**Conclusión clave:** la regla de oro del curso es *"no automatizar ineficiencias"* — primero se optimiza el proceso y solo después se automatiza, y únicamente si es repetitivo, basado en reglas y de volumen suficiente. El **ciclo de vida de una automatización** (identificación → diseño → evaluación → construcción → entrega) es el eje que se usará durante todo el curso y en el proyecto final.

### Clase 2 — Power Automate (flujos en la nube)
Recorrido por Power Platform (Power BI, Power Apps, Power Automate, Copilot Studio, Power Pages, Dataverse/AI Builder) y por la interfaz de Power Automate (tipos de flujo, plantillas, entornos, licenciamiento, colas de concurrencia). Construcción en vivo de dos flujos: (1) lista de SharePoint "Solicitud de permisos" que envía un correo al crear un elemento, y (2) formulario de Microsoft Forms → SharePoint → aprobación (Approvals) → condición → correo, depurando errores típicos.

**Conclusión clave:** el contenido dinámico solo expone datos de acciones ya ejecutadas antes en el flujo, y los valores internos de las opciones de aprobación siempre llegan en inglés aunque la interfaz esté en español (fuente común de errores de condición).

### Clase 3 — Power Automate Desktop
*(Conclusión provisional a partir del PDF de apoyo; se completará con la transcripción real del video.)* Power Automate Desktop como herramienta RPA de escritorio: automatización de UI, automatización web/scraping y manipulación de archivos. Ejemplos guiados: escribir en Excel, y un flujo que abre Chrome, busca el valor del dólar en Google y lo captura en una variable. Cubre selectores y XPath, acciones de archivos, control de flujo (If/Else, bucles) e invocación de un flujo de escritorio desde un flujo de nube (función Premium).

### Clase 4 — AI Hub y fundamentos de IA
Ampliación del flujo del dólar (variables de entrada/salida, Machine Runtime, flujo de nube programado que invoca un flujo de escritorio atendido). Construcción guiada de un modelo de IA Builder/AI Hub para extraer campos de facturas en PDF, consumido después desde Power Automate (acción *Process Document*). Teoría de fundamentos de IA: historia (Turing, Dartmouth, AlexNet, Transformers, ChatGPT), arquitectura Transformer/atención, tokenización y su costo económico, embeddings, temperatura, técnicas de prompting (estructura Rol-Tarea-Contexto-Formato, zero/few-shot, chain-of-thought, ReAct) y RAG.

**Nota:** la carpeta `Facturas/` solo contiene 15 de los 20 PDFs de ejemplo esperados (faltan `factura_6` a `factura_10`).

## Conclusión general del curso

El curso construye, clase a clase, el mismo ciclo de vida de automatización presentado en la Clase 1: primero con herramientas *low-code* en la nube (Power Automate), luego en el escritorio (Power Automate Desktop/RPA), y finalmente incorporando IA (AI Builder, LLMs y prompting) como un componente más del flujo. Todo apunta a un **proyecto final individual o en equipo**: automatizar un proceso real, sencillo, documentando su ciclo de vida completo y exponiéndolo brevemente. El detalle de fechas y entregas se lleva en [`ENTREGAS.md`](./ENTREGAS.md).

## Entregas del curso

Ver [`ENTREGAS.md`](./ENTREGAS.md) — incluye el estado de la entrega más próxima y un prompt sugerido para Copilot en Power Automate.
