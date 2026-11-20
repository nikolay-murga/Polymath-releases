# Polymath para Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

Una pequeña barra de ayuda para conversaciones y reuniones. Escucha a la otra persona y traduce su voz a su idioma, sugiere una respuesta en el idioma de la conversación, resuelve una tarea de la pantalla y responde cualquier pregunta en el chat.

**Solo usted ve la barra.** No aparece cuando comparte la pantalla en Zoom, Teams, Meet, Discord u OBS, ni en las capturas de pantalla y las grabaciones de pantalla.

## Funciones

- **Escuchar**. Escucha el sonido del ordenador (la voz de la otra persona en una llamada), reconoce frases, muestra una traducción a su idioma nativo y, cuando se dirigen a usted, una respuesta lista en el idioma de la conversación con su traducción. Haga clic en una respuesta para copiarla. El modo «Solo cuando haga falta una respuesta» muestra solo las frases a las que conviene contestar.
- **Pantalla**. Una captura de pantalla se envía al modelo: resolver una tarea, responder una pregunta de prueba, revisar código.
- **Observar**. Vigila la pantalla y responde cuando aparece en ella una nueva pregunta o tarea. Se apaga solo después de 10 minutos.
- **Chat**. Preguntas normales. Una cifra al principio elige un comando: `1` Rápido (respuesta corta, modelo rápido), `3` Respuesta (respuesta a la última pregunta escuchada, teniendo en cuenta la conversación), `5` Traducir.
- El modelo ve las últimas frases de la conversación, así que en el chat puede preguntar: «¿cómo respondo a su última pregunta?».
- **Base de conocimientos**. Sus propios archivos `.txt` y `.md` con respuestas preparadas a preguntas frecuentes. La respuesta adecuada se busca en el ordenador, sin internet, y se muestra al instante mientras el modelo todavía responde.
- **Comandos propios**. Añada sus propios comandos con cifras, con sus instrucciones, su modelo y sus ajustes de pantalla o sonido.
- **Historial y exportación**. Guardado opcional de las conversaciones, cifrado, y exportación a un archivo de texto.

## Instalación

En cada versión se publican dos archivos listos:

- `Polymath-Setup-<versión>.exe` - el instalador, se muestra en el idioma de Windows y admite 22 idiomas. Puede elegir la carpeta, no necesita derechos de administrador, los accesos directos van al escritorio y al menú Inicio, y el programa se inicia al terminar la instalación.

Windows SmartScreen puede advertir sobre un editor desconocido, porque el archivo todavía no está firmado. Haga clic en «Más información» y luego en «Ejecutar de todos modos».

Requisitos: Windows 10 versión 2004 (mayo de 2020) o más reciente, o Windows 11. En sistemas más antiguos no funciona ocultarse de la captura de pantalla.

Actualizaciones: la copia instalada comprueba esta página en busca de nuevas versiones unos segundos después de iniciarse. Cuando aparece una versión más nueva, el programa muestra una tarjeta y descarga la actualización solo con su consentimiento. La actualización se instala en la misma carpeta y el programa se vuelve a iniciar.

## Primer inicio

1. Abra los ajustes (el engranaje de la barra).
2. Elija un proveedor de modelos, pegue la clave API y haga clic en «Guardar clave». El enlace «Obtener una clave» abre la página del proveedor.
3. Haga clic en «Probar conexión». Aparecerá una lista de modelos disponibles, y al hacer clic en un modelo se pone en el campo.
4. Indique su idioma nativo. En la sección «Base de conocimientos», describa brevemente su perfil en «Sobre usted» (trabajo, experiencia). El modelo lo usa en sus respuestas.
5. Haga clic en «Guardar» (o pulse Ctrl+S).

### Proveedores

