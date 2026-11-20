# Polymath for Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

A small helper bar for conversations and meetings. It listens to the other person and translates their speech into your language, suggests a reply in the language of the conversation, solves a task from the screen and answers any question in the chat.

**Only you can see the bar.** It does not appear when you share the screen in Zoom, Teams, Meet, Discord or OBS, nor in screenshots and screen recordings.

## Features

- **Listen**. Listens to the computer's sound (the other person's voice in a call), recognises phrases, shows a translation into your native language and, when you are addressed, a ready reply in the language of the conversation with its translation. Click a reply to copy it. The "Only when a reply is needed" mode shows only the lines you should answer.
- **Screen**. A screenshot goes to the model: solving a task, answering a test question, reviewing code.
- **Watch**. Watches the screen and answers when a new question or task appears on it. Turns itself off after 10 minutes.
- **Chat**. Ordinary questions. A digit at the start picks a command: `1` Quick (short, fast model), `3` Answer (an answer to the last question heard, with the conversation in mind), `5` Translate.
- The model sees the latest phrases of the conversation, so in the chat you can ask "how do I answer their last question?".
- **Knowledge base**. Your own `.txt` and `.md` files with ready answers to frequent questions. A matching answer is found on the computer, without the internet, and shown at once while the model is still answering.
- **Your own commands**. Add your own digit commands with your own instructions, model and screen or sound settings.
- **History and export**. Optional saving of conversations, encrypted, with export to a text file.

## Installation

Two ready files are published in each release:

- `Polymath-Setup-<version>.exe` - the installer. It follows the Windows language, and 22 languages are supported. You can pick the folder, no administrator rights are needed, shortcuts go to the desktop and the Start menu, and the program starts after installation.

Windows SmartScreen may warn about an unknown publisher, because the file is not signed yet. Click "More info" and then "Run anyway".

Requirements: Windows 10 version 2004 (May 2020) or newer, or Windows 11. On older systems hiding from screen capture does not work.

Updates: an installed copy checks this page for new versions a few seconds after start. When a newer version appears, the program shows a card and downloads the update only after you agree. The update is installed into the same folder and the program starts again.

## First start

1. Open the settings (the gear on the bar).
2. Pick a model provider, paste the API key and click "Save key". The "Get a key" link opens the provider's page.
3. Click "Test connection". A list of available models appears. Clicking a model puts it in the field.
4. Set your native language. In the "Knowledge base" section, describe yourself briefly in "About you" (job, experience). The model uses it in its answers.
5. Click "Save" (or press Ctrl+S).

### Providers

| Provider                   | Default model            | Pictures (Screen/Watch) | Sound directly |
| -------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini              | gemini-flash-lite-latest | yes                     | yes            |
| OpenAI                     | gpt-5-mini               | yes                     | no             |
| Anthropic Claude           | claude-sonnet-5-5        | yes                     | no             |
| OpenRouter                 | openrouter/auto          | yes                     | no             |
| Groq                       | openai/gpt-oss-120b      | no                      | no             |
| Mistral                    | mistral-medium-latest    | yes                     | no             |
| Ollama (local)             | llama3.2                 | no                      | no             |
| Custom (OpenAI-compatible) | any                      | depends on the model    | no             |

Providers rename their models. If a model is not found, click "Test connection" and pick one from the list.

The "Fast model" is used by the Quick and Translate commands. It can stay empty, and then the main model is used.

When a model answers 503 (overloaded) or 429 (out of quota), the program asks the other model of the pair at once.

### Reserve model

The "Reserve model" section of the settings sets another provider that the program asks when both models above answer 503 or 429. For example, Anthropic Claude (`claude-haiku-5-5` by default, a fast one). The reserve key is stored separately. Without it, the key of the same provider from the "Model" section is used. The reserve is skipped when it cannot read what is sent, such as a screen picture (Screen/Watch) or sound.

## Speech recognition (for Listen)

