# Polymath für Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**
(Ihr stiller KI-Partner in jedem Gespräch)

Polymath sitzt neben Ihnen und hilft, wenn Ihnen die Worte oder das Wissen fehlen. Er hört, was Ihr Gegenüber sagt, sieht, was auf Ihrem Bildschirm ist, und schlägt vor, was Sie als Nächstes tun können. Niemand sonst sieht ihn, und er spricht nie für Sie.

### Wozu er gut ist

- **Gespräche mit Menschen, deren Sprache Sie nicht sprechen.** Polymath hört Ihrem Gegenüber zu und zeigt, was gesagt wurde. Dann schlägt er vor, was Sie antworten können, in der Sprache Ihres Gegenübers und in Ihrer Muttersprache (damit Sie immer verstehen, was genau Sie Ihrem Gegenüber sagen). Sie bleiben selbst im Gespräch, statt sich hinter einem Übersetzer zu verstecken.
- **Online-Dating.** Polymath kann Ihren Bildschirm beobachten und vorschlagen, wie Sie in der Sprache Ihres Gegenübers und in Ihrer Muttersprache antworten (damit Sie immer verstehen, was genau Sie schreiben). Sie schreiben eine Nachricht, die nach Ihnen klingt, nur besser.
- **Flirten.** Bekommen Sie eine Idee für eine Antwort, einen Witz oder ein Kompliment genau dann, wenn Sie es brauchen.
- **Alltägliche Aufgaben.** Stellen Sie eine Frage, machen Sie mit der App einen Screenshot und erhalten Sie eine Antwort, die genau zu Ihrer Situation passt.
- **Schwierige und unverständliche Dinge.** Sie wissen nicht, wo Sie klicken sollen oder warum etwas nicht funktioniert? Zeigen Sie Polymath Ihren Bildschirm, und er zeigt auf den Fehler und sagt, wie Sie ihn beheben.

### Was früher Angst machte, schaffen Sie jetzt mit Polymath

- Zu einem Online-Vorstellungsgespräch gehen und wissen, was man sagt.
- Werbung bei Google oder Meta einrichten, ohne das Budget zu verbrennen.
- Die erste eigene Website bauen und bei einem beliebigen Hoster veröffentlichen.
- Einen Miet- oder Kreditvertrag verstehen und das Kleingedruckte nicht übersehen.
- Die Steuererklärung ausfüllen oder ein Visum beantragen, ohne Fehler in den Unterlagen.
- Einen Lebenslauf und ein Anschreiben schreiben, die auffallen, auch in einer Fremdsprache.
- Über Preis oder Rabatt verhandeln und Bedingungen mit Vermieter, Handwerker oder Kunden besprechen.
- Den Brief von Bank, Finanzamt oder Versicherung verstehen und erfahren, was man wirklich von Ihnen will.
- Einen WLAN-Router, einen Drucker oder ein Handy einrichten, wenn nichts funktioniert und der Techniker teuer oder nicht erreichbar ist.
- Eine überzeugende Beschwerde an ein Geschäft, eine Fluggesellschaft oder eine Hausverwaltung schreiben.
- Sich auf ein schwieriges Gespräch mit Chef, Partner oder Eltern vorbereiten und die richtigen Worte finden.

Früher brauchte man dafür einen Fachmann an der Seite oder einen Anruf bei einem Freund. Jetzt haben Sie Polymath, der sich in allen Bereichen auskennt und immer zur Hand ist.

---

Eine kleine Hilfsleiste für Gespräche und Besprechungen. Sie hört dem Gegenüber zu und übersetzt seine Sprache in Ihre, schlägt eine Antwort in der Sprache des Gesprächs vor, löst eine Aufgabe vom Bildschirm und beantwortet jede Frage im Chat.

**Nur Sie sehen die Leiste.** Sie erscheint nicht, wenn Sie den Bildschirm in Zoom, Teams, Meet, Discord oder OBS teilen, und auch nicht auf Screenshots und in Bildschirmaufnahmen.

## Funktionen

