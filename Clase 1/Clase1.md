# Clase 1 - Transcripción

*Nota sobre esta transcripción: el archivo original es una transcripción automática (VTT) generada por Teams. El canal de audio principal, identificado en la grabación como "Esp. Analítica de Datos Segundo Semestre G2", corresponde casi siempre al profesor, pero al ser el micrófono compartido del salón, en algunos tramos también recoge intervenciones cortas de estudiantes presentes físicamente en el aula que no quedaron identificados por nombre. Los estudiantes que participaron desde una conexión individual (virtual) sí quedaron identificados y se citan con su nombre. Se limpiaron marcas de tiempo, numeración de cues y ruido de transcripción (interjecciones sueltas sin contenido, como sonidos o palabras aisladas mal reconocidas por el sistema), y se corrigieron nombres de herramientas que el reconocimiento de voz transcribió de forma incorrecta (por ejemplo "por auto" o "power automated" se normalizó a "Power Automate", "iPad" a "UiPath", "lanchain" a "LangChain", etc.), sin alterar el contenido de lo dicho.*

## Apertura y presentación del profesor

La sesión arranca con problemas de audio: el profesor saluda y explica que le avisaron apenas el día anterior que le tocaba dictar esta clase, así que "voy a asumir este reto". Pasan varios minutos ajustando el micrófono mientras estudiantes confirman si se le escucha ("Negativo, profe", dice Jesús Emilio Palacio Agudelo); una vez resuelto, Héctor Hernán Buitrago Pabón, Brandon Arboleda Jaramillo, Angie Tatiana Salazar Muñetón y Mario Daniel Enrique Pérez Jiménez confirman que ya se escucha mejor.

Resuelto el sonido, el profesor se presenta: se llama **Jonatan Andrés Londoño Taborda**, es ingeniero informático del Politécnico Jaime Isaza Cadavid, tiene una especialización en ingeniería de software (Universidad de Medellín), otra en gerencia de proyectos (UPV) y este año terminó una especialización en ciencia de datos e inteligencia artificial, también en la Universidad de Medellín.

Cuenta su trayectoria laboral: lleva 9 años en EPM (va a cumplir 10). Antes trabajó varios años como desarrollador de software en Unión Eléctrica, programando dispositivos electrónicos para comunicarse con medidores (medición inteligente de servicios públicos). Luego pasó a Intergrupo (hoy Software One), donde desarrolló en C# y en iOS para dispositivos móviles, y en ASP. En EPM inicialmente no hacía desarrollo, aunque comenta que el área está retomando esa cultura; actualmente implementa agentes de inteligencia artificial para mejorar el proceso de facturación, en el área de facturación de EPM ("el área que le cobra a todos los que pagan los servicios [públicos]"). A modo de anécdota cuenta que en ese momento están trabajando en un requerimiento de la CRA para cobrar un desincentivo por el uso de energía relacionado con el fenómeno del Niño: se calculará una meta de consumo por hogar y quien la supere en más de un 40 % pagará un valor adicional, mientras que quien ahorre recibirá una bonificación.

A continuación pide a los estudiantes que se presenten: de dónde vienen, qué han estudiado, qué experiencia tienen y qué esperan de la materia.

## Presentación de los estudiantes

Varios estudiantes que estaban físicamente en el salón se presentaron por el micrófono compartido del aula, por lo que en la grabación no siempre quedó claro el nombre de cada uno. Entre lo que se alcanza a identificar: alguien (aparentemente de nombre Carlos) comenta trabajar en el área de control u operaciones financieras de una empresa; se pregunta al grupo si conocen machine learning; y hay comentarios sobre la importancia de justificar bien el retorno de la inversión antes de construir una automatización, "porque si nadie la usa y es demasiado costosa" no tendría sentido. Dentro de este mismo tramo, alguien se identifica como **Estela Torre**, licenciada en educación (su presentación se corta antes de precisar en qué se desempeña actualmente).

Los estudiantes conectados de forma individual sí quedaron identificados por nombre:

