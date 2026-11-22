# Polymath for Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**

Polymath sits next to you and helps when you run short of words or knowledge. It hears what the other person says, sees what is on your screen and suggests what to do next. Nobody else sees it, and it never speaks for you.

### Why you need it

- **Talking to people whose language you don't speak.** Polymath listens to the other person and shows what they said, then suggests what to answer in their language and in your native one (so you always know exactly what you are saying to them). You stay in the conversation yourself instead of hiding behind a translator.
- **Online dating.** Polymath can watch your screen and suggest how to reply in the other person's language and in your native one (so you always know exactly what you are writing to them). You write a message that sounds like you, only better.
- **Flirting.** Get an idea for a reply, a joke or a compliment exactly when you need it.
- **Everyday tasks.** Ask a question, take a screenshot of the screen with the app and get an answer that fits your situation.
- **Hard and confusing things.** Don't know where to click or why something doesn't work? Show Polymath your screen and it points to the mistake and tells you how to fix it.

### What used to be scary is now doable with Polymath

- Go to an online job interview and know what to say.
- Set up ads in Google or Meta without wasting your budget.
- Build your first website and put it on any hosting.
- Understand a rental or loan contract and not miss the small print.
- Fill in a tax return or apply for a visa without mistakes in the documents.
- Write a CV and a cover letter that get noticed, also in a foreign language.
- Negotiate a price or a discount, discuss terms with a landlord, a contractor or a client.
- Understand a letter from a bank, a tax office or an insurer and find out what they really want from you.
- Set up a Wi-Fi router, a printer or a phone when nothing works and a technician is expensive or unavailable.
- Write a convincing complaint to a shop, an airline or a property manager.
- Prepare for a hard conversation with a boss, a partner or parents and find the right words.

Before, you needed a specialist next to you or a call to a friend. Now you have Polymath, who knows every field and is always at hand.

---

A small helper bar for conversations and meetings. It listens to the other person and translates their speech into your language, suggests a reply in the language of the conversation, solves a task from the screen and answers any question in the chat.

**Only you can see the bar.** It does not appear when you share the screen in Zoom, Teams, Meet, Discord or OBS, nor in screenshots and screen recordings.

## Features

- **Listen** (`7` / `Ctrl` + `Alt` + `7`). Listens to the computer's sound (the other person's voice in a call), recognises phrases, shows a translation into your native language and, when you are addressed, a ready reply in the language of the conversation with its translation. Click a reply to copy it. The "Only when a reply is needed" mode shows only the lines you should answer.
- **Screenshot** (`2` / `Ctrl` + `Alt` + `2`). A screenshot goes to the model: solving a task, answering a test question, reviewing code.
- **Watch** (`4` / `Ctrl` + `Alt` + `4`). Watches the screen and answers when a new question or task appears on it. Turns itself off after 10 minutes.
- **Chat**. Ordinary questions. A digit at the start picks a command: `1` Quick (short, fast model), `3` Answer (an answer to the last question heard, with the conversation in mind), `5` Translate.
- The model sees the latest phrases of the conversation, so in the chat you can ask "how do I answer their last question?".
- **Knowledge base**. Your own `.txt` and `.md` files with ready answers to frequent questions. A matching answer is found on the computer, without the internet, and shown at once while the model is still answering.

## Installation

The ready files are in the `dist` folder:

- `Polymath-Setup-<version>.exe` - the installer, it follows the Windows language and supports 22 languages: you can pick the folder, no administrator rights needed, shortcuts on the desktop and in the Start menu, the program starts after installation;

Windows SmartScreen may warn about an unknown publisher (the file is not signed). Click "More info" and "Run anyway".

Requirements: Windows 10 version 2004 (May 2020) or newer, Windows 11. On older systems hiding from screen capture does not work.

## First start

1. Open the settings (the gear on the bar).
2. Pick a model provider, paste the API key and click "Save key". The "Get a key" link opens the provider's page.
3. Click "Test connection". A list of available models appears, clicking a model puts it in the field.
4. Set your native language. In the "Knowledge base" section, describe yourself briefly in "About you" (job, experience). The model uses it in its answers.
5. Click "Save" (or Ctrl+S).

### Providers

