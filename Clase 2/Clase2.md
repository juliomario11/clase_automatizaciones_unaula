# Clase 2 - Transcripción

*Nota: el archivo de subtítulos original identifica al profesor con la etiqueta de cuenta "Esp. Analítica de Datos Segundo Semestre G2" (nombre del equipo de Teams, no su nombre real). En este documento, todo el texto sin atribución explícita corresponde al profesor. Las intervenciones de estudiantes se marcan con su nombre en negrita.*

## Introducción a Microsoft Power Platform

Listo, entonces, como habíamos dicho, Power Platform es un grupo de herramientas que proporciona Microsoft. Tenemos Power BI para visualización de datos, Power Apps para construcción de aplicaciones (low code), Power Automate para automatizar procesos (se comportaría como el backend de una aplicación construida ahí), y Power Virtual Agents, que es lo que antes se conocía como Microsoft Copilot Studio: sirve para crear agentes de inteligencia artificial, también low code, sin que el usuario tenga que preocuparse por construir un RAG desde cero.

Sobre el concepto de RAG: básicamente es coger un documento —por ejemplo un PDF— y transformarlo a vectores; por debajo eso es matemática pura, puras operaciones matriciales y vectoriales (álgebra lineal), y también estadística y probabilidad. El RAG consiste en vectorizar el documento; el modelo ejecuta una consulta sobre esa base de datos vectorial, y esa consulta se le entrega de nuevo al LLM junto con el contexto que encontró en la base de datos, para que responda basado en los datos de ese documento. Este tema se profundiza más adelante en la clase de inteligencia artificial, porque explicado así, tan rápido, no se entiende muy bien.

Power Pages es para crear ya aplicaciones —es muy parecido a Power Apps, pero orientado a crear páginas web—.

Por encima de todo esto está la capa de conectores, y la capa de AI Builder o AI Hub, que es la capa de inteligencia artificial que maneja Power Platform, y Dataverse, que son las bases de datos propias que maneja toda esta infraestructura. De todas formas, también es posible conectarse a bases de datos externas (SQL, MySQL o cualquier otra), porque estas herramientas son muy fáciles de conectar.

## ¿Qué es y para qué sirve Power Automate?

Pasemos entonces a la pregunta: ¿qué podemos hacer en Power Automate? Power Automate permite automatizar flujos de trabajo entre las aplicaciones y servicios favoritos, sincronizar archivos, recibir notificaciones, recopilar datos y mucho más.

Por ejemplo, se pueden automatizar tareas como responder al instante a una notificación o a correos electrónicos de prioridad alta. Power Automate es capaz de conectarse al buzón de un correo y, apenas llega un mensaje, ejecutar una acción, como copiar los archivos adjuntos del correo a una cuenta de OneDrive. Supongamos que a un buzón de correo que gestiona una persona le llegan adjuntos que hay que almacenar en OneDrive; ese proceso manual es un poco tedioso. Con Power Automate se puede capturar ese correo inmediatamente, descargar los adjuntos y dejarlos en un repositorio (en este caso, OneDrive).

Otro ejemplo es automatizar flujos de trabajo de aprobación. Hay un mecanismo muy útil en Power Automate llamado "Aprobaciones", que se ve reflejado en Teams como una pestaña con ese nombre. Como su nombre lo indica, sirve para cuando se requiere la aprobación de un jefe sobre algo, por ejemplo una solicitud de permiso: el empleado la registra por un formulario, y la automatización se queda esperando hasta que le llega la notificación al jefe (vea, este empleado solicitó un permiso, ¿aprueba o no aprueba?), ya sea por Teams o por correo; mientras tanto, la automatización se queda en *standby* hasta que reciba la aprobación o el rechazo. Esto se ve en detalle más adelante en la clase.

Otro uso común es recibir notificaciones: por ejemplo, recibir al instante un mensaje de correo o una notificación push en el teléfono cada vez que se agregue un cliente potencial (lead) en un CRM, por ejemplo Dynamics 365 (de Microsoft) o Salesforce.

## Ingreso a la herramienta

La idea es ingresar a un navegador, entrar a Office 365, loguearse y, una vez logueados, llegar a la plataforma. Se recomienda hacerlo con la cuenta de la universidad, ya que tiene toda la suite lista; en caso de que alguien haya traído el equipo de su empresa y esta tenga la suite de Microsoft, Power Automate también se podría usar desde ahí, pero como la universidad ya tiene todas las herramientas listas, es preferible ingresar desde la cuenta institucional.