- **Laura Marcela Gaviria Yepes**: administradora tecnológica; tiene maestría en gestión de innovación y cursa un doctorado en gestión de la tecnología y la innovación; ha trabajado con datos para investigación y vigilancia tecnológica; actualmente es instructora del SENA y trabaja de forma independiente formulando proyectos para convocatorias de beneficios tributarios. Aclara que sus conocimientos de programación son básicos y pide tener en cuenta que hay un subgrupo del curso en la misma situación.
- **Santiago Saldarriaga Restrepo**: administrador de empresas; trabaja en el Grupo Éxito administrando una sublínea, y fue administrador de inventarios del mismo grupo.
- **Evelin Hernández Avendaño**: administradora de empresas; especialista de proveedores en Amrise, un centro de servicios para una cementera de Estados Unidos.
- **Mario Daniel Enrique Pérez Jiménez**: ingeniero de instrumentación y control del Politécnico Jaime Isaza Cadavid; hoy es desarrollador de software, contratista para Tigo y Afinia. Su expectativa es profundizar en agentes autónomos con LangChain/LangGraph. Más adelante en la clase cuenta que en su trabajo interactúa con una versión antigua de un facturador de servicios (menciona el sistema como "Marflex"/OpenSmartFlex), principalmente a nivel de base de datos, no del programa de escritorio.
- **Brandon Arboleda Jaramillo**: politólogo; trabaja en una universidad digital como oficial de monitoreo y evaluación de proyectos, primero sociales y ahora educativos. Le interesa mucho el tema agéntico —menciona una actualización reciente de Grok que, según él, representó "la primera consolidación real de un agente"— y pide profundizar en el tema durante el curso.
- **Juan Felipe Muñoz Zuluaga**: ingeniero de producción; trabaja para una empresa de software en España. Su objetivo es aprender más sobre agentes y sobre las herramientas para desarrollarlos en las empresas.
- **Marinella González Mayo**: administradora de empresas; trabaja en EPM, en el área de Contact Center y Soporte.
- **Juan José Blandón Isaza**: ingeniero civil; trabaja en el área de desarrollos inmobiliarios de la constructora Coninsa (tuvo que reconectarse por problemas de audio y repitió su presentación). Su expectativa es ampliar su conocimiento en automatización y aplicarlo en su trabajo.
- **Henry Antonio Uyazán Rodríguez**: abogado de profesión; trabaja en una empresa estatal de seguridad, en un área que describe como "seguridad analítica", sobre todo en labores de operación. Cuenta que siempre ha tenido interés en el análisis de datos, pero no había tenido la oportunidad de acercarse porque lo veía como "un tema de ingenieros"; dice sentirse "de cero" en el tema, pero muy motivado por aprender.
- **Angie Tatiana Salazar Muñetón**: ingeniera informática; trabaja como analista de datos (el profesor comenta que "le gusta aprender Power Automate").
- **Jesús Emilio Palacio Agudelo**: de formación administrador comercial, con una tecnología en desarrollo de software; trabaja en Corbeta, en la unidad de negocio de electrodomésticos, como analista de inteligencia de negocios. Su expectativa es profundizar en herramientas low-code y en agentes; menciona también interés en "vibe coding" (programar apoyándose fuertemente en IA).
- **Grace Lorena Londoño Arango** y **Luisa Fernanda Murcia Vargas**: participan durante la sesión (preguntas sobre el receso y sobre el material de la clase, despedida final) sin que quedara registrada en el audio una presentación individual completa.

## Metodología del curso, herramientas a usar y evaluación

El profesor explica que el curso consta de **6 clases a lo largo de 3 semanas**:

- **Clase 1** (hoy): introducción, conceptos básicos, herramientas y proceso de automatización.
- **Clase 2** (mañana): Power Automate Cloud — desencadenadores, acciones (los "cajoncitos" que se arrastran para armar un flujo) y conectores.
- **Clase 3**: Power Automate Desktop, la herramienta que permite interactuar directamente con la máquina (mover archivos, dar clics en páginas web, etc.).
- **Clase 4**: introducción a AI Hub —los componentes de inteligencia artificial que trae Power Automate ya construidos, como OCR para extraer texto de PDFs o análisis de sentimiento— junto con conceptos básicos de inteligencia artificial: cómo funcionan los modelos de lenguaje, tokenización, embeddings y técnicas básicas de prompt engineering.
- **Clase 5**: LangChain y LangGraph, las librerías para construir agentes de inteligencia artificial con código.
- **Clase 6**: proyecto final, donde cada estudiante o grupo expone su trabajo.

