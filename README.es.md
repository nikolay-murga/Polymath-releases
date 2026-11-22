# Polymath para Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**
(Tu socio de IA discreto, en cada conversación)

Polymath se sienta a tu lado y te ayuda cuando te faltan palabras o conocimientos. Oye lo que dice la otra persona, ve lo que hay en tu pantalla y te sugiere qué hacer a continuación. Nadie más lo ve y nunca habla por ti.

### Para qué sirve

- **Hablar con personas cuyo idioma no conoces.** Polymath escucha a la otra persona y te muestra lo que dijo. Luego te sugiere qué responder en su idioma y en tu lengua materna (para que siempre entiendas qué le estás diciendo exactamente). Sigues en la conversación tú mismo, en lugar de esconderte detrás de un traductor.
- **Citas en línea.** Polymath puede vigilar tu pantalla y sugerirte cómo responder en el idioma de la otra persona y en tu lengua materna (para que siempre entiendas qué estás escribiendo exactamente). Escribes un mensaje que suena a ti, solo que mejor.
- **Ligar.** Recibe una idea para responder, un chiste o un cumplido justo cuando lo necesitas.
- **Tareas cotidianas.** Haz una pregunta, saca una captura de pantalla con la aplicación y recibe una respuesta que se ajusta a tu situación.
- **Cosas difíciles y confusas.** ¿No sabes dónde hacer clic o por qué algo no funciona? Muéstrale tu pantalla a Polymath y señalará el error y te dirá cómo corregirlo.

### Lo que antes daba miedo, ahora está a tu alcance con Polymath

- Ir a una entrevista de trabajo en línea y saber qué decir.
- Configurar anuncios en Google o Meta sin tirar el presupuesto.
- Hacer tu primer sitio web y publicarlo en cualquier hosting.
- Entender un contrato de alquiler o de crédito sin pasar por alto la letra pequeña.
- Rellenar la declaración de la renta o tramitar un visado sin errores en los documentos.
- Escribir un currículum y una carta de presentación que destaquen, también en un idioma extranjero.
- Negociar un precio o un descuento y hablar de las condiciones con el casero, un contratista o un cliente.
- Entender la carta del banco, de Hacienda o del seguro y saber qué quieren de ti en realidad.
- Configurar un router Wi-Fi, una impresora o un teléfono cuando nada funciona y el técnico es caro o no está disponible.
- Redactar una queja o reclamación convincente a una tienda, una aerolínea o la comunidad de vecinos.
- Prepararte para una conversación difícil con tu jefe, tu pareja o tus padres y encontrar las palabras adecuadas.

Antes hacía falta un especialista a tu lado o una llamada a un amigo. Ahora tienes a Polymath, que entiende de todo y está siempre a mano.

---

Una pequeña barra de ayuda para conversaciones y reuniones. Escucha a la otra persona y traduce su voz a tu idioma, sugiere una respuesta en el idioma de la conversación, resuelve una tarea desde la pantalla y responde cualquier pregunta en el chat.

**Solo tú ves la barra.** No aparece cuando compartes la pantalla en Zoom, Teams, Meet, Discord u OBS, ni en capturas de pantalla ni en grabaciones.

## Funciones

- **Listen** (`7` / `Ctrl` + `Alt` + `7`). Escucha el sonido del ordenador (la voz de la otra persona en una llamada), reconoce frases, muestra una traducción a tu lengua materna y, cuando se dirigen a ti, una respuesta lista en el idioma de la conversación con su traducción. Un clic en una respuesta la copia. El modo «Solo cuando hace falta responder» muestra solo las líneas a las que debes contestar.
- **Screenshot** (`2` / `Ctrl` + `Alt` + `2`). Una captura de pantalla va al modelo: resolver una tarea, responder una pregunta de un examen, revisar código.
- **Watch** (`4` / `Ctrl` + `Alt` + `4`). Vigila la pantalla y responde cuando aparece en ella una pregunta o tarea nueva. Se apaga solo a los 10 minutos.
- **Chat**. Preguntas normales. Un dígito al principio elige un comando: `1` Quick (corto, modelo rápido), `3` Answer (una respuesta a la última pregunta oída, teniendo en cuenta la conversación), `5` Translate.
- El modelo ve las últimas frases de la conversación, así que en el chat puedes preguntar «¿cómo respondo a su última pregunta?».
- **Base de conocimientos**. Tus propios archivos `.txt` y `.md` con respuestas listas a preguntas frecuentes. Una respuesta adecuada se encuentra en el ordenador, sin internet, y se muestra al instante mientras el modelo todavía responde.