- **Listen** (`7` / `Strg` + `Alt` + `7`). Hört den Ton des Computers (die Stimme des Gegenübers im Anruf), erkennt Sätze, zeigt eine Übersetzung in Ihre Muttersprache und, wenn man Sie anspricht, eine fertige Antwort in der Sprache des Gesprächs mit Übersetzung. Ein Klick auf eine Antwort kopiert sie. Der Modus „Nur wenn eine Antwort nötig ist“ zeigt nur die Zeilen, auf die Sie antworten sollten.
- **Screenshot** (`2` / `Strg` + `Alt` + `2`). Ein Screenshot geht an das Modell: eine Aufgabe lösen, eine Testfrage beantworten, Code prüfen.
- **Watch** (`4` / `Strg` + `Alt` + `4`). Beobachtet den Bildschirm und antwortet, wenn dort eine neue Frage oder Aufgabe erscheint. Schaltet sich nach 10 Minuten selbst aus.
- **Chat**. Gewöhnliche Fragen. Eine Ziffer am Anfang wählt einen Befehl: `1` Quick (kurz, schnelles Modell), `3` Answer (eine Antwort auf die zuletzt gehörte Frage, mit Blick auf das Gespräch), `5` Translate.
- Das Modell sieht die letzten Sätze des Gesprächs, deshalb können Sie im Chat fragen: „Wie antworte ich auf ihre letzte Frage?“.
- **Wissensbasis**. Ihre eigenen `.txt`- und `.md`-Dateien mit fertigen Antworten auf häufige Fragen. Eine passende Antwort wird auf dem Computer gefunden, ohne Internet, und sofort angezeigt, während das Modell noch antwortet.

## Installation

Die fertigen Dateien liegen im Ordner `dist`:

- `Polymath-Setup-<Version>.exe` - das Installationsprogramm, es richtet sich nach der Windows-Sprache und unterstützt 22 Sprachen: Sie können den Ordner wählen, Administratorrechte sind nicht nötig, Verknüpfungen auf dem Desktop und im Startmenü, das Programm startet nach der Installation;

Windows SmartScreen kann vor einem unbekannten Herausgeber warnen (die Datei ist nicht signiert). Klicken Sie auf „Weitere Informationen“ und „Trotzdem ausführen“.

Voraussetzungen: Windows 10 Version 2004 (Mai 2020) oder neuer, Windows 11. Auf älteren Systemen funktioniert das Verstecken vor der Bildschirmaufnahme nicht.

## Erster Start

1. Öffnen Sie die Einstellungen (das Zahnrad auf der Leiste).
2. Wählen Sie einen Modellanbieter, fügen Sie den API-Schlüssel ein und klicken Sie auf „Schlüssel speichern“. Der Link „Schlüssel holen“ öffnet die Seite des Anbieters.
3. Klicken Sie auf „Verbindung testen“. Eine Liste der verfügbaren Modelle erscheint, ein Klick auf ein Modell setzt es in das Feld.
4. Legen Sie Ihre Muttersprache fest. Beschreiben Sie sich im Bereich „Wissensbasis“ kurz im Feld „Über Sie“ (Beruf, Erfahrung). Das Modell nutzt es in seinen Antworten.
5. Klicken Sie auf „Speichern“ (oder Strg+S).

### Anbieter

| Anbieter                     | Standardmodell           | Bilder (Screenshot/Watch)   | Ton direkt     |
| ---------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini                | gemini-flash-lite-latest | ja                      | ja             |
| OpenAI                       | gpt-5-mini               | ja                      | nein           |
| Anthropic Claude             | claude-sonnet-5-5        | ja                      | nein           |
| OpenRouter                   | openrouter/auto          | ja                      | nein           |
| Groq                         | openai/gpt-oss-120b      | nein                    | nein           |
| Mistral                      | mistral-medium-latest    | ja                      | nein           |
| Ollama (lokal)               | llama3.2                 | nein                    | nein           |
| Eigener (OpenAI-kompatibel)  | beliebig                 | je nach Modell          | nein           |

Anbieter benennen ihre Modelle um. Wenn ein Modell nicht gefunden wird, klicken Sie auf „Verbindung testen“ und wählen Sie eines aus der Liste.

Das „Schnelle Modell“ wird von den Befehlen Quick und Translate verwendet. Es kann leer bleiben, dann wird das Hauptmodell benutzt.

Wenn ein Modell 503 (überlastet) oder 429 (Kontingent aufgebraucht) antwortet, fragt das Programm sofort das andere Modell des Paares.

### Reservemodell

Der Bereich „Reservemodell“ in den Einstellungen: ein anderer Anbieter, den das Programm fragt, wenn beide Modelle oben 503 oder 429 antworten. Zum Beispiel Anthropic Claude (standardmäßig `claude-haiku-5-5`, ein schnelles). Der Schlüssel des Reservemodells wird getrennt gespeichert. Ohne ihn wird der Schlüssel desselben Anbieters aus dem Bereich „Modell“ benutzt. Das Reservemodell wird übersprungen, wenn es nicht lesen kann, was gesendet wird: ein Bildschirmbild (Screenshot/Watch) oder Ton.