| Provider                     | Default model            | Pictures (Screenshot/Watch) | Sound directly |
| ---------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini                | gemini-flash-lite-latest | yes                     | yes            |
| OpenAI                       | gpt-5-mini               | yes                     | no             |
| Anthropic Claude             | claude-sonnet-5-5        | yes                     | no             |
| OpenRouter                   | openrouter/auto          | yes                     | no             |
| Groq                         | openai/gpt-oss-120b      | no                      | no             |
| Mistral                      | mistral-medium-latest    | yes                     | no             |
| Ollama (local)               | llama3.2                 | no                      | no             |
| Custom (OpenAI-compatible)   | any                      | depends on the model    | no             |

Providers rename their models. If a model is not found, click "Test connection" and pick one from the list.

The "Fast model" is used by the Quick and Translate commands. It can stay empty, then the main model is used.

When a model answers 503 (overloaded) or 429 (out of quota), the program asks the other model of the pair at once.

### Reserve model

The "Reserve model" section of the settings: another provider the program asks when both models above answer 503 or 429. For example, Anthropic Claude (`claude-haiku-5-5` by default, a fast one). The reserve key is stored separately. Without it, the key of the same provider from the "Model" section is used. The reserve is skipped when it cannot read what is sent: a screen picture (Screenshot/Watch) or sound.

## Speech recognition (for Listen)

The "Speech recognition" settings offer four engines:

1. **Via the model** (default). The phrase goes straight to the chat model. Works with Google Gemini, with the same key.
2. **Cloud Whisper API**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, fast and cheap) or your own OpenAI-compatible server. The recognition key is stored apart from the model key.
3. **Local (whisper.cpp)**. The sound never leaves the computer. Installed with one command:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

In the installed program the script is in `<program folder>\resources\scripts`. Options: `-Model tiny|base|small|medium|large-v3-turbo` (small by default, 466 MB) and `-Cuda` for NVIDIA graphics cards. The files go to `%APPDATA%\Polymath\whisper`. Then pick "Local" and click "Test recognition".

4. **Local (NVIDIA Parakeet)**. Also on this computer, faster than whisper.cpp on a processor and usually more accurate. The model `parakeet-tdt-0.6b-v3` knows 25 European languages (English, Russian, Ukrainian, German, French, Spanish and others), but not Turkish or Chinese. Runs through [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx). The "Download Parakeet" button in the settings puts it in place, or one command:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

About 520 MB in all. The option `-Model v2` takes the English-only model, a little more accurate in English. The files go to `%APPDATA%\Polymath\parakeet`. Then pick "Local (NVIDIA Parakeet)" and click "Test recognition". The first phrase after a pause waits 7-10 s while the model loads, the next ones take under a second. After 10 minutes without speech the server stops and frees the memory. Both downloads (the program and the model) are checked against the SHA-256 published by GitHub, a file that does not match is discarded and nothing is installed. Without a published hash there is no install.

On the first start on a new computer the bar asks once how to recognize speech: through Gemini (nothing to download) or with Parakeet on this computer (the app downloads about 520 MB, with progress and a cancel button). The answer can be changed later in the settings.

The "Test recognition" button works for all four engines.

## How to use

| Action                        | Shortcut                     |
| ----------------------------- | ---------------------------- |
| Show / hide the bar           | `Ctrl` + `Alt` + `P`         |
| Quick answer (short, fast model) | `Ctrl` + `Alt` + `1` |
| Solve a task from the screen  | `Ctrl` + `Alt` + `2`         |
| Answer to the question just heard | `Ctrl` + `Alt` + `3` |
| Watch the screen (on/off)     | `Ctrl` + `Alt` + `4`         |
| Translate | `Ctrl` + `Alt` + `5` |
| Listen to the call (on/off)   | `Ctrl` + `Alt` + `7`         |
| Click through the bar (on/off)| `Ctrl` + `Alt` + `T`         |
| Send                          | `Enter`                      |
| New line                      | `Shift` + `Enter`            |
| Stop the answer               | `Ctrl` + `.` or the `■` button |
| New conversation              | `Ctrl` + `N` or the `+` button |
| Previous request              | `↑` / `↓` in an empty field  |
| Hide the bar                  | `Esc`                        |

### Short and long commands

Short commands work inside the bar, long ones (with `Ctrl` + `Alt`) work from any window. A digit typed into an empty field picks a command, `1 your text` works too.