| Proveedor                          | Modelo por defecto       | Imágenes (Pantalla/Observar) | Sonido directo |
| ---------------------------------- | ------------------------ | ---------------------------- | -------------- |
| Google Gemini                      | gemini-flash-lite-latest | sí                           | sí             |
| OpenAI                             | gpt-5-mini               | sí                           | no             |
| Anthropic Claude                   | claude-sonnet-5-5        | sí                           | no             |
| OpenRouter                         | openrouter/auto          | sí                           | no             |
| Groq                               | openai/gpt-oss-120b      | no                           | no             |
| Mistral                            | mistral-medium-latest    | sí                           | no             |
| Ollama (local)                     | llama3.2                 | no                           | no             |
| Personalizado (compatible con OpenAI) | cualquiera            | depende del modelo           | no             |

Los proveedores cambian el nombre de sus modelos. Si un modelo no se encuentra, haga clic en «Probar conexión» y elija uno de la lista.

El «Modelo rápido» lo usan los comandos «Rápido» y «Traducir». Puede dejarlo vacío, y entonces se usa el modelo principal.

Cuando un modelo responde 503 (sobrecargado) o 429 (sin cuota), el programa pregunta de inmediato al otro modelo de la pareja.

### Modelo de reserva

En la sección «Modelo de reserva» de los ajustes se define otro proveedor al que el programa consulta cuando los dos modelos principales responden 503 o 429. Por ejemplo, Anthropic Claude (por defecto `claude-haiku-5-5`, un modelo rápido). La clave de reserva se guarda por separado. Si no existe, se usa la clave del mismo proveedor de la sección «Modelo». La reserva se omite cuando no puede leer lo que se envía, como una imagen de la pantalla (Pantalla/Observar) o el sonido.

## Reconocimiento de voz (para «Escuchar»)

En los ajustes de «Reconocimiento de voz» hay cuatro opciones:

1. **A través del modelo** (por defecto). La frase va directamente al modelo de chat. Funciona con Google Gemini, con la misma clave.
2. **Whisper API en la nube**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, rápido y barato) o su propio servidor compatible con OpenAI. La clave de reconocimiento se guarda aparte de la clave del modelo.
3. **Local (whisper.cpp)**. El sonido nunca sale del ordenador. Se instala con un solo comando y los archivos van a `%APPDATA%\Polymath\whisper`. Después elija «Local» y haga clic en «Probar reconocimiento». Por defecto se usa el modelo pequeño (466 MB). Otros tamaños y la aceleración con tarjetas gráficas NVIDIA están disponibles como opciones del script de instalación.
4. **Local (NVIDIA Parakeet)**. También en este ordenador, más rápido que whisper.cpp en el procesador y normalmente más preciso. El modelo conoce 25 idiomas europeos (inglés, ruso, ucraniano, alemán, francés, español y otros), pero no el turco ni el chino. El botón «Descargar Parakeet» de los ajustes lo instala. En total son unos 520 MB. Después elija «Local (NVIDIA Parakeet)» y haga clic en «Probar reconocimiento». La primera frase tras una pausa tarda 7-10 segundos en lo que se carga el modelo, y las siguientes, menos de un segundo. Tras 10 minutos sin voz, el servidor se detiene y libera la memoria.

En el primer inicio en un ordenador nuevo, la barra pregunta una vez cómo reconocer la voz: con Gemini (no hay nada que descargar) o con Parakeet en este ordenador (el programa descarga unos 520 MB, con progreso y un botón para cancelar). La respuesta se puede cambiar después en los ajustes.

El botón «Probar reconocimiento» funciona con las cuatro opciones.

## Cómo se usa

| Acción                            | Atajo                          |
| --------------------------------- | ------------------------------ |
| Mostrar / ocultar la barra        | `Ctrl` + `Alt` + `P`           |
| Resolver una tarea de la pantalla | `Ctrl` + `Alt` + `2`           |
| Observar la pantalla (sí/no)      | `Ctrl` + `Alt` + `4`           |
| Escuchar la llamada (sí/no)       | `Ctrl` + `Alt` + `7`           |
| Clic a través de la barra (sí/no) | `Ctrl` + `Alt` + `T`           |
| Enviar                            | `Enter`                        |
| Nueva línea                       | `Mayús` + `Enter`              |
| Detener la respuesta              | `Ctrl` + `.` o el botón `■`    |
| Nueva conversación                | `Ctrl` + `N` o el botón `+`    |
| Petición anterior                 | `↑` / `↓` en un campo vacío    |
| Ocultar la barra                  | `Esc`                          |