Sobre el uso de modelos de lenguaje, el profesor explica que hay dos formas de acceder a ellos: a través de un **chat** (como ChatGPT), que es la interfaz que usa todo el mundo, o a través de una **API**, un mecanismo para comunicarse con los modelos vía programación (se necesita una "api key" que se configura en el código). La capa gratuita de estos servicios da acceso limitado; pagando se accede a un catálogo más amplio de modelos (pone como ejemplo Claude, con acceso a Sonnet y Opus, y en su momento de forma limitada a "Fable"). Elegir el modelo adecuado es un tema complejo porque depende de si la solución necesita velocidad o potencia: un análisis de sentimiento, por ejemplo, no requiere un modelo muy potente, y cada modelo tiene un costo distinto. Esto se profundizará más adelante en el curso (tokenización, embeddings).

Para la parte agéntica del curso (LangChain/LangGraph) no van a "tirar código" desde cero: van a seguir un notebook ya preparado (en Visual Studio Code) que se ejecuta paso a paso mientras el profesor va explicando qué hace cada parte, incluyendo al final la construcción de un sistema multiagente básico. **Esta parte no hace parte de la evaluación del curso**, es solo para entender cómo funciona un agente de inteligencia artificial "por dentro". Para poder ejecutar esos modelos de pago se sugiere que, entre quienes puedan, aporten unos 5 USD para usar modelos de OpenAI; alternativamente se mostrará un ejemplo usando modelos de Google, que tienen una cuota gratuita hasta cierto límite.

**La evaluación del curso** consiste en construir, individualmente o en grupo (sugiere grupos de hasta 3 o 4 personas, aunque también se puede trabajar solo), una automatización sencilla siguiendo el ciclo de vida que se explica en esta clase —el mismo que el profesor usa en su área de EPM—, usando Power Automate (nube, escritorio, o ambos combinados). El profesor insiste varias veces en que no hay que estresarse por la nota: "aquí vinimos fue a aprender... eso pues cuando es conmigo todo el mundo gana".

## ¿Qué es la automatización de procesos?

El profesor la define como el diseño y uso de herramientas tecnológicas para ejecutar tareas repetitivas y basadas en reglas, con mínima o ninguna intervención humana: básicamente, decirle a un robot que ejecute una serie de pasos secuenciales, uno detrás de otro, para cumplir una tarea u objetivo.

¿Para qué sirve? Para mejorar la eficiencia —todos los procesos hay que mejorarlos y reducir costos—. Una tarea manual es propensa a errores (por ejemplo, al transcribir documentos a un sistema), y automatizarla libera tiempo de las personas para actividades de mayor valor estratégico. Pone como ejemplo su propia área en EPM: tenían un grupo de personas próximas a pensionarse que antes debían trabajar fines de semana y horas extra; al introducir automatización en el proceso, ya no tienen que trabajar los fines de semana y dedican ese tiempo a su familia y a actividades que aporten más valor a la empresa.

Pregunta al grupo quién ha automatizado algo (aunque sea una macro de Excel), quién ha abierto Power Automate y quién escribe código hoy. Comenta que las macros de Excel fueron la primera herramienta que usaron para automatizar en EPM, y que todavía las usan bastante. Cuenta dos anécdotas: un robot que todos los días entrega un informe, y otro que corre todo el fin de semana para procesar el pago del auxilio de conectividad (internet y energía) de los teletrabajadores de EPM —antes era una tarea completamente manual, y ahora, cuando llegan el lunes, el pago ya está hecho para todo el mundo—.

## RDA vs. RPA (conceptos básicos)

- **RDA (Robotic Desktop Automation)**: automatización **asistida** que trabaja directamente en el escritorio del usuario. El usuario la ejecuta a demanda, su computador se bloquea mientras el robot trabaja, y los robots actúan como asistentes virtuales que permiten al usuario mantener el control durante la ejecución (por ejemplo, pedirle que organice unas carpetas y archivos).
- **RPA (Robotic Process Automation)**: automatización **no asistida**, con robots basados en reglas que se ejecutan de forma independiente, sin intervención humana; ideal para procesos escalables y de alto volumen. Normalmente corren en servidores o equipos aparte, para no ocupar el equipo de una persona, aunque herramientas como Power Automate manejan una función llamada "picture in picture" que crea una especie de máquina virtual dentro de la máquina para que la automatización corra mientras la persona sigue trabajando; aun así, sigue siendo, en esencia, un RDA.

## ¿Por qué automatizamos? Beneficios de automatizar