The "Speech recognition" settings offer four engines:

1. **Via the model** (default). The phrase goes straight to the chat model. Works with Google Gemini, with the same key.
2. **Cloud Whisper API**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, fast and cheap), or your own OpenAI-compatible server. The recognition key is stored apart from the model key.
3. **Local (whisper.cpp)**. The sound never leaves the computer. Installed by one command, and the files go to `%APPDATA%\Polymath\whisper`. Then pick "Local" and click "Test recognition". The small model is used by default (466 MB). Other sizes and NVIDIA graphics acceleration are available as options of the installation script.
4. **Local (NVIDIA Parakeet)**. Also on this computer, faster than whisper.cpp on a processor and usually more accurate. The model knows 25 European languages (English, Russian, Ukrainian, German, French, Spanish and others), but not Turkish or Chinese. The "Download Parakeet" button in the settings puts it in place. The download is about 520 MB in all. Then pick "Local (NVIDIA Parakeet)" and click "Test recognition". The first phrase after a pause waits 7-10 seconds while the model loads, and the next ones take under a second. After 10 minutes without speech the server stops and frees the memory.

On the first start on a new computer the bar asks once how to recognise speech: through Gemini (nothing to download) or with Parakeet on this computer (the app downloads about 520 MB, with progress and a cancel button). The answer can be changed later in the settings.

The "Test recognition" button works for all four engines.

## How to use

| Action                         | Shortcut                       |
| ------------------------------ | ------------------------------ |
| Show / hide the bar            | `Ctrl` + `Alt` + `P`           |
| Solve a task from the screen   | `Ctrl` + `Alt` + `2`           |
| Watch the screen (on/off)      | `Ctrl` + `Alt` + `4`           |
| Listen to the call (on/off)    | `Ctrl` + `Alt` + `7`           |
| Click through the bar (on/off) | `Ctrl` + `Alt` + `T`           |
| Send                           | `Enter`                        |
| New line                       | `Shift` + `Enter`              |
| Stop the answer                | `Ctrl` + `.` or the `■` button |
| New conversation               | `Ctrl` + `N` or the `+` button |
| Previous request               | `↑` / `↓` in an empty field    |
| Hide the bar                   | `Esc`                          |

Hotkeys are changed in the settings: click the field and press the shortcut. If another program already uses it, the bar says so.

Drag the bar by its title. Its place is remembered. Width, opacity and font size are adjustable.

### Look and mouse

The "Interface" section of the settings:

- **Theme**: dark (graphite, default) or light (ivory).
- **Bar opacity**: the whole bar with its text (30-100%).
- **Background opacity**: only the bar's background, the text stays sharp (20-100%).
- **Click through the bar**: clicks pass through the helper bar to the window below. The bar cannot be moved or clicked with the mouse, but the keyboard and hotkeys still work. Toggled with `Ctrl` + `Alt` + `T`, and the bar's title then shows a "click-through" mark. The settings window is always a normal one.
- **Press buttons by hovering**: rest the cursor on a bar button (3 seconds by default, 1.5-5 possible) and it presses itself. A strip fills under the button. Works in click-through mode too.

Listen captures the sound of the whole system. Use headphones, so that only the other person is recorded and not your own voice.

## Your own commands

The digit commands live in `%APPDATA%\Polymath\commands.json` (the "Open commands.json" button in the settings). The file is read again on every call, so no restart is needed. Example:

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Fields: `name`, `instructions` (required), `model` (`main` or `small`), `screen: true` (attach a screenshot), `watch: true` (watch the screen), `listen: true` (turn Listen on). Placeholders: `{native}` is your language, and `{conversation_language}` is the language of the conversation.

## Hiding from screen sharing

The windows are created with the Windows mechanism that excludes them from capture (`WDA_EXCLUDEFROMCAPTURE`). A screen capture shows what is under the window instead. Zoom, Teams, Google Meet in a browser, Discord, OBS, Snipping Tool, PrintScreen and Xbox Game Bar respect it.