Una vez logueados, en los nueve puntitos de la esquina superior izquierda se encuentra toda la suite de aplicaciones de la licencia de Office 365. Ahí se busca "Automate" y se abre la aplicación; eso abre una nueva pestaña y aterriza en el entorno de la herramienta.

La aplicación de escritorio es para otro tipo de automatizaciones: primero se trabaja con lo que se puede hacer en la versión nube, y la próxima semana se verá lo que se puede hacer con la versión de escritorio, que fue la que se instaló la noche anterior. Básicamente esta última permite interactuar con el equipo local —escribir archivos en el disco, abrir un navegador Chrome e interactuar con una página—, cosas que no se pueden hacer desde la versión nube.

Mientras se iba abriendo la herramienta, se comentó que también se le puede pedir a Copilot que cree una automatización usando lenguaje natural, pero esa opción todavía "le falta mucho"; el profesor prefiere hacer los flujos desde cero, o cuando la automatización es muy compleja, dejar que Copilot deje una base y trabajar sobre esa base.

## Recorrido por la interfaz de Power Automate

La interfaz gráfica de la aplicación de Power Automate (versión nube) es relativamente sencilla. En el Home se puede escribir en lenguaje natural qué automatización se quiere construir y la herramienta la crea, aunque como ya se dijo, esa función de Copilot todavía no convence del todo.

En el botón **Crear** se muestran todas las opciones de creación de automatizaciones:

- **Flujo de nube automatizado**: se disparan a través de un evento, por ejemplo cuando llega un correo a un buzón, cuando se diligencia un formulario, cuando se ingresa un elemento a una lista de SharePoint, o cuando se crea un archivo en OneDrive.
- **Flujos instantáneos**: se ejecutan a demanda; el usuario simplemente le da "play" y el flujo corre cuando él lo necesite.
- **Flujos programados**: se ejecutan según una programación, por ejemplo, "necesito que este flujo corra todos los días a las 3:00 de la mañana".
- **Diseñar con IA**: se describe en lenguaje natural la automatización deseada y la herramienta intenta crear el flujo; todavía está creciendo, pero le están invirtiendo mucho, y según el "cuadrante mágico" está entre las herramientas líderes del mercado, justo detrás de UiPath y Automation Anywhere.
- **Flujos de escritorio**: para crear automatizaciones RPA que abren la aplicación de escritorio (si está instalada); para trabajar con esta versión se necesita licenciamiento premium, pero la universidad tiene convenio con Microsoft que permite usarla igual (ya se instaló el día anterior).
- **Process mining**: permite evaluar procesos, algo similar a evaluar si una automatización es viable o no; el profesor comenta que no lo ha explorado mucho, pues se mueve más en las opciones de flujos de nube, flujos instantáneos y flujos de escritorio.
- **Plantillas (templates)**: plantillas preconstruidas por Microsoft para armar automatizaciones más rápido, agrupadas por categorías (trabajo remoto, aprobaciones, correo, calendario, etc.). Por ejemplo, existe una plantilla lista para almacenar los asuntos de un correo en OneDrive, o para copiar los adjuntos de un correo de Gmail a Google Drive (se puede conectar con buzones de otras empresas/proveedores). El profesor comenta que a él personalmente no le gusta partir de plantillas, prefiere construir desde cero, aunque reconoce que son formas válidas de trabajar y que hay infinidad de plantillas disponibles.
- **Learn**: es la plataforma de aprendizaje de la herramienta, con cursos gratuitos y posibilidad de certificarse.
- **Mis flujos**: ahí aparecen los flujos que ya se han construido —tanto los de nube como los de escritorio (listados)—, aunque estos últimos se trabajan realmente desde la aplicación de escritorio.
- **Pruebas unitarias**: para crear pruebas sobre los flujos; el profesor comenta que todavía no lo ha explorado.
- **Flujos compartidos**: se puede trabajar colaborativamente sobre un mismo flujo, compartiéndolo con otra persona para contribuir juntos.
- **Aprobaciones** y **Soluciones**: las soluciones permiten combinar aplicaciones de Power Platform —agentes de Copilot, Power Apps, flujos de escritorio— y empaquetar todo eso en una solución.
- **AI Hub**: son los componentes de inteligencia artificial que maneja Power Automate/Power Platform. Aquí hay muchas capacidades: se pueden ejecutar prompts, y existen modelos preconstruidos, por ejemplo para automatización de documentos (extraer información de un PDF, es decir, de datos no estructurados).