1. **Eficiencia operativa**: el flujo se ejecuta en minutos, sin pausas y 24/7; libera a una persona de una tarea repetitiva que "hasta aburre".
2. **Reducción de errores**: una persona que hace tareas manuales se cansa, le da sueño o tiene un mal día, lo que afecta el resultado; un proceso estandarizado y automatizado no comete esos errores por fatiga o distracción. Eso sí, hay que controlar qué pasa cuando el proceso se sale del "flujo feliz": por ejemplo, si se espera un correo con un asunto en un formato específico y este no llega así, "el robot va a estallar" si no se programó el manejo de esa excepción (por ejemplo, reenviando una alerta a otro correo).
3. **Trazabilidad y control**: los robots dejan logs de ejecución (qué se hizo, cuándo y con qué datos) que permiten auditar el proceso y saber, por ejemplo, cuánto se demoró.
4. **Escalabilidad y foco**: si aumenta el volumen de trabajo, el equipo no tiene que crecer y el robot no se cansa (aunque si se va a demorar más).

En medio de esta parte surge una pregunta por el chat sobre **n8n**: el profesor explica que es otra herramienta (no vista en el curso) para crear agentes de inteligencia artificial, que funciona de forma parecida a Power Automate —también se arrastran "cajoncitos" y se configuran modelos de lenguaje con su propia API key—. A diferencia de Power Automate, en n8n no vienen componentes de IA incluidos por defecto: hay que configurarlos. n8n tiene una versión gratuita que se puede instalar en el propio equipo, y una capa en la nube que sí tiene costo.

## ¿Qué NO automatizar?

1. **Reglas que cambian con frecuencia**: el mantenimiento cuesta más que el ahorro. El profesor explica que, siempre que se puede, prefieren conectarse a los sistemas por API en lugar de por la interfaz gráfica, porque las páginas web usan selectores (fragmentos de código HTML) para que el robot ubique cada botón o campo, y ese código puede cambiar —por ejemplo, cada vez que alguien inicia sesión en el facturador OpenSmartFlex de EPM, el código interno de cada etiqueta cambia—, lo que hace que el selector falle y el robot se pierda y falle también. Aclara que si el robot se apoya en **mnemónicos** (códigos fijos de cada funcionalidad del sistema, por ejemplo el que liquida la factura tomando el consumo y multiplicándolo por la tarifa) no hay problema, porque esos códigos no cambian; el problema está en el código HTML de la página, no en el mnemónico. Cuenta también el caso de una automatización que dejó de funcionar porque la Fiscalía le cambió todo el diseño a su página web.
2. **Decisiones con criterio subjetivo**: un robot de RPA sigue un flujo rígido y no puede replicar el juicio humano; eso sí lo puede hacer una inteligencia artificial, que "ya tiene un cerebro" —el modelo de lenguaje (LLM)—.
3. **Volumen bajo**: si una tarea se ejecuta, por ejemplo, una sola vez al año, hay que calcular cuánto cuesta hacerla manualmente frente a lo que costaría automatizarla (incluyendo, si se hace en Python, un orquestador para disparar el proceso de forma desatendida); si no compensa, no vale la pena.
4. **Sistemas legados** que van a ser reemplazados en el corto o mediano plazo, o **sistemas sin acceso autorizado o con bloqueos de seguridad**. Aquí el profesor menciona un problema recurrente con el área de ciberseguridad de su empresa: quieren ponerle múltiple factor de autenticación (MFA) a las cuentas técnicas que usan los robots, lo cual no tiene sentido porque un robot no puede recibir un código por mensaje de texto ni resolver un captcha. Los captchas existen precisamente para bloquear robots; meterle un modelo de IA para resolver un captcha de imágenes (tipo "seleccione los hidrantes") requeriría OCR y no lo ve viable, y de todas formas ese tipo de control es propio de entornos públicos —para evitar que alguien tumbe una aplicación con peticiones automatizadas—, no de entornos corporativos donde el usuario ya se autenticó.

## Glosario de términos del ecosistema de automatización

