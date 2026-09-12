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

## Opciones de proceso a automatizar (elegir 1)

1. **Triage automático de correos (soporte/PQR):** clasifica correos entrantes con un modelo de IA Builder (clasificación de texto), responde con la plantilla según categoría, registra el caso en Excel/SharePoint y avisa por Teams si es queja.
2. **Lector automático de facturas para control de gastos:** extiende el modelo de AI Builder ya entrenado en la Clase 4 (facturas) — al subir un PDF, extrae los campos, los escribe en Excel y alerta si el total supera un umbral.
3. **Organizador automático de carpetas (Power Automate Desktop):** un flujo de escritorio mueve archivos a subcarpetas según tipo/nombre, invocado a diario por un flujo de nube programado (como el flujo del dólar de la Clase 4).

*(Detalle completo de cada opción discutido en el chat; se deja aquí la versión resumida como registro.)*

## Súper prompt para Copilot

Se movió a su propio archivo: [`PROMPT_COPILOT.md`](./PROMPT_COPILOT.md).