| Action | Short (in the bar) | Long (from any window) |
| --- | --- | --- |
| Quick answer (short, fast model) | `1` | `Ctrl` + `Alt` + `1` |
| Solve a task from the screen | `2` | `Ctrl` + `Alt` + `2` |
| Answer to the question just heard | `3` | `Ctrl` + `Alt` + `3` |
| Watch the screen (on/off) | `4` | `Ctrl` + `Alt` + `4` |
| Translate | `5` | `Ctrl` + `Alt` + `5` |
| Listen to the call (on/off) | `7` | `Ctrl` + `Alt` + `7` |
| Show / hide the bar | `Esc` | `Ctrl` + `Alt` + `P` |
| Click through the bar (on/off) | - | `Ctrl` + `Alt` + `T` |
| Settings | `Ctrl` + `,` | `Ctrl` + `,` |
| New conversation | `Ctrl` + `N` | - |
| Stop the answer | `Ctrl` + `.` | - |
| Show all hotkeys | `F1` | - |

**Bar hidden?** Press `Ctrl` + `Alt` + `P` (or the shortcut set in the settings) or start Polymath again (the Start menu shortcut), the bar comes back. The tray icon is off by default. The `?` button in the bar (next to the settings, or `F1`) shows all commands and hotkeys.

**Note:** short commands work only while the input field is active, and not in click-through mode. Long commands (with `Ctrl` + `Alt`) work always.

Hotkeys are changed in the settings: click the field and press the shortcut. If another program already uses it, the bar says so.

Drag the bar by its title, its place is remembered. Width, opacity and font size are adjustable.

### Look and mouse

The "Interface" section of the settings:

- **Theme** - dark (graphite, default) or light (ivory);
- **Bar opacity** - the whole bar with its text (30-100%);
- **Background opacity** - only the bar's background, the text stays sharp (20-100%);
- **Click through the bar** - clicks pass through the helper bar to the window below. The bar cannot be moved or clicked with the mouse, the keyboard and hotkeys still work. Toggled with `Ctrl` + `Alt` + `T`, the bar's title then shows a "click-through" mark. The settings window is always a normal one;
- **Press buttons by hovering** - rest the cursor on a bar button (3 seconds by default, 1.5-5 possible) and it presses itself. A strip fills under the button. Works in click-through mode too.

Listen captures the sound of the whole system. Use headphones: then only the other person gets recorded, not your own voice.

## Your own commands

The digit commands live in `%APPDATA%\Polymath\commands.json` (the "Open commands.json" button in the settings). The file is read again on every call, no restart needed. Example:

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Fields: `name`, `instructions` (required), `model` (`main` or `small`), `screen: true` (attach a screenshot), `watch: true` (watch the screen), `listen: true` (turn Listen on). Placeholders: `{native}` - your language, `{conversation_language}` - the language of the conversation.

## How reliable the hiding is

The windows are created with `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)`. This is a Windows mechanism: a screen capture shows what is under the window instead. Zoom, Teams, Google Meet in a browser, Discord, OBS, Snipping Tool, PrintScreen and Xbox Game Bar respect it.

Also:

- no taskbar button and no Alt+Tab entry;
- the tray icon is off by default (the tray is visible when the whole screen is shared);
- no system pop-ups: tooltips, lists and menus are drawn inside the bar, the context menu is off.

Limits:

- Hiding does not protect from a camera pointed at the monitor or from hardware HDMI capture.
- If you share a **window** of a program (not the whole screen) and the bar lies on top of it, the other side sees what is under the bar. That is expected.
- Windows older than 10 version 2004 shows a black rectangle in the capture instead of the bar.
- Opened links and files (commands.json, the data folder) open in ordinary programs and are visible when the screen is shared.

Check the hiding on your computer:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

The script shows two protected test windows and one normal one, captures the screen in two ways and prints the result. The line `RESULT: Polymath windows are hidden from screen capture` means everything works.

## Knowledge base

The "Knowledge base" section of the settings:

- **About you** - general information about you. The model uses it in every answer.
- **Files** - the "Add files" button, or drop `.txt` and `.md` files on the section. The files are copied to `%APPDATA%\Polymath\knowledge` (the "Open folder" button). You can edit them there, the program picks up the changes itself. A file with the same name is replaced, up to 2 MB, in UTF-8, UTF-16 or Windows-1251.
- **Use the knowledge base in answers** - turns on once the base has a file.
- **Show a match from the base at once, before the model answers** - the same.