- **Attended / Unattended (atendida / desatendida)**: una automatización atendida se ejecuta a demanda; una desatendida se dispara sola —programada a una hora fija, o por un evento como la llegada de un correo o el envío de un formulario de Forms—.
- **Orquestador**: quien programa, ejecuta y monitorea los robots desatendidos, y permite saber si se ejecutaron correctamente o tuvieron algún fallo.
- **Conector**: la puerta de entrada a un sistema vía API, sin necesidad de tocar su interfaz.
- **OCR (procesamiento inteligente de documentos)**: lee PDFs y facturas y extrae información no estructurada.
- **Hiperautomatización**: la combinación de RPA con inteligencia artificial o flujos agénticos; según el profesor, es un término que ya casi no se usa.
- **Modelo de machine learning** (a modo de "abrebocas", ya que el grupo aún no ha visto esa materia): un modelo entrenado con datos. Ejemplo: si se tiene una base de datos con la estatura, el color de piel y la ubicación geográfica de varias personas, se puede entrenar un modelo con una variable objetivo —por ejemplo, la edad— para que, a partir de esas características, prediga esa variable con cierto porcentaje de acierto; usar el modelo ya entrenado para predecir sobre datos nuevos se llama **inferencia**. Aclara que este tipo de modelo es mucho más pequeño que los modelos de lenguaje grandes actuales (como los de OpenAI o ChatGPT), entrenados con enormes cantidades de información y basados en redes neuronales.
- **Agente de IA**: a diferencia de un flujo de RPA que sigue pasos fijos, un agente de IA es capaz de tomar decisiones durante la ejecución. El profesor dice que este concepto quedará más claro cuando vean agentes con Python más adelante en el curso.

## El mercado de herramientas de automatización

Para hablar de qué herramientas se mueven en el mercado, el profesor muestra el cuadrante mágico de Gartner (con fecha de mayo de 2026): una consultora que evalúa periódicamente los proveedores de un mercado y los ubica en cuatro cuadrantes (líderes, visionarios, challengers y niche players, según su capacidad de ejecución y su visión de hacia dónde va el mercado). En el cuadrante de RPA, **UiPath** aparece como líder — "hoy en día es la herramienta que lidera el tema de RPA o desarrollo de automatizaciones" —, seguida de **Automation Anywhere** y de **Microsoft** (Power Automate); más abajo aparecen SS&C Blue Prism y ServiceNow, y como visionarios o niche players, Appian, Pegasystems, EvoluteIQ, Laiye y Samsung SDS.

Cuenta que en EPM usaban UiPath, pero es una herramienta muy costosa —por tres años de licencia pagaron cerca de un millón de dólares— y en noviembre termina el contrato, por lo que están migrando todas sus automatizaciones de UiPath a Power Automate. Automation Anywhere, otra herramienta líder, según el profesor la usa Bancolombia. Sobre Microsoft/Power Automate comenta que "inició muy escueta" y ha ido ganando terreno hasta estar dentro de los líderes, por debajo de UiPath y Automation Anywhere, apalancada por la fuerte inversión de Microsoft (incluye Copilot).

**Laura Gaviria** pregunta por qué EPM decidió cambiar de herramienta: ¿es solo un tema de costos, o las otras son más vulnerables a ataques o hackeos? El profesor responde que fue netamente un tema de costos: EPM debía entregar mensualmente un informe de los ahorros generados por cada automatización, y el proveedor de UiPath seguía subiendo los precios sin que la relación costo-beneficio se sostuviera; al ser una empresa pública que contrata por contrato, decidieron no renovar y migrar a Microsoft, que en cualquier caso ya está bien posicionado como líder.

**Mario Pérez** pregunta por qué ServiceNow aparece en el cuadrante inferior (visionarios) si es una herramienta ITIL muy usada (dice que también se usa en Tigo). El profesor responde que no conoce bien esa herramienta, pero que probablemente todavía no esté consolidada específicamente en el mercado de RPA/automatización —de ahí que Gartner la ubique como visionaria: sabe hacia dónde va el mercado, pero aún no tiene ahí un producto muy sólido—.

## Cómo elegir la herramienta y licenciamiento de Power Automate

El profesor presenta un pequeño árbol de decisión para elegir la herramienta según el caso:

- Si el sistema tiene **APIs o conectores disponibles** (Salesforce, SAP, bases de datos, etc.) → **Power Automate Cloud**.
- Si no hay API y solo existe la interfaz gráfica → **Power Automate Desktop**, que sí puede interactuar con la interfaz de usuario de la aplicación.
- Si hay **documentos no estructurados** (PDFs, correos, texto libre) → la capa de inteligencia artificial / OCR de Power Automate (AI Hub) —aclara que usar esos componentes avanzados requiere una licencia premium, que la universidad sí tiene disponible—.
- Si hay **transformación de datos pesada, muchos archivos o lógica compleja** → Python o una herramienta como n8n.
- Si el proceso requiere **criterio, contexto o varios pasos encadenados** → LangChain / LangGraph.