En este punto se hizo una pausa para preguntar: ¿saben qué es la data no estructurada y cuál es la diferencia con la estructurada? Un estudiante respondió que la data estructurada, por ejemplo, es la de una base de datos, que ya tiene una estructura definida; un PDF o un documento de Word es data no estructurada porque es texto sin una estructura definida; un documento XML es data estructurada, y un documento en formato JSON es data no estructurada. El profesor comentó que hay una clase específica para profundizar un poco más en estos modelos.

Siguiendo el recorrido:

- **Tablas**: para crear tablas de Dataverse.
- **Conexiones y colas de trabajo (queues)**: el tema de las colas de trabajo se usa mucho en las automatizaciones de la empresa donde trabaja el profesor. La idea es que se pueden tener varios robots ejecutando una misma automatización; el trabajo queda listado en una cola, con una estructura que uno mismo define, y se pueden poner a correr varios robots para que "desencolen" esa información en paralelo. Si un solo robot se demora, digamos, un día completo ejecutando la automatización y vaciando todo el proceso, poniendo dos o tres robots esa tarea se demoraría la mitad o una cuarta parte del tiempo. Para eso sirven las colas de trabajo: para que varios robots ejecuten la misma tarea, y eso maneja **concurrencia**.

  Sobre la concurrencia: si un robot va a tomar un elemento de la cola y, al mismo tiempo, otro robot también intenta tomar un elemento, internamente el sistema es capaz de bloquear para que los robots no tomen el mismo elemento, sino que siempre se asegure que tomen elementos diferentes cuando dos robots van a procesar un registro al mismo tiempo. Por ejemplo, en una cola puede haber una lista de correos, y dos robots van cogiendo cada uno de esos correos y procesándolos en paralelo; esto funciona con robots desatendidos, los que operan solos.

- **Máquinas**: es cuando ya se tienen máquinas que no son el propio equipo, sino servidores para que las automatizaciones corran allá, solas, en un servidor.
- **Entornos**: en la parte superior están los entornos, que son como espacios de trabajo donde se pueden crear automatizaciones. Se puede tener un entorno de desarrollo, uno de pruebas y uno productivo; el entorno por defecto (en este caso, "Universidad Autónoma") se crea automáticamente cuando se empieza a trabajar con la herramienta. El profesor comentó que él podría crear un entorno nuevo, pero eso implicaría dar permisos a todos los estudiantes para ingresar, lo cual consumiría tiempo de clase; por eso cada quien trabaja en el entorno que ya tiene por defecto.
- **Licenciamiento**: en la parte superior, en el ícono de configuración (el "piñoncito"), se puede ver el tipo de licenciamiento actual dando clic en "View My License". Ahí se ve, por ejemplo, "Power Automate Free" para la versión de Office, y que no se cuenta con la versión Premium. La versión Premium habilita conectores premium, conectores personalizados, conectores on-premise, y robots RPA atendidos y desatendidos (el desatendido requiere, además, un licenciamiento de "process"). El día anterior ya se habían revisado las licencias disponibles para el curso.

En resumen, ese es el vistazo general de la herramienta.

## Creación de la lista de SharePoint "Solicitud de Permisos"

Con la introducción hecha, se procedió a construir la primera automatización: un flujo que se dispara cuando se agrega un elemento a una lista, y que envía un correo. Para eso primero había que construir la lista de SharePoint.

Se navegó a la aplicación de listas de SharePoint (Microsoft Lists) desde los nueve puntos —una herramienta que se comparó con un Excel, donde se pueden almacenar registros, crear columnas y definir opciones—. Se creó una nueva lista en blanco, llamada **"Solicitud de permisos"**.

Por defecto, la lista trae creada una columna llamada "Título". Esa columna se renombró a **"Nombres"** (desde "Configuración de columnas" → "Cambiar nombre"), para digitar allí nombres y apellidos de quien solicita el permiso.