## Spracherkennung (für Listen)

Die Einstellungen „Spracherkennung“ bieten vier Engines:

1. **Über das Modell** (Standard). Der Satz geht direkt an das Chat-Modell. Funktioniert mit Google Gemini, mit demselben Schlüssel.
2. **Cloud-Whisper-API**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, schnell und günstig) oder Ihr eigener OpenAI-kompatibler Server. Der Erkennungsschlüssel wird getrennt vom Modellschlüssel gespeichert.
3. **Lokal (whisper.cpp)**. Der Ton verlässt den Computer nie. Wird mit einem Befehl installiert:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

Im installierten Programm liegt das Skript in `<Programmordner>\resources\scripts`. Optionen: `-Model tiny|base|small|medium|large-v3-turbo` (standardmäßig small, 466 MB) und `-Cuda` für NVIDIA-Grafikkarten. Die Dateien landen in `%APPDATA%\Polymath\whisper`. Wählen Sie dann „Lokal“ und klicken Sie auf „Erkennung testen“.

4. **Lokal (NVIDIA Parakeet)**. Ebenfalls auf diesem Computer, auf einem Prozessor schneller als whisper.cpp und meist genauer. Das Modell `parakeet-tdt-0.6b-v3` kennt 25 europäische Sprachen (Englisch, Russisch, Ukrainisch, Deutsch, Französisch, Spanisch und andere), aber weder Türkisch noch Chinesisch. Läuft über [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx). Die Schaltfläche „Parakeet herunterladen“ in den Einstellungen legt alles an Ort und Stelle, oder ein Befehl:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

Insgesamt etwa 520 MB. Die Option `-Model v2` nimmt das Modell nur für Englisch, auf Englisch etwas genauer. Die Dateien landen in `%APPDATA%\Polymath\parakeet`. Wählen Sie dann „Lokal (NVIDIA Parakeet)“ und klicken Sie auf „Erkennung testen“. Der erste Satz nach einer Pause wartet 7-10 s, während das Modell lädt, die nächsten dauern unter einer Sekunde. Nach 10 Minuten ohne Sprache stoppt der Server und gibt den Speicher frei. Beide Downloads (Programm und Modell) werden anhand des von GitHub veröffentlichten SHA-256 geprüft. Eine Datei, die nicht passt, wird verworfen und nichts wird installiert. Ohne veröffentlichten Hash gibt es keine Installation.

Beim ersten Start auf einem neuen Computer fragt die Leiste einmal, wie die Sprache erkannt werden soll: über Gemini (nichts herunterzuladen) oder mit Parakeet auf diesem Computer (die App lädt etwa 520 MB herunter, mit Fortschrittsanzeige und Abbrechen-Schaltfläche). Die Antwort lässt sich später in den Einstellungen ändern.

Die Schaltfläche „Erkennung testen“ funktioniert für alle vier Engines.

## Bedienung

| Aktion                          | Tastenkürzel                   |
| ------------------------------- | ------------------------------ |
| Leiste zeigen / verbergen       | `Strg` + `Alt` + `P`           |
| Schnelle Antwort (kurz, schnelles Modell) | `Strg` + `Alt` + `1` |
| Aufgabe vom Bildschirm lösen    | `Strg` + `Alt` + `2`           |
| Antwort auf die gerade gehörte Frage | `Strg` + `Alt` + `3` |
| Bildschirm beobachten (an/aus)  | `Strg` + `Alt` + `4`           |
| Übersetzen | `Strg` + `Alt` + `5` |
| Anruf mithören (an/aus)         | `Strg` + `Alt` + `7`           |
| Durch die Leiste klicken (an/aus) | `Strg` + `Alt` + `T`         |
| Senden                          | `Enter`                        |
| Neue Zeile                      | `Umschalt` + `Enter`           |
| Antwort stoppen                 | `Strg` + `.` oder die Taste `■` |
| Neues Gespräch                  | `Strg` + `N` oder die Taste `+` |
| Vorherige Anfrage               | `↑` / `↓` im leeren Feld       |
| Leiste verbergen                | `Esc`                          |

### Kurze und lange Befehle

Kurze Befehle funktionieren in der Leiste, lange (mit `Strg` + `Alt`) aus jedem Fenster. Eine Ziffer im leeren Feld wählt einen Befehl, auch `1 Ihr Text` funktioniert.