Sobre licenciamiento de Power Automate, muestra en pantalla los distintos niveles:

- Una **capa gratuita** (con un trial de 30 días) con conectores básicos, sobre todo para interactuar con la suite de Office (crear/editar Excel, mover archivos a OneDrive, trabajar con Forms, listas de SharePoint).
- **Power Automate Premium** (unos 15 USD mensuales), que permite ejecutar flujos en la nube en modo atendido y usar componentes más avanzados; incluye una cuota de almacenamiento en Dataverse (la base de datos propia de la plataforma, que en EPM no usan y que, según comenta el profesor, Bancolombia tiene prohibido usar por temas de seguridad).
- **Power Automate Process**, para ejecutar procesos desatendidos, que requiere infraestructura (una máquina/servidor) para correr aislado.
- **Power Automate Hosted Process**, en la que Microsoft además de la licencia atendida también pone el servidor (aunque el usuario debe entrar a instalarle las aplicaciones con las que interactúa el robot).

Comenta que, gracias a un convenio con Microsoft, en EPM la licencia les sale por unos 5 USD.

## El ciclo de vida de una automatización

El profesor presenta el hilo conductor del trabajo evaluado del curso: **identificación → diseño → evaluación → construcción → entrega**. Cada etapa tiene un entregable que debe validarse antes de avanzar a la siguiente. La idea es que cada estudiante (o grupo) siga este mismo flujo para construir su automatización, diligenciando una plantilla en Word que el profesor va a compartir, empezando por elegir una tarea manual y repetitiva —del trabajo o de la vida personal— que sea candidata a automatizar.

### 1. Identificación (descubrimiento y mapeo del proceso)

1. **Filtración de tareas candidatas**: deben ser repetitivas y reproducibles (que siempre sigan el mismo flujo), basadas en reglas y sin criterio subjetivo, con alto volumen de transacciones, con entrada de datos estandarizada y en formato digital, y con un proceso estable (que las reglas no cambien con frecuencia).
2. **Diagramación del proceso actual**: mapear paso a paso lo que hace hoy el usuario, identificando sistemas, archivos, accesos y responsables, y midiendo tiempos, volumen mensual y excepciones. El profesor insiste en que medir el tiempo desde el principio facilita luego calcular los costos.
3. **Entregable**: la ficha del proceso (un documento de Excel que se va diligenciando) y el diagrama del proceso, validados con el dueño del proceso.

**Regla de oro**, repetida varias veces durante la clase: *no automatizar ineficiencias*. Primero se ordena y se optimiza el proceso, y solo después se automatiza.

Para diagramar, recomienda herramientas tipo BPMN y hace una demostración en vivo con **Visio** (disponible en la nube a través de Office 365 con la cuenta institucional): entra a Office 365, abre Visio desde el menú de aplicaciones, crea un lienzo y va armando un flujo con cuadros para actividades y rombos para decisiones (por ejemplo: "¿el correo tiene un asunto X?" → sí / no). Aclara que no es obligatorio usar Visio —cualquier herramienta de diagramación sirve—, pero a su equipo en EPM les ha funcionado bien porque el diagrama da un panorama gráfico claro del proceso candidato a automatizar.

### 2. Diseño (arquitectura de la solución)

1. **Optimización del proceso**: eliminar pasos innecesarios o duplicados, unificar controles redundantes y estandarizar los formatos de entrada y salida de los datos (por ejemplo, si la información llega unas veces por correo y otras por Teams, estandarizarla en un solo canal o en un Excel con una estructura fija), para que la automatización sea más fácil de construir y no termine automatizando una ineficiencia.
2. **Diagramación del nuevo proceso (TO-BE)**: un segundo diagrama, ya sobre el proceso propuesto, definiendo qué va a ejecutar el robot y qué queda en manos del usuario, eligiendo la herramienta (Power Automate Cloud, Desktop o ambos combinados, o Python) y el disparador (programado, por evento o manual).
3. **Definiciones técnicas**: entradas, salidas y reglas de negocio del flujo; manejo de excepciones, reintentos y notificaciones de error; usuarios, permisos y credenciales necesarias. Aquí introduce el concepto de **cuentas técnicas**: cuentas de acceso independientes y exclusivas para las automatizaciones (no ligadas a una persona), que en EPM se administran a través de un componente que el profesor menciona como "Kibols" (muy probablemente Azure Key Vault, a juzgar por el contexto), un almacén de credenciales del que el desarrollador "jala" el recurso sin llegar a ver ni conocer la contraseña. Aclara que implementar esto a fondo requeriría recursos de Azure que no van a alcanzar a ver en el curso, pero que la herramienta lo permite por temas de seguridad.
4. **Entregable**: el diagrama TO-BE y el documento de diseño, aprobados antes de construir.