Los atajos se cambian en los ajustes: haga clic en el campo y pulse la combinación. Si otro programa ya usa ese atajo, la barra lo indica.

La barra se arrastra por su título, y su posición se recuerda. El ancho, la opacidad y el tamaño de letra se pueden ajustar.

### Aspecto y ratón

La sección «Interfaz» de los ajustes:

- **Tema**: oscuro (grafito, por defecto) o claro (marfil).
- **Opacidad de la barra**: toda la barra con su texto (30-100 %).
- **Opacidad del fondo**: solo el fondo de la barra, el texto se mantiene nítido (20-100 %).
- **Clic a través de la barra**: los clics atraviesan la barra de ayuda y llegan a la ventana de debajo. La barra no se puede mover ni pulsar con el ratón, pero el teclado y los atajos siguen funcionando. Se activa y desactiva con `Ctrl` + `Alt` + `T`, y en el título de la barra aparece la marca «clic a través». La ventana de ajustes siempre es una ventana normal.
- **Pulsar botones al pasar el cursor**: deje el cursor sobre un botón de la barra (3 segundos por defecto, se puede de 1,5 a 5) y se pulsa solo. Bajo el botón se llena una franja. Funciona también en el modo de clic a través.

«Escuchar» capta el sonido de todo el sistema. Use auriculares: así solo se graba a la otra persona y no su propia voz.

## Comandos propios

Los comandos con cifras se guardan en `%APPDATA%\Polymath\commands.json` (botón «Abrir commands.json» en los ajustes). El archivo se vuelve a leer en cada llamada, no hace falta reiniciar. Ejemplo:

```json
{
  "1": {
    "name": "Entrevista",
    "instructions": "Responde como un desarrollador Java senior en una entrevista de trabajo. Responde en {conversation_language} y después da una breve traducción a {native}.",
    "model": "main"
  }
}
```

Campos: `name`, `instructions` (obligatorio), `model` (`main` o `small`), `screen: true` (adjuntar una captura de pantalla), `watch: true` (observar la pantalla), `listen: true` (activar «Escuchar»). Marcadores: `{native}` es su idioma y `{conversation_language}` es el idioma de la conversación.

## Ocultarse de la captura de pantalla

Las ventanas se crean con el mecanismo de Windows que las excluye de la captura (`WDA_EXCLUDEFROMCAPTURE`). Al capturar la pantalla se ve lo que hay debajo de la ventana. Zoom, Teams, Google Meet en el navegador, Discord, OBS, la Herramienta de recorte, PrintScreen y la Xbox Game Bar respetan este mecanismo.

Además:

- no hay botón en la barra de tareas ni entrada en Alt+Tab;
- el icono de la bandeja está desactivado por defecto (la bandeja se ve cuando se comparte toda la pantalla);
- no hay ventanas emergentes del sistema: las sugerencias, las listas y los menús se dibujan dentro de la barra, y el menú contextual está desactivado.

Límites:

- Ocultarse no protege frente a una cámara apuntada al monitor ni frente a la captura por HDMI por hardware.
- Si comparte una **ventana** de un programa (no toda la pantalla) y la barra queda encima, la otra parte ve lo que hay debajo de la barra. Es lo esperado.
- En Windows anterior a la versión 2004 de Windows 10, en la captura aparece un rectángulo negro en lugar de la barra.
- Los enlaces y archivos abiertos (commands.json, la carpeta de datos) se abren en programas normales y son visibles al compartir la pantalla.

## Base de conocimientos

La sección «Base de conocimientos» de los ajustes:

- **Sobre usted**: información general sobre usted. El modelo la usa en cada respuesta.
- **Archivos**: el botón «Añadir archivos» o arrastrar archivos `.txt` y `.md` a la sección. Los archivos se copian a `%APPDATA%\Polymath\knowledge` (botón «Abrir carpeta»). Puede editarlos allí, y el programa recoge los cambios solo. Un archivo con el mismo nombre se reemplaza. El límite es de 2 MB por archivo, en UTF-8, UTF-16 o Windows-1251.
- **Usar la base en las respuestas**: se activa en cuanto la base tiene un archivo.
- **Mostrar al instante una coincidencia de la base, antes de la respuesta del modelo**: lo mismo.