Luego se agregó una nueva columna de tipo **Fecha**, llamada **"Fecha del permiso"**, con la descripción "Este campo corresponde a la fecha de solicitud de permiso"; no se incluyó la hora y se dejó el formato de fecha por defecto.

A continuación se agregó otra columna de tipo **texto**, llamada **"Justificación"**, con la descripción "Esta es la justificación del permiso", configurada como "varias líneas de texto" (multilínea), para permitir digitar más contenido que en un campo de una sola línea.

Se explicó de paso que existen muchos tipos de columna disponibles al crear una nueva: texto libre, elección (como un combo con varias opciones predefinidas), fecha, varias líneas de texto, tipo usuario (que se conecta con el directorio activo), número, sí/no, hipervínculos, moneda, entre otros.

También se mencionó el campo **"Datos adjuntos"**, que SharePoint crea por defecto sin que el usuario lo haya definido explícitamente, y que se puede ocultar si no se necesita. El profesor comentó un caso real: en su empresa, para solicitudes de permiso, a veces se exige subir un soporte en los datos adjuntos (por ejemplo, el soporte de una cita médica).

Se creó una tercera columna adicional, de tipo **Elección**, llamada **"Aprobación"**, con tres opciones: **Pendiente** (cuando el usuario apenas ingresó la solicitud y el jefe todavía no la ha aprobado), **Aprobado** y **Rechazado**.

Al ingresar un elemento de prueba a la lista (por ejemplo, "Jonathan", con una fecha de permiso "para mañana, domingo" y justificación "necesito hacer una diligencia personal"), se explicó cómo funciona la vista de detalle de un elemento, y cómo se pueden mostrar u ocultar columnas —incluyendo metadatos por defecto como el ID único autonumérico del elemento, quién lo creó, cuándo fue creado, cuándo fue la última modificación, etc.— usando la opción "Agregar columna" → "Mostrar u ocultar columnas".

Se comentó que, por detrás, un equipo de Teams también es, técnicamente, una lista de SharePoint. Además, es posible anclar una lista existente como pestaña dentro de un canal de Teams para ingresar elementos directamente desde ahí (se mostró brevemente el proceso, aunque no se completó en ese momento porque se iba a alimentar la lista de forma automática con el flujo).

Como ejemplo adicional de uso, el profesor mencionó que en su trabajo también tienen una lista de SharePoint para gestionar las asignaciones del equipo de trabajo (por ejemplo, "Jonathan tiene 5 tareas, Felipe tiene 10 tareas"), y que ese tipo de información se puede incluso visualizar en un tablero de Power BI; considera esa alternativa más robusta que manejarlo en un Excel, entre otras cosas porque se puede empaquetar y construir un frontend en Power Apps para que el ingreso de información sea más amigable.

## Primera automatización: flujo manual con envío de correo

Se procedió a crear el primer flujo, llamado **"por_automatización_1"**. Se seleccionó **"Flujo de nube automatizado"**, ya que se busca que se dispare cuando se cree un elemento en la lista (aunque, por tiempo, se simuló con un disparador manual para la demostración).

Al crear el flujo aparecieron los distintos tipos de disparadores disponibles: cuando se envía una nueva respuesta de Microsoft Forms, cuando se crea un elemento en una lista de SharePoint (el que se necesitaba), entre otros.

En ese punto se explicó brevemente el concepto de **gateway** (puerta de enlace de datos local): permite conectar la nube con recursos on-premises. Por ejemplo, si la empresa tiene una base de datos Oracle dentro de su propia red, una aplicación en la nube no tiene forma de ver esa red corporativa a menos que se conecte a través de una VPN; el gateway es justamente para eso: se instala en un equipo ese complemento, y permite conectar la nube con lo que está en la red corporativa. Alternativamente, se puede usar Power Automate Desktop para este propósito, ya que el flujo de escritorio corre directamente en el equipo, que ya está dentro de la red corporativa y ve todas las aplicaciones de la empresa.

Se configuró el disparador **"Cuando se crea un elemento"** de SharePoint, apuntando a la dirección del sitio y a la lista "Solicitud de permisos". Como la lista no aparecía automáticamente en el listado de sitios (por no haberse creado desde el mismo equipo/cuenta), se explicó cómo resolverlo: ir a la lista de SharePoint, copiar la URL (hasta antes de la palabra "Lists"), volver al flujo y, en el campo de dirección del sitio, seleccionar "Ingresar un valor personalizado" y pegar esa URL; una vez hecho esto, el campo "Nombre de la lista" ya mostraba la lista correctamente.