### 3. Evaluación (análisis de viabilidad)

1. **Costo de la ejecución manual**: tiempo promedio por tarea × volumen mensual × costo de la hora del analista.
2. **Costo de la automatización**: tiempo de desarrollo, licenciamiento, infraestructura y mantenimiento posterior.
3. **Decisión**: se calcula el ahorro en horas y en dinero, y el retorno de inversión; si el ahorro supera el costo total, la automatización se aprueba; si no, se replantea el alcance, se optimiza el proceso o se descarta.
4. **Entregable**: un caso de negocio con el ahorro estimado y la decisión documentada.

En este punto, **Mario Daniel Pérez** pregunta por un caso real: una empresa le pagaba a unos analistas exclusivamente para ejecutar, todos los días a la misma hora, un procedimiento manual (descargar una data y enviarla por correo a un buzón). El profesor confirma que si la tarea era 100 % manual y se había contratado personal específicamente para hacerla, ahí sí aplica calcular el costo en horas-hombre (el sueldo de esas personas), porque la automatización sustituyó por completo esa intervención humana. Aclara que si no se cuenta con la información de costos, basta con dejar el análisis en el ahorro de tiempo (por ejemplo, "esta automatización nos va a ahorrar 10 horas frente a como se hacía antes").

### 4. Construcción e implementación

1. **Desarrollo**: construir el flujo en la herramienta elegida, por módulos, nombrando acciones y variables de forma clara y consistente, e incluyendo manejo de errores, reintentos y registro de ejecución (logs).
2. **Pruebas**: unitarias por módulo y una prueba integral de punta a punta, con datos reales y casos de excepción, validando el resultado con el usuario del proceso.
3. **Documentación**: un manual de usuario para la operación diaria, y un documento técnico con variables, credenciales y puntos de falla.
4. **Entregable**: la automatización probada y documentada, lista para producción.

### 5. Entrega, puesta en marcha y temas relacionados (DevOps, MLOps, LLMOps, fine-tuning)

La entrega normalmente incluye una demostración en vivo del flujo con el dueño y los usuarios del proceso, comparando el antes y el después (tiempos, errores, esfuerzo), el despliegue en el ambiente productivo, la capacitación al usuario y un acompañamiento inicial, además de un seguimiento posterior (monitoreo de ejecuciones fallidas, medición del ahorro real frente al estimado).

El profesor aprovecha para introducir el concepto de **DevOps**: una combinación de filosofía cultural y prácticas y herramientas que buscan integrar a los equipos de desarrollo y de operaciones —estos últimos son quienes despliegan entre ambientes (desarrollo, pruebas y producción) a través de pipelines automatizados—. Comenta que en la nube esto resulta más sencillo que, por ejemplo, en UiPath, donde ese despliegue exigía más manejo de código. De forma similar, menciona **MLOps** (para operacionalizar modelos de machine learning) y **LLMOps** (para modelos de lenguaje), y de ahí se desvía brevemente a explicar el **fine-tuning**: reentrenar un modelo genérico (como GPT) con información propia de una empresa para que pueda responder preguntas específicas del negocio (por ejemplo, sobre las ventas del mes pasado, algo que un modelo comercial sin ese reentrenamiento no podría responder). Muestra también **Hugging Face** como una especie de "GitHub de modelos" de IA (de texto, imagen, video, etc.), donde por ejemplo un modelo gratuito de OpenAI (una versión de 20 mil millones de parámetros, frente a otra de 120 mil millones que ya requeriría un servidor con al menos 80 GB de GPU) se puede descargar y ajustar con datos propios en un servidor de la empresa, para no depender del cobro por token de los proveedores comerciales.