How it works. For a chat question and for every phrase of the other person in Listen, the program first looks for an answer in your files, without the internet and without the model. A match appears at once as a blue "From the knowledge base" block above the model's answer, with a "Copy" button next to it. At the same time the model gets this data (the whole base when it is small, otherwise the matching parts) and answers based on it. The search understands different word forms. The local search will not find a question in another language, but the model still answers from the base.

Any of three ways to write the files:

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

Or just paragraphs split by an empty line: the short first line of a paragraph is its topic.

## History and export

The "History" section of the settings:

- **Save the history to disk**. Off by default: the history then lives only in memory until the program closes. On: every question and answer is appended to `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl`, each line encrypted with Windows DPAPI (only your Windows account can read it).
- **Name in the history**. Signs your questions in exports. Empty means the Windows user name.
- **Keep, days**. Older days are deleted at start. 0 keeps everything.
- **Export** this session, today, 7 days, 30 days or all time. "Export to .txt" saves a file to `Documents\Polymath`, "Copy as text" puts the same text on the clipboard.
- **Clear the history** deletes the history files and this session's entries (press the button twice).

What is recorded:

- chat: Q - your question (with the command and a screenshot mark), A - the model's answer;
- Listen: Q - the other person's phrase and its translation, A - the reply suggested to you and its translation (when a reply was needed);
- Watch: answers to tasks from the screen, empty runs are not recorded.

The export file is not encrypted. Explorer and Notepad, opened with the "Show the file" button, are visible when the screen is shared.

## Privacy

- API keys are stored encrypted by Windows (DPAPI via Electron safeStorage) in `%APPDATA%\Polymath\settings.json`.
- By default the history is only in memory and is gone when the program closes. Saving to disk is turned on in the settings, the history files are encrypted with DPAPI.
- Knowledge base files are stored in `%APPDATA%\Polymath\knowledge` without encryption, they are searched on the computer. They go to the model only with a question: the whole base when it is small, otherwise the matching parts.
- Sound and screenshots go only to the chosen provider (or the reserve one) and only while Listen, Screenshot or Watch is on. With local whisper.cpp or Parakeet the sound never leaves the computer.
- Error log: `%APPDATA%\Polymath\logs\app.log` (no conversation text).

## Running in the background

The "Start at Windows sign-in" box starts Polymath hidden. Call the bar with Ctrl+Alt+P. By hand: `Polymath.exe --background`.

## Updates

The installed Polymath (from `Polymath-Setup`) looks for a new version a few seconds after start. Nothing is downloaded without you: the bar shows "Polymath X is available" with the buttons "Update" and "Later", then "Restart and update" once the download is done. Polymath closes, installs over the old one and starts again, settings, keys and history stay. If the tray icon is on, its menu has "Check for updates". A copy run from the source folder or a portable copy does not update itself.

The download is checked against the SHA-512 in the `latest.yml` of the release. A release without this hash is refused, a file that does not match is not installed. Every build checks that `latest.yml` carries the right hash. The installer is not code-signed yet, so Windows SmartScreen may still warn.

## For developers

Node.js 20 or newer is needed.

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

- `npm test` - unit tests (phrase detector, WAV, answer parsing, SSE, commands, settings, model client, history).
- `npm run dist` - the installer in `dist`, then a check that `latest.yml` carries the right SHA-512.
- `python scripts/make-installer-art.py` - redraws the installer artwork (`build/`: sidebar picture, header, icon) from `assets/icon.png`. Needs Python with Pillow.
- `npm run capture-test` - the built-in hiding check (result in JSON).
- The `POLYMATH_VISIBLE=1` variable turns hiding off in development mode, to take screenshots of the interface. It has no effect in the built program.

Layout:

- `src/main` - the main process: windows, hotkeys, model, speech recognition, Listen, Watch;
- `src/renderer` - the bar and the settings window, system sound capture;
- `src/shared` - shared code: phrase detector, WAV, text parsing, SSE, interface translations;
- `scripts` - whisper.cpp and Parakeet installation and the hiding check;
- `tests` - tests.