## Instalación

Los archivos listos están en la carpeta `dist`:

- `Polymath-Setup-<versión>.exe` - el instalador, sigue el idioma de Windows y admite 22 idiomas: puedes elegir la carpeta, no hacen falta permisos de administrador, accesos directos en el escritorio y en el menú Inicio, el programa se inicia tras la instalación;

Windows SmartScreen puede avisar de un editor desconocido (el archivo no está firmado). Haz clic en «Más información» y «Ejecutar de todas formas».

Requisitos: Windows 10 versión 2004 (mayo de 2020) o posterior, Windows 11. En sistemas más antiguos el ocultamiento de la captura de pantalla no funciona.

## Primer inicio

1. Abre los ajustes (el engranaje de la barra).
2. Elige un proveedor de modelo, pega la clave de API y haz clic en «Guardar clave». El enlace «Obtener una clave» abre la página del proveedor.
3. Haz clic en «Probar la conexión». Aparece una lista de modelos disponibles, un clic en un modelo lo pone en el campo.
4. Indica tu lengua materna. En la sección «Base de conocimientos», descríbete brevemente en «Sobre usted» (trabajo, experiencia). El modelo lo usa en sus respuestas.
5. Haz clic en «Guardar» (o Ctrl+S).

### Proveedores

| Proveedor                    | Modelo por defecto       | Imágenes (Screenshot/Watch) | Sonido directo |
| ---------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini                | gemini-flash-lite-latest | sí                      | sí             |
| OpenAI                       | gpt-5-mini               | sí                      | no             |
| Anthropic Claude             | claude-sonnet-5-5        | sí                      | no             |
| OpenRouter                   | openrouter/auto          | sí                      | no             |
| Groq                         | openai/gpt-oss-120b      | no                      | no             |
| Mistral                      | mistral-medium-latest    | sí                      | no             |
| Ollama (local)               | llama3.2                 | no                      | no             |
| Personalizado (compatible con OpenAI) | cualquiera      | depende del modelo      | no             |

Los proveedores cambian el nombre de sus modelos. Si no se encuentra un modelo, haz clic en «Probar la conexión» y elige uno de la lista.

El «Modelo rápido» lo usan los comandos Quick y Translate. Puede quedar vacío, entonces se usa el modelo principal.

Cuando un modelo responde 503 (sobrecargado) o 429 (sin cuota), el programa consulta al instante al otro modelo del par.

### Modelo de reserva

La sección «Modelo de reserva» de los ajustes: otro proveedor al que el programa consulta cuando los dos modelos de arriba responden 503 o 429. Por ejemplo, Anthropic Claude (`claude-haiku-5-5` por defecto, uno rápido). La clave de reserva se guarda aparte. Sin ella se usa la clave del mismo proveedor de la sección «Modelo». La reserva se omite cuando no puede leer lo que se envía: una imagen de la pantalla (Screenshot/Watch) o sonido.

## Reconocimiento de voz (para Listen)

Los ajustes de «Reconocimiento de voz» ofrecen cuatro motores:

1. **A través del modelo** (por defecto). La frase va directamente al modelo del chat. Funciona con Google Gemini, con la misma clave.
2. **API de Whisper en la nube**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, rápido y barato) o tu propio servidor compatible con OpenAI. La clave de reconocimiento se guarda aparte de la clave del modelo.
3. **Local (whisper.cpp)**. El sonido nunca sale del ordenador. Se instala con un comando:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

En el programa instalado el script está en `<carpeta del programa>\resources\scripts`. Opciones: `-Model tiny|base|small|medium|large-v3-turbo` (por defecto small, 466 MB) y `-Cuda` para tarjetas gráficas NVIDIA. Los archivos van a `%APPDATA%\Polymath\whisper`. Después elige «Local» y haz clic en «Probar el reconocimiento».

4. **Local (NVIDIA Parakeet)**. También en este ordenador, más rápido que whisper.cpp en un procesador y normalmente más preciso. El modelo `parakeet-tdt-0.6b-v3` conoce 25 idiomas europeos (inglés, ruso, ucraniano, alemán, francés, español y otros), pero no turco ni chino. Funciona mediante [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx). El botón «Descargar Parakeet» de los ajustes lo deja todo en su sitio, o un comando:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

En total unos 520 MB. La opción `-Model v2` toma el modelo solo para inglés, algo más preciso en inglés. Los archivos van a `%APPDATA%\Polymath\parakeet`. Después elige «Local (NVIDIA Parakeet)» y haz clic en «Probar el reconocimiento». La primera frase tras una pausa espera 7-10 s mientras se carga el modelo, las siguientes tardan menos de un segundo. Tras 10 minutos sin voz el servidor se detiene y libera la memoria. Ambas descargas (el programa y el modelo) se comprueban con el SHA-256 que publica GitHub. Un archivo que no coincide se descarta y no se instala nada. Sin un hash publicado no hay instalación.