## Taller práctico: diligenciando la plantilla del ciclo de vida

Ya cerca del final de la clase, el profesor comparte en el equipo de Teams del curso tanto la presentación como una **plantilla en Word** (organizada según el mismo ciclo de vida) para que los estudiantes empiecen a diligenciarla, y explica campo por campo cómo debe completarse:

- Nombre del proceso, integrantes del equipo (grupos de hasta 3 o 4 personas, o individual), área o empresa (real o inventada, si alguien prefiere no usar datos de su trabajo) y dueño del proceso.
- En **identificación**: los criterios de filtración (si la tarea es repetitiva, si se basa en reglas claras, el volumen de transacciones, si la entrada está estandarizada, si el proceso es estable) y la diagramación del proceso actual, actividad por actividad, con su responsable, sistema o archivo y tiempo, más el diagrama gráfico (hecho, por ejemplo, en Visio).
- En **diseño**: el diagnóstico y la justificación de cada paso (si se elimina, se simplifica o se estandariza), el nuevo diagrama TO-BE, la herramienta elegida y la justificación de por qué se eligió, el disparador, y las definiciones técnicas de entradas y salidas.
- En **evaluación**: tiempos, volumen y —si se cuenta con la información— costos, infraestructura y mantenimiento, hasta llegar al ahorro estimado y a la decisión (aprobar, replantear o descartar).
- En **construcción** no hay que diligenciar nada, porque ya es el flujo como tal.
- En **entrega**: una ficha con evidencia de la demostración, comparación de antes/después en tiempos y errores, y el manual de usuario.

Como ejemplo de un posible proceso a automatizar —aclara que no tiene que ser necesariamente de la empresa de cada quien, puede ser algo inventado—, propone la **solicitud y aprobación de permisos o vacaciones**: hoy en día suele hacerse por correo o de palabra; se podría estandarizar con un formulario de Microsoft Forms, registrar la solicitud en una lista de SharePoint y automatizar el flujo de aprobación del jefe, notificando por correo tanto si se aprueba como si se rechaza.

## Primeros pasos con Power Automate (configuración práctica)

Para cerrar la sesión, el profesor pide a todos loguearse con la **cuenta institucional de Office 365 de la universidad** (Universidad Autónoma Latinoamericana) y, desde el menú de aplicaciones (los "9 puntos"), entrar a Power Automate, verificando que quede seleccionado el entorno correcto ("Universidad Autónoma Latinoamericana"). Explica que la aplicación de escritorio (Power Automate Desktop) instala además una extensión en el navegador, necesaria para que el robot pueda interactuar con páginas web (abrir páginas, dar clic, etc.). Solo desde el escritorio se pueden crear flujos que interactúen con componentes de la propia máquina (mover un archivo de un disco a otro, abrir el navegador y extraer un dato); la versión en la nube no tiene esa capacidad porque no cuenta con navegador. Como ejemplo sencillo de automatización de escritorio, menciona el caso de una persona que todos los días debe entrar a internet a consultar la TRM (tasa de cambio del dólar) y registrarla en un Excel: se podría automatizar con un flujo que abra el navegador, busque "dólar hoy" en Google, capture el valor y lo guarde en el archivo.

En este tramo final surge un intercambio con **Henry Uyazán**, quien cuenta que automatizó parcialmente con Python una tarea que hace como líder de su grupo en el trabajo: descargar todos los días un informe (de asistencia o turnos) de su equipo y de otros dos grupos a su cargo. Como no tiene permisos de administrador para dejarlo completamente automatizado, hoy en día debe correr el script manualmente y, además, repetirlo más de una vez porque hay compañeros con horarios distintos (algunos entran a las 7:15, otros a las 8:30, por lo que debe volver a ejecutarlo hacia las 8:35). El profesor le sugiere revisar si existe un desencadenante que se active automáticamente cuando se registre una nueva entrada en esa herramienta de turnos —dado que, según entiende, hace parte de la suite de Microsoft y probablemente esté integrada con Teams—, en lugar de tener que ejecutar el proceso manualmente varias veces al día; queda como algo por revisar más adelante.

## Cierre de la clase

Con las máquinas de los estudiantes ya encaminadas para arrancar sin contratiempos al día siguiente, el profesor agradece la participación, confirma que subirá la presentación y la plantilla al equipo de Teams del curso, y se despide hasta la Clase 2.