| Aktion | Kurz (in der Leiste) | Lang (aus jedem Fenster) |
| --- | --- | --- |
| Schnelle Antwort (kurz, schnelles Modell) | `1` | `Strg` + `Alt` + `1` |
| Aufgabe vom Bildschirm lösen | `2` | `Strg` + `Alt` + `2` |
| Antwort auf die gerade gehörte Frage | `3` | `Strg` + `Alt` + `3` |
| Bildschirm beobachten (an/aus) | `4` | `Strg` + `Alt` + `4` |
| Übersetzen | `5` | `Strg` + `Alt` + `5` |
| Anruf mithören (an/aus) | `7` | `Strg` + `Alt` + `7` |
| Leiste ein- / ausblenden | `Esc` | `Strg` + `Alt` + `P` |
| Durch die Leiste klicken (an/aus) | - | `Strg` + `Alt` + `T` |
| Einstellungen | `Strg` + `,` | `Strg` + `,` |
| Neues Gespräch | `Strg` + `N` | - |
| Antwort stoppen | `Strg` + `.` | - |
| Alle Tastenkürzel anzeigen | `F1` | - |

**Leiste ausgeblendet?** Drücken Sie `Strg` + `Alt` + `P` (oder das in den Einstellungen gewählte Kürzel) oder starten Sie Polymath erneut (Verknüpfung im Startmenü), dann kommt die Leiste zurück. Das Symbol im Infobereich ist standardmäßig aus. Die Schaltfläche `?` in der Leiste (neben den Einstellungen, oder `F1`) zeigt alle Befehle und Tastenkürzel.

**Wichtig:** Kurzbefehle funktionieren nur, wenn das Eingabefeld aktiv ist, und nicht im Durchklick-Modus. Lange Befehle (mit `Strg` + `Alt`) funktionieren immer.

Die Tastenkürzel ändern Sie in den Einstellungen: Klicken Sie auf das Feld und drücken Sie die Kombination. Wenn ein anderes Programm sie schon benutzt, meldet das die Leiste.

Ziehen Sie die Leiste an ihrem Titel, ihre Position wird gemerkt. Breite, Deckkraft und Schriftgröße sind einstellbar.

### Aussehen und Maus

Der Bereich „Oberfläche“ der Einstellungen:

- **Design** - dunkel (Graphit, Standard) oder hell (Elfenbein);
- **Deckkraft der Leiste** - die ganze Leiste mit ihrem Text (30-100 %);
- **Deckkraft des Hintergrunds** - nur der Hintergrund der Leiste, der Text bleibt scharf (20-100 %);
- **Durch die Leiste klicken** - Klicks gehen durch die Hilfsleiste hindurch zum Fenster darunter. Die Leiste lässt sich mit der Maus weder verschieben noch anklicken, Tastatur und Tastenkürzel funktionieren weiter. Umgeschaltet mit `Strg` + `Alt` + `T`, im Titel der Leiste erscheint dann die Markierung „Klicks durch die Leiste“. Das Einstellungsfenster ist immer ein normales;
- **Schaltflächen durch Verweilen drücken** - lassen Sie den Mauszeiger auf einer Schaltfläche der Leiste ruhen (standardmäßig 3 Sekunden, 1,5-5 möglich), und sie drückt sich selbst. Unter der Schaltfläche füllt sich ein Streifen. Funktioniert auch im Durchklick-Modus.

Listen nimmt den Ton des ganzen Systems auf. Benutzen Sie Kopfhörer: Dann wird nur das Gegenüber aufgenommen, nicht Ihre eigene Stimme.

## Eigene Befehle

Die Ziffernbefehle liegen in `%APPDATA%\Polymath\commands.json` (die Schaltfläche „commands.json öffnen“ in den Einstellungen). Die Datei wird bei jedem Aufruf neu gelesen, ein Neustart ist nicht nötig. Beispiel:

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Felder: `name`, `instructions` (erforderlich), `model` (`main` oder `small`), `screen: true` (einen Screenshot anhängen), `watch: true` (den Bildschirm beobachten), `listen: true` (Listen einschalten). Platzhalter: `{native}` - Ihre Sprache, `{conversation_language}` - die Sprache des Gesprächs.

## Wie zuverlässig das Verstecken ist

Die Fenster werden mit `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)` erstellt. Das ist ein Windows-Mechanismus: Eine Bildschirmaufnahme zeigt stattdessen, was unter dem Fenster liegt. Zoom, Teams, Google Meet im Browser, Discord, OBS, das Snipping Tool, PrintScreen und die Xbox Game Bar halten sich daran.