Also:

- no taskbar button and no Alt+Tab entry;
- the tray icon is off by default (the tray is visible when the whole screen is shared);
- no system pop-ups: tooltips, lists and menus are drawn inside the bar, and the context menu is off.

Limits:

- Hiding does not protect from a camera pointed at the monitor or from hardware HDMI capture.
- If you share a **window** of a program (not the whole screen) and the bar lies on top of it, the other side sees what is under the bar. This is expected.
- Windows older than 10 version 2004 shows a black rectangle in the capture instead of the bar.
- Opened links and files (commands.json, the data folder) open in ordinary programs and are visible when the screen is shared.

## Knowledge base

The "Knowledge base" section of the settings:

- **About you**: general information about you. The model uses it in every answer.
- **Files**: the "Add files" button, or drop `.txt` and `.md` files on the section. The files are copied to `%APPDATA%\Polymath\knowledge` (the "Open folder" button). You can edit them there, and the program picks up the changes itself. A file with the same name is replaced. The limit is 2 MB per file, in UTF-8, UTF-16 or Windows-1251.
- **Use the knowledge base in answers**: turns on once the base has a file.
- **Show a match from the base at once, before the model answers**: the same.

How it works. For a chat question and for every phrase of the other person in Listen, the program first looks for an answer in your files, without the internet and without the model. A match appears at once as a blue "From the knowledge base" block above the model's answer, with a "Copy" button next to it. At the same time the model gets this data (the whole base when it is small, otherwise the matching parts) and answers based on it. The search understands different word forms. The local search does not find a question written in another language, but the model still answers from the base.

Three ways to write the files:

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

Or simply paragraphs separated by an empty line. The short first line of a paragraph is its topic.

## History and export

The "History" section of the settings:

- **Save the history to disk**. Off by default: the history then lives only in memory until the program closes. When on, every question and answer is appended to a daily file in `%APPDATA%\Polymath\history`, and each line is encrypted with Windows DPAPI, so only your Windows account can read it.
- **Name in the history**. Signs your questions in exports. Empty means the Windows user name.
- **Keep, days**. Older days are deleted at start. 0 keeps everything.
- **Export** this session, today, 7 days, 30 days or all time. "Export to .txt" saves a file to `Documents\Polymath`, and "Copy as text" puts the same text on the clipboard.
- **Clear the history** deletes the history files and this session's entries (press the button twice).

What is recorded:

- chat: the question (with the command and a screenshot mark) and the model's answer;
- Listen: the other person's phrase and its translation, and the suggested reply and its translation when a reply was needed;
- Watch: answers to tasks from the screen. Empty runs are not recorded.

The export file is not encrypted. Explorer and Notepad, opened with the "Show the file" button, are visible when the screen is shared.

## Privacy

- API keys are stored encrypted by Windows (DPAPI) in `%APPDATA%\Polymath\settings.json`.
- By default the history is only in memory and is gone when the program closes. Saving to disk is turned on in the settings, and the history files are encrypted with DPAPI.
- Knowledge base files are stored without encryption in `%APPDATA%\Polymath\knowledge` and are searched on the computer. They go to the model only together with a question: the whole base when it is small, otherwise the matching parts.
- Sound and screenshots go only to the chosen provider (or the reserve one), and only while Listen, Screen or Watch is on. With local whisper.cpp or Parakeet the sound never leaves the computer.
- The error log is `%APPDATA%\Polymath\logs\app.log`. It contains no conversation text.

## Running in the background

The "Start at Windows sign-in" box starts Polymath hidden. Call the bar with `Ctrl` + `Alt` + `P`.

## Requirements and limits

- Windows 10 version 2004 or newer, or Windows 11.
- Internet access for the cloud models. Local speech recognition works offline after installation.
- A key from at least one model provider. The keys are your own and are billed by the provider.