En el primer inicio en un ordenador nuevo la barra pregunta una vez cómo reconocer la voz: a través de Gemini (nada que descargar) o con Parakeet en este ordenador (la aplicación descarga unos 520 MB, con progreso y un botón de cancelar). La respuesta se puede cambiar después en los ajustes.

El botón «Probar el reconocimiento» funciona con los cuatro motores.

## Cómo se usa

| Acción                            | Atajo                          |
| --------------------------------- | ------------------------------ |
| Mostrar / ocultar la barra        | `Ctrl` + `Alt` + `P`           |
| Respuesta rápida (breve, modelo rápido) | `Ctrl` + `Alt` + `1` |
| Resolver una tarea desde la pantalla | `Ctrl` + `Alt` + `2`        |
| Respuesta a la pregunta recién oída | `Ctrl` + `Alt` + `3` |
| Vigilar la pantalla (sí/no)       | `Ctrl` + `Alt` + `4`           |
| Traducir | `Ctrl` + `Alt` + `5` |
| Escuchar la llamada (sí/no)       | `Ctrl` + `Alt` + `7`           |
| Clic a través de la barra (sí/no) | `Ctrl` + `Alt` + `T`           |
| Enviar                            | `Enter`                        |
| Nueva línea                       | `Shift` + `Enter`              |
| Detener la respuesta              | `Ctrl` + `.` o el botón `■`    |
| Nueva conversación                | `Ctrl` + `N` o el botón `+`    |
| Petición anterior                 | `↑` / `↓` en un campo vacío    |
| Ocultar la barra                  | `Esc`                          |

### Comandos cortos y largos

Los comandos cortos funcionan dentro de la barra, los largos (con `Ctrl` + `Alt`) desde cualquier ventana. Un dígito en un campo vacío elige un comando, también funciona `1 su texto`.

| Acción | Corto (en la barra) | Largo (desde cualquier ventana) |
| --- | --- | --- |
| Respuesta rápida (breve, modelo rápido) | `1` | `Ctrl` + `Alt` + `1` |
| Resolver una tarea desde la pantalla | `2` | `Ctrl` + `Alt` + `2` |
| Respuesta a la pregunta recién oída | `3` | `Ctrl` + `Alt` + `3` |
| Vigilar la pantalla (sí/no) | `4` | `Ctrl` + `Alt` + `4` |
| Traducir | `5` | `Ctrl` + `Alt` + `5` |
| Escuchar la llamada (sí/no) | `7` | `Ctrl` + `Alt` + `7` |
| Mostrar / ocultar la barra | `Esc` | `Ctrl` + `Alt` + `P` |
| Clic a través de la barra (sí/no) | - | `Ctrl` + `Alt` + `T` |
| Ajustes | `Ctrl` + `,` | `Ctrl` + `,` |
| Nueva conversación | `Ctrl` + `N` | - |
| Detener la respuesta | `Ctrl` + `.` | - |
| Mostrar todos los atajos | `F1` | - |

**¿Barra oculta?** Pulse `Ctrl` + `Alt` + `P` (o el atajo definido en los ajustes) o inicie Polymath de nuevo (acceso directo del menú Inicio) y la barra vuelve. El icono de la bandeja está desactivado por defecto. El botón `?` de la barra (junto a los ajustes, o `F1`) muestra todos los comandos y atajos.

**Importante:** los comandos cortos solo funcionan con el campo de entrada activo, y no en el modo de clic a través. Los comandos largos (con `Ctrl` + `Alt`) funcionan siempre.

Los atajos se cambian en los ajustes: haz clic en el campo y pulsa la combinación. Si otro programa ya la usa, la barra lo avisa.

Arrastra la barra por su título, su posición se recuerda. El ancho, la opacidad y el tamaño de la letra se pueden ajustar.

### Aspecto y ratón

La sección «Interfaz» de los ajustes:

- **Tema** - oscuro (grafito, por defecto) o claro (marfil);
- **Opacidad de la barra** - toda la barra con su texto (30-100 %);
- **Opacidad del fondo** - solo el fondo de la barra, el texto se mantiene nítido (20-100 %);
- **Clic a través de la barra** - los clics atraviesan la barra de ayuda hasta la ventana de debajo. La barra no se puede mover ni pulsar con el ratón, el teclado y los atajos siguen funcionando. Se activa con `Ctrl` + `Alt` + `T`, y el título de la barra muestra entonces una marca «clic a través». La ventana de ajustes es siempre una normal;
- **Pulsar botones al pasar el cursor** - deja el cursor sobre un botón de la barra (3 segundos por defecto, de 1,5 a 5) y se pulsa solo. Debajo del botón se llena una tira. Funciona también en el modo de clic a través.

Listen captura el sonido de todo el sistema. Usa auriculares: así solo se graba a la otra persona, no tu propia voz.

## Tus propios comandos

Los comandos de dígito están en `%APPDATA%\Polymath\commands.json` (el botón «Abrir commands.json» de los ajustes). El archivo se vuelve a leer en cada llamada, no hace falta reiniciar. Ejemplo:

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Campos: `name`, `instructions` (obligatorios), `model` (`main` o `small`), `screen: true` (adjuntar una captura de pantalla), `watch: true` (vigilar la pantalla), `listen: true` (activar Listen). Marcadores: `{native}` - tu idioma, `{conversation_language}` - el idioma de la conversación.

## Qué tan fiable es el ocultamiento

Las ventanas se crean con `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)`. Es un mecanismo de Windows: la captura de pantalla muestra en su lugar lo que hay debajo de la ventana. Lo respetan Zoom, Teams, Google Meet en el navegador, Discord, OBS, la Herramienta de recortes, PrintScreen y Xbox Game Bar.

Además:

- no hay botón en la barra de tareas ni entrada en Alt+Tab;
- el icono de la bandeja está desactivado por defecto (la bandeja se ve cuando se comparte toda la pantalla);
- no hay ventanas emergentes del sistema: las sugerencias, listas y menús se dibujan dentro de la barra, el menú contextual está desactivado.

Límites:

- El ocultamiento no protege de una cámara apuntada al monitor ni de una captura HDMI por hardware.
- Si compartes una **ventana** de un programa (no toda la pantalla) y la barra queda encima, el otro lado ve lo que hay bajo la barra. Es lo esperado.
- Windows anterior a 10 versión 2004 muestra un rectángulo negro en la captura en lugar de la barra.
- Los enlaces y archivos abiertos (commands.json, la carpeta de datos) se abren en programas normales y se ven al compartir la pantalla.

Comprueba el ocultamiento en tu ordenador:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

El script muestra dos ventanas de prueba protegidas y una normal, captura la pantalla de dos maneras e imprime el resultado. La línea `RESULT: Polymath windows are hidden from screen capture` significa que todo funciona.

## Base de conocimientos

La sección «Base de conocimientos» de los ajustes:

- **Sobre usted** - información general sobre ti. El modelo la usa en cada respuesta.
- **Archivos** - el botón «Añadir archivos», o suelta archivos `.txt` y `.md` sobre la sección. Los archivos se copian a `%APPDATA%\Polymath\knowledge` (el botón «Abrir carpeta»). Puedes editarlos allí, el programa recoge los cambios por sí solo. Un archivo con el mismo nombre se reemplaza, hasta 2 MB, en UTF-8, UTF-16 o Windows-1251.
- **Usar la base de conocimientos en las respuestas** - se activa cuando la base tiene un archivo.
- **Mostrar enseguida una coincidencia de la base, antes de que responda el modelo** - igual.

Cómo funciona. Para una pregunta del chat y para cada frase de la otra persona en Listen, el programa busca primero una respuesta en tus archivos, sin internet y sin el modelo. Una coincidencia aparece al instante como un bloque azul «De la base de conocimientos» sobre la respuesta del modelo, con un botón «Copiar» al lado. Al mismo tiempo el modelo recibe estos datos (toda la base cuando es pequeña, si no las partes que coinciden) y responde basándose en ellos. La búsqueda entiende distintas formas de las palabras. La búsqueda local no encontrará una pregunta en otro idioma, pero el modelo igualmente responde desde la base.

Cualquiera de tres maneras de escribir los archivos:

```markdown
# What salary do you expect?
From 5,000 USD net, open to discussion.

# Why are you leaving your current job?
I want more architecture work.
```

```text
Q: What is your notice period?
A: Two weeks.
```

O simplemente párrafos separados por una línea vacía: la primera línea corta de un párrafo es su tema.

## Historial y exportación

La sección «Historial» de los ajustes:

- **Guardar el historial en el disco**. Desactivado por defecto: el historial vive entonces solo en la memoria hasta que se cierra el programa. Activado: cada pregunta y respuesta se añade a `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl`, cada línea cifrada con Windows DPAPI (solo tu cuenta de Windows puede leerla).
- **Nombre en el historial**. Firma tus preguntas en las exportaciones. Vacío significa el nombre de usuario de Windows.
- **Conservar, días**. Los días más antiguos se eliminan al iniciar. 0 lo conserva todo.
- **Exportar** esta sesión, hoy, 7 días, 30 días o todo el tiempo. «Exportar a .txt» guarda un archivo en `Documents\Polymath`, «Copiar como texto» pone el mismo texto en el portapapeles.
- **Borrar el historial** elimina los archivos del historial y las entradas de esta sesión (pulsa el botón dos veces).

Qué se registra:

- chat: Q - tu pregunta (con el comando y una marca de captura de pantalla), A - la respuesta del modelo;
- Listen: Q - la frase de la otra persona y su traducción, A - la respuesta que se te sugirió y su traducción (cuando hacía falta responder);
- Watch: respuestas a tareas de la pantalla, las ejecuciones vacías no se registran.

El archivo de exportación no está cifrado. El Explorador y el Bloc de notas, abiertos con el botón «Mostrar el archivo», se ven al compartir la pantalla.

## Privacidad

- Las claves de API se guardan cifradas por Windows (DPAPI mediante Electron safeStorage) en `%APPDATA%\Polymath\settings.json`.
- Por defecto el historial está solo en la memoria y desaparece al cerrar el programa. El guardado en disco se activa en los ajustes, los archivos del historial se cifran con DPAPI.
- Los archivos de la base de conocimientos se guardan en `%APPDATA%\Polymath\knowledge` sin cifrar, se buscan en el ordenador. Llegan al modelo solo con una pregunta: toda la base cuando es pequeña, si no las partes que coinciden.
- El sonido y las capturas de pantalla van solo al proveedor elegido (o al de reserva) y solo mientras Listen, Screenshot o Watch están activados. Con whisper.cpp o Parakeet locales el sonido nunca sale del ordenador.
- Registro de errores: `%APPDATA%\Polymath\logs\app.log` (sin texto de las conversaciones).

## Funcionamiento en segundo plano

La casilla «Iniciar al entrar en Windows» inicia Polymath oculto. Llama a la barra con Ctrl+Alt+P. A mano: `Polymath.exe --background`.

## Actualizaciones

El Polymath instalado (desde `Polymath-Setup`) busca una versión nueva unos segundos después de arrancar. Sin su permiso no se descarga nada: la barra muestra «Polymath X está disponible» con los botones «Actualizar» y «Más tarde», y al terminar la descarga «Reiniciar y actualizar». Polymath se cierra, se instala sobre la versión anterior y arranca de nuevo, los ajustes, las claves y el historial se conservan. Si el icono de la bandeja está activado, su menú tiene «Check for updates». Una copia ejecutada desde la carpeta de código fuente y una copia portátil no se actualizan solas.

La descarga se comprueba con el SHA-512 del `latest.yml` de la versión. Una versión sin este hash se rechaza y un archivo que no coincide no se instala. Cada compilación comprueba que `latest.yml` lleva el hash correcto. El instalador aún no está firmado, así que Windows SmartScreen puede seguir avisando.

## Para desarrolladores

Hace falta Node.js 20 o posterior.

```powershell
npm install
```

```powershell
npm start
```

```powershell
npm test
```

```powershell
npm run dist
```

- `npm test` - pruebas unitarias (detector de frases, WAV, análisis de respuestas, SSE, comandos, ajustes, cliente del modelo, historial).
- `npm run dist` - el instalador en `dist`, y después una comprobación de que `latest.yml` lleva el SHA-512 correcto.
- `python scripts/make-installer-art.py` - vuelve a dibujar las imágenes del instalador (`build/`: imagen lateral, cabecera, icono) a partir de `assets/icon.png`. Necesita Python con Pillow.
- `npm run capture-test` - la comprobación de ocultamiento integrada (resultado en JSON).
- La variable `POLYMATH_VISIBLE=1` desactiva el ocultamiento en modo de desarrollo, para hacer capturas de la interfaz. No tiene efecto en el programa compilado.

Estructura:

- `src/main` - el proceso principal: ventanas, atajos, modelo, reconocimiento de voz, Listen, Watch;
- `src/renderer` - la barra y la ventana de ajustes, captura del sonido del sistema;
- `src/shared` - código compartido: detector de frases, WAV, análisis de texto, SSE, traducciones de la interfaz;
- `scripts` - instalación de whisper.cpp y Parakeet y la comprobación del ocultamiento;
- `tests` - pruebas.