Después se agregó la acción **"Obtener mi perfil" (Get My Profile V2, de Office 365 Users)**, que sirve para obtener la información de la persona que está logueada en la plataforma (por ejemplo, su nombre para mostrarlo (Display Name)).

Por último, se agregó la acción **"Enviar un correo electrónico (V2)"** de Outlook/Office 365. En el campo "Para" se puso la propia cuenta del curso; como asunto se escribió "Nuevo elemento creado"; y en el cuerpo se usó contenido dinámico (el ícono del rayo ⚡) para insertar el nombre obtenido de "Get My Profile" (Display Name / nombre preferido) y datos del elemento recién creado en la lista (por ejemplo, el ID del elemento, tomado del disparador "Cuando se crea un elemento").

En este punto se explicó la diferencia entre **contenido dinámico** y texto "quemado" (fijo): al usar contenido dinámico en el rayito, solo se muestran los metadatos generados por las acciones *anteriores* a la acción donde uno está parado; por eso, por ejemplo, desde la acción de correo se puede ver tanto la información de "Get My Profile" como la del disparador "Cuando se crea un elemento", pero no al revés.

Con el flujo guardado, se probó usando el botón **"Probar" (Test)** en modo manual: el flujo quedó a la espera de que se creara un elemento en la lista. Se fue entonces a la lista de SharePoint y se creó un nuevo elemento de prueba (nombre "Jonathan", fecha del permiso para el día siguiente, justificación "diligencia personal"; el campo de aprobación se dejó vacío por el momento, aunque se comentó que lo ideal sería ocultarlo, pues no debería diligenciarse en esta etapa). Al guardar el elemento, el flujo se disparó, se ejecutaron todas las acciones (marcadas con chulitos verdes) y llegó el correo de confirmación con el nombre de la persona logueada y el título del elemento recién creado.

Con esto quedó lista la primera automatización, y el profesor preguntó qué tan fácil les había parecido, antes de anunciar el desayuno: "vamos a desayunar y volvemos a las 10:00".

---

*(Pausa / descanso de la clase)*

---

## Segunda automatización: formulario de Microsoft Forms con aprobación

Al regresar del descanso, se saludó a los estudiantes virtuales y se continuó con la siguiente parte: ahora se construiría un **formulario de Microsoft Forms** que serviría de "front end" de la herramienta —es decir, lo que el usuario digite en el formulario se registraría automáticamente en la lista de SharePoint y, además, iniciaría un flujo de aprobación—. Cuando se registre la solicitud, el elemento quedará en estado "Pendiente"; y cuando alguien la apruebe o rechace, el flujo continuará.

Se creó el formulario desde los nueve puntos → Forms (buscándolo si no aparece directamente). Se eligió "Cuestionario" (o formulario en blanco) y se le dio como título **"Solicitud de permisos, curso Automate"**, con una breve descripción.

Se recordó que el formulario debía pedir lo mismo que la lista de SharePoint: nombres, fecha del permiso y justificación (la aprobación no tiene nada que ver con el formulario, ya que esa la define el jefe, no quien solicita). Se agregaron entonces tres preguntas de tipo texto:

1. **"Nombres"** (respuesta obligatoria).
2. **"Fecha del permiso"** (tipo fecha).
3. **"Justificación del permiso"** (tipo respuesta larga, para permitir más texto, y también obligatoria).

Con el formulario construido (sin necesidad de guardarlo manualmente, ya que se guarda automáticamente), se volvió al flujo de Power Automate para modificarlo:

- Se eliminó el disparador anterior ("Cuando se crea un elemento") y se agregó uno nuevo: **"Cuando se envía una nueva respuesta"** (Forms), buscando por la palabra "forms" entre los conectores disponibles (en inglés "When a new response is submitted").
- Este disparador pedía el **ID del formulario**. Para no complicarse buscando el formulario en el listado desplegable (que a veces no lo muestra), se explicó un truco: entrar al formulario, y en la URL, después de "id=", copiar todo el texto alfanumérico que sigue (ese es el identificador único del formulario); luego, en el flujo, seleccionar "Ingresar un valor personalizado" y pegar ese ID.
- Se agregó la acción **"Obtener detalles de la respuesta" (Get response details)**, que también pide el ID del formulario (el mismo de arriba) y, además, el **ID de la respuesta**, que se toma dinámicamente desde el disparador anterior (ya que cada respuesta de Forms genera también un identificador único).
- Luego se agregó una acción de SharePoint: **"Crear elemento" (Create item)**, apuntando a la misma lista "Solicitud de permisos" (usando de nuevo la URL del sitio como valor personalizado). En los parámetros avanzados ("Mostrar todo") se mapearon los campos: **Título** = Nombres (desde la respuesta del formulario), **Fecha del permiso** y **Justificación** (también desde las respuestas del formulario), y **Aprobación** = "Pendiente" (fijo, ya que todavía no ha sido evaluada por nadie).
- A continuación se agregó la acción de aprobación: se buscó "Aprobaciones" (Approvals) y se seleccionó **"Iniciar y esperar una aprobación" (Start and wait for an approval)**, de tipo "Aprobar/Rechazar - Primero en responder" (hay otras variantes, como "todos deben aprobar", donde el flujo no continúa hasta que todos los aprobadores respondan). Se configuró el título de la aprobación como "Solicitud de permiso", el nombre de la persona que diligenció el formulario (desde contenido dinámico), y como aprobador se puso la propia cuenta del curso (se explicó que, si se ponen varios correos, a todos les llega la notificación, pero con la opción elegida basta con que el primero apruebe o rechace para que el flujo continúe).
- Finalmente, se armó una **condición (If)**: si el "Resultado" de la aprobación es igual a **"Approve"** (importante: en inglés, aun si la interfaz está en español, porque el valor interno que retorna la acción de aprobación siempre viene en inglés), entonces se envía un correo indicando que el permiso fue aprobado y se actualiza el elemento de la lista; si no, se envía un correo de rechazo y también se actualiza el elemento, pero con el estado "Rechazado".

  En la rama **verdadera (True)**: se agregó "Enviar un correo electrónico (V2)" al correo de quien respondió el formulario (contenido dinámico "Responder's email"), con asunto "Su permiso fue aprobado" y cuerpo "Hola [nombre], su permiso fue aprobado. Feliz día."; y después, **"Actualizar elemento" (Update item)** de SharePoint, usando el ID del elemento creado anteriormente (tomado de la acción "Crear elemento"), cambiando el campo Aprobación a **"Aprobado"**.

  En la rama **falsa (False)**: de forma análoga, se copió la acción de correo (clic derecho → copiar acción → pegar) y se cambió el asunto a "Su permiso fue rechazado" y el cuerpo correspondiente; y se agregó otra acción "Actualizar elemento" con Aprobación = **"Rechazado"**.

### Depuración y pruebas del flujo de aprobación

Al guardar y probar el flujo en vivo aparecieron varios problemas típicos, que se fueron resolviendo en clase (y que sirven como aprendizaje sobre errores comunes al construir automatizaciones):

- **El formulario solo aceptaba una respuesta por persona.** Por defecto, Forms puede estar configurado para admitir una sola respuesta; había que entrar a la configuración del formulario (los tres puntos) y activar "Cualquier persona puede responder" y permitir múltiples respuestas, para poder hacer varias pruebas seguidas.
- **Confusión entre "Aprobado" (español) y "Approve" (valor real de la variable).** Aunque la interfaz mostraba las opciones traducidas al español, el valor que efectivamente retorna la acción de aprobación siempre es "Approve"/"Reject" en inglés. Poner "Aprobado" en la condición hacía que la comparación fallara siempre y el flujo se fuera por la rama de rechazo, incluso si se había aprobado. La solución fue cambiar el valor de comparación a "Approve".
- **Error "el parámetro de entrada 'email' es requerido" en el envío de correo.** Esto ocurría cuando el campo "Para" quedaba vacío o mal enlazado; se corrigió usando el contenido dinámico "Responder's email" desde la acción "Obtener detalles de la respuesta".
- **Usar el ID equivocado en alguna acción** (por ejemplo, pegar la URL del sitio de SharePoint en el campo pensado para el ID del formulario, o viceversa), lo que hacía que la acción no encontrara ni el formulario ni la lista.
- **Olvidar diligenciar el campo "Aprobación" al crear el elemento en la lista**, dejándolo vacío en lugar de "Pendiente".
- **Olvidar agregar la acción "Actualizar elemento" tras la aprobación**, lo que dejaba el estado del registro siempre en "Pendiente" en la lista, aun después de haber aprobado o rechazado la solicitud.
- Como recomendación general ante fallos recurrentes en una acción, el profesor sugirió eliminarla por completo y volverla a crear desde cero, en lugar de insistir editando la misma acción ya "dañada".