Außerdem:

- keine Schaltfläche in der Taskleiste und kein Eintrag in Alt+Tab;
- das Symbol im Infobereich ist standardmäßig aus (der Infobereich ist sichtbar, wenn der ganze Bildschirm geteilt wird);
- keine System-Popups: Tooltips, Listen und Menüs werden innerhalb der Leiste gezeichnet, das Kontextmenü ist aus.

Grenzen:

- Das Verstecken schützt nicht vor einer auf den Monitor gerichteten Kamera oder vor einer HDMI-Hardwareaufnahme.
- Wenn Sie ein **Fenster** eines Programms teilen (nicht den ganzen Bildschirm) und die Leiste darüber liegt, sieht die Gegenseite, was unter der Leiste liegt. Das ist zu erwarten.
- Windows älter als 10 Version 2004 zeigt in der Aufnahme statt der Leiste ein schwarzes Rechteck.
- Geöffnete Links und Dateien (commands.json, der Datenordner) öffnen sich in gewöhnlichen Programmen und sind beim Teilen des Bildschirms sichtbar.

Prüfen Sie das Verstecken auf Ihrem Computer:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

Das Skript zeigt zwei geschützte Testfenster und ein normales, nimmt den Bildschirm auf zwei Arten auf und gibt das Ergebnis aus. Die Zeile `RESULT: Polymath windows are hidden from screen capture` bedeutet, dass alles funktioniert.

## Wissensbasis

Der Bereich „Wissensbasis“ der Einstellungen:

- **Über Sie** - allgemeine Informationen über Sie. Das Modell nutzt sie in jeder Antwort.
- **Dateien** - die Schaltfläche „Dateien hinzufügen“, oder ziehen Sie `.txt`- und `.md`-Dateien auf den Bereich. Die Dateien werden nach `%APPDATA%\Polymath\knowledge` kopiert (die Schaltfläche „Ordner öffnen“). Sie können sie dort bearbeiten, das Programm übernimmt die Änderungen selbst. Eine Datei mit demselben Namen wird ersetzt, bis 2 MB, in UTF-8, UTF-16 oder Windows-1251.
- **Die Wissensbasis in Antworten verwenden** - schaltet sich ein, sobald die Basis eine Datei hat.
- **Einen Treffer aus der Basis sofort zeigen, vor der Antwort des Modells** - ebenso.

So funktioniert es. Bei einer Chatfrage und bei jedem Satz des Gegenübers in Listen sucht das Programm zuerst in Ihren Dateien nach einer Antwort, ohne Internet und ohne das Modell. Ein Treffer erscheint sofort als blauer Block „Aus der Wissensbasis“ über der Antwort des Modells, mit einer Schaltfläche „Kopieren“ daneben. Gleichzeitig bekommt das Modell diese Daten (die ganze Basis, wenn sie klein ist, sonst die passenden Teile) und antwortet auf dieser Grundlage. Die Suche versteht verschiedene Wortformen. Die lokale Suche findet keine Frage in einer anderen Sprache, aber das Modell antwortet trotzdem aus der Basis.

Die Dateien lassen sich auf drei Arten schreiben:

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

Oder einfach Absätze, getrennt durch eine Leerzeile: Die kurze erste Zeile eines Absatzes ist sein Thema.

## Verlauf und Export

Der Bereich „Verlauf“ der Einstellungen:

- **Verlauf auf der Festplatte speichern**. Standardmäßig aus: Der Verlauf lebt dann nur im Speicher, bis das Programm geschlossen wird. Ein: Jede Frage und Antwort wird an `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl` angehängt, jede Zeile mit Windows DPAPI verschlüsselt (nur Ihr Windows-Konto kann sie lesen).
- **Name im Verlauf**. Signiert Ihre Fragen im Export. Leer bedeutet den Windows-Benutzernamen.
- **Aufbewahren, Tage**. Ältere Tage werden beim Start gelöscht. 0 behält alles.
- **Exportieren** dieser Sitzung, heute, 7 Tage, 30 Tage oder die gesamte Zeit. „Als .txt exportieren“ speichert eine Datei in `Documents\Polymath`, „Als Text kopieren“ legt denselben Text in die Zwischenablage.
- **Verlauf löschen** entfernt die Verlaufsdateien und die Einträge dieser Sitzung (die Schaltfläche zweimal drücken).

Was aufgezeichnet wird:

- Chat: Q - Ihre Frage (mit dem Befehl und einer Screenshot-Markierung), A - die Antwort des Modells;
- Listen: Q - der Satz des Gegenübers und seine Übersetzung, A - die Ihnen vorgeschlagene Antwort und ihre Übersetzung (wenn eine Antwort nötig war);
- Watch: Antworten auf Aufgaben vom Bildschirm, leere Durchläufe werden nicht aufgezeichnet.

Die Exportdatei ist nicht verschlüsselt. Explorer und Editor, geöffnet mit der Schaltfläche „Datei anzeigen“, sind beim Teilen des Bildschirms sichtbar.

## Datenschutz

- API-Schlüssel werden von Windows verschlüsselt gespeichert (DPAPI über Electron safeStorage) in `%APPDATA%\Polymath\settings.json`.
- Standardmäßig liegt der Verlauf nur im Speicher und ist weg, wenn das Programm schließt. Das Speichern auf der Festplatte wird in den Einstellungen eingeschaltet, die Verlaufsdateien sind mit DPAPI verschlüsselt.
- Dateien der Wissensbasis liegen unverschlüsselt in `%APPDATA%\Polymath\knowledge`, sie werden auf dem Computer durchsucht. Zum Modell gelangen sie nur mit einer Frage: die ganze Basis, wenn sie klein ist, sonst die passenden Teile.
- Ton und Screenshots gehen nur an den gewählten Anbieter (oder den Reserveanbieter) und nur solange Listen, Screenshot oder Watch eingeschaltet ist. Mit lokalem whisper.cpp oder Parakeet verlässt der Ton den Computer nie.
- Fehlerprotokoll: `%APPDATA%\Polymath\logs\app.log` (ohne Gesprächstext).

## Betrieb im Hintergrund

Das Kästchen „Bei der Windows-Anmeldung starten“ startet Polymath ausgeblendet. Rufen Sie die Leiste mit Strg+Alt+P auf. Von Hand: `Polymath.exe --background`.

## Updates

Das installierte Polymath (aus `Polymath-Setup`) sucht wenige Sekunden nach dem Start nach einer neuen Version. Ohne Ihre Zustimmung wird nichts heruntergeladen: Die Leiste zeigt „Polymath X ist verfügbar“ mit den Schaltflächen „Aktualisieren“ und „Später“, nach dem Download „Neu starten und aktualisieren“. Polymath schließt sich, installiert sich über die alte Version und startet neu, Einstellungen, Schlüssel und Verlauf bleiben erhalten. Wenn das Tray-Symbol aktiv ist, hat sein Menü den Eintrag „Check for updates“. Eine Kopie aus dem Quellordner und eine portable Kopie aktualisieren sich nicht selbst.

Der Download wird anhand des SHA-512 in der `latest.yml` des Releases geprüft. Ein Release ohne diesen Hash wird abgelehnt, eine Datei, die nicht passt, wird nicht installiert. Jeder Build prüft, dass `latest.yml` den richtigen Hash enthält. Der Installer ist noch nicht code-signiert, deshalb kann Windows SmartScreen weiterhin warnen.

## Für Entwickler

Node.js 20 oder neuer wird benötigt.

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

- `npm test` - Unit-Tests (Satzerkennung, WAV, Antwortverarbeitung, SSE, Befehle, Einstellungen, Modell-Client, Verlauf).
- `npm run dist` - der Installer in `dist`, danach eine Prüfung, dass `latest.yml` den richtigen SHA-512 enthält.
- `python scripts/make-installer-art.py` - zeichnet die Grafiken des Installationsprogramms (`build/`: Seitenbild, Kopfzeile, Symbol) aus `assets/icon.png` neu. Benötigt Python mit Pillow.
- `npm run capture-test` - die eingebaute Prüfung des Versteckens (Ergebnis als JSON).
- Die Variable `POLYMATH_VISIBLE=1` schaltet das Verstecken im Entwicklungsmodus aus, um Screenshots der Oberfläche zu machen. Im gebauten Programm hat sie keine Wirkung.

Aufbau:

- `src/main` - der Hauptprozess: Fenster, Tastenkürzel, Modell, Spracherkennung, Listen, Watch;
- `src/renderer` - die Leiste und das Einstellungsfenster, Aufnahme des Systemtons;
- `src/shared` - gemeinsamer Code: Satzerkennung, WAV, Textverarbeitung, SSE, Übersetzungen der Oberfläche;
- `scripts` - Installation von whisper.cpp und Parakeet und die Prüfung des Versteckens;
- `tests` - Tests.