Cómo funciona. Para una pregunta del chat y para cada frase de la otra persona en «Escuchar», el programa primero busca una respuesta en sus archivos, sin internet y sin modelo. La coincidencia aparece al instante como un bloque azul «De la base de conocimientos» encima de la respuesta del modelo, con un botón «Copiar» al lado. Al mismo tiempo, el modelo recibe estos datos (toda la base si es pequeña, o las partes encontradas en caso contrario) y responde basándose en ellos. La búsqueda entiende las distintas formas de las palabras. La búsqueda local no encuentra una pregunta escrita en otro idioma, pero el modelo responde igualmente con la base.

Tres formas de escribir los archivos:

```markdown
# ¿Qué salario espera?
Desde 5.000 USD netos, abierto a negociación.

# ¿Por qué deja su trabajo actual?
Quiero más trabajo de arquitectura.
```

```text
Q: ¿Cuál es su periodo de preaviso?
A: Dos semanas.
```

O simplemente párrafos separados por una línea vacía. La primera línea corta de un párrafo es su tema.

## Historial y exportación

La sección «Historial» de los ajustes:

- **Guardar el historial en disco**. Desactivado por defecto: el historial queda solo en memoria hasta que se cierra el programa. Cuando está activado, cada pregunta y respuesta se añade al archivo del día en `%APPDATA%\Polymath\history`, y cada línea se cifra con DPAPI de Windows, así que solo su cuenta de Windows puede leerla.
- **Nombre en el historial**. Firma sus preguntas en las exportaciones. Vacío significa el nombre de usuario de Windows.
- **Conservar, días**. Los días antiguos se borran al iniciar. 0 significa conservar todo.
- **Exportar** esta sesión, hoy, 7 días, 30 días o todo el tiempo. «Exportar a .txt» guarda un archivo en `Documentos\Polymath`, y «Copiar como texto» pone el mismo texto en el portapapeles.
- **Borrar el historial** elimina los archivos del historial y las entradas de esta sesión (hay que pulsar el botón dos veces).

Qué se registra:

- chat: la pregunta (con el comando y la marca de captura de pantalla) y la respuesta del modelo;
- Escuchar: la frase de la otra persona y su traducción, y la respuesta sugerida con su traducción cuando hizo falta una respuesta;
- Observar: respuestas a tareas de la pantalla. Las ejecuciones vacías no se registran.

El archivo de exportación no está cifrado. El Explorador y el Bloc de notas, abiertos con el botón «Mostrar el archivo», son visibles al compartir la pantalla.

## Privacidad

- Las claves API se guardan cifradas por Windows (DPAPI) en `%APPDATA%\Polymath\settings.json`.
- Por defecto el historial está solo en memoria y desaparece al cerrar el programa. El guardado en disco se activa en los ajustes, y los archivos del historial se cifran con DPAPI.
- Los archivos de la base de conocimientos se guardan sin cifrar en `%APPDATA%\Polymath\knowledge` y se buscan en el ordenador. Van al modelo solo junto con una pregunta: toda la base si es pequeña, o las partes coincidentes en caso contrario.
- El sonido y las capturas de pantalla se envían solo al proveedor elegido (o al de reserva), y solo mientras estén activados «Escuchar», «Pantalla» u «Observar». Con whisper.cpp o Parakeet locales, el sonido nunca sale del ordenador.
- El registro de errores está en `%APPDATA%\Polymath\logs\app.log`. No contiene texto de las conversaciones.

## Inicio en segundo plano

La casilla «Iniciar al entrar en Windows» arranca Polymath oculto. Muestre la barra con `Ctrl` + `Alt` + `P`.

## Requisitos y límites

- Windows 10 versión 2004 o más reciente, o Windows 11.
- Se necesita internet para los modelos en la nube. El reconocimiento de voz local funciona sin red después de la instalación.
- Una clave de al menos un proveedor de modelos. Las claves son suyas y las factura el proveedor.