Durante las pruebas, varios estudiantes tuvieron inconvenientes puntuales que se resolvieron en vivo, compartiendo pantalla: a **Sair Stephania López Valencia** no le aparecía la acción "Obtener mi perfil" porque tenía activada otra acción distinta ("actualizar mi perfil"); a **Juan Felipe Muñoz Zuluaga** no le aparecían los desencadenadores porque su entorno de trabajo estaba vacío (distinto al entorno "aula"); **Carlos Andrés Quintero Laverde** tuvo un error en la acción "Iniciar y esperar" y, más adelante, no le aparecía ningún valor en la columna de aprobación de su lista al crear el elemento (se detectó que no estaba diligenciando el campo "Aprobación" en la acción "Crear elemento"); y **Angie Tatiana Salazar Muñetón** tuvo dificultades para copiar correctamente la URL de su lista de SharePoint, resueltas mostrando hasta qué parte de la URL debía copiarse.

También se mostró cómo revisar el **historial de ejecuciones** de un flujo (desde la vista principal de "Mis flujos"): ahí se puede ver la fecha de creación, la última modificación, y el listado de todas las ejecuciones (exitosas o fallidas); se puede entrar a cada ejecución para ver el estado exacto de los datos en ese momento, lo cual da trazabilidad completa sobre lo que hizo la automatización. Como buena práctica, se recomendó borrar los elementos de prueba de la lista una vez la automatización quede funcionando correctamente, para que arranque "limpia" cuando entre en operación real.

Sobre el final de esta parte, se comentó brevemente que si en el futuro se necesitara leer y **interpretar** el contenido de un correo (por ejemplo, distinguir asuntos con lenguaje libre), ya no bastaría con una automatización estructurada como esta, sino que habría que incorporar un LLM (modelo de lenguaje) para el razonamiento; pero por ahora, con un asunto de correo con estructura fija, la automatización tradicional es suficiente.

## Cierre de la clase: material, tarea y trabajo final

Con el flujo de aprobación funcionando correctamente para todos (incluidos los estudiantes virtuales), el profesor cerró la sesión con varios anuncios:

- Queda como ejercicio pendiente (mencionado explícitamente como "tarea") resolver cómo **ocultar el campo "Aprobación" del formulario** —o, más precisamente, evitar que ese campo se pueda diligenciar desde el formulario, ya que la aprobación no le corresponde a quien solicita el permiso sino al jefe—; se revisará más adelante cómo hacerlo.
- En el equipo de Teams del curso, dentro de los archivos compartidos de "Automatizaciones", queda disponible el **material de la clase de hoy**: la presentación (PDF) y unos archivos de Excel con los que se trabajará más adelante otros flujos —esos Excel se trabajarán la próxima semana—.
- La **próxima clase** se continuará con **Power Automate Desktop** (la versión que se instaló la noche anterior).
- Antes de terminar, se pidió a los estudiantes ingresar a un archivo de Excel compartido en la pestaña de **"Equipos"** de Teams (dentro del canal del curso) para **conformar los grupos del trabajo final**. El trabajo final consiste en construir una automatización propia en Power Automate —no tiene que ser algo muy complejo, similar a lo que se hizo en esta clase— pensando en algo que a cada estudiante o equipo le pueda servir, y explorando la herramienta por su cuenta. Se aclaró que el número de grupo que se diligencie en ese Excel **no** corresponde al orden final de presentación (eso se definirá después); el número sirve, por ahora, para saber cuántos grupos habrá en total y así calcular cuánto tiempo tomarán las presentaciones, y si alcanzará con una sola clase o se necesitarán dos.
- Se hizo un último llamado a los estudiantes virtuales para confirmar que todo había quedado claro, y se despidió agradeciendo a todos por la sesión.
