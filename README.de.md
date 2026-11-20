# Polymath für Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

Eine kleine Hilfsleiste für Gespräche und Besprechungen. Sie hört dem Gegenüber zu und übersetzt seine Sprache in Ihre, schlägt eine Antwort in der Sprache des Gesprächs vor, löst eine Aufgabe vom Bildschirm und beantwortet jede Frage im Chat.

**Nur Sie sehen die Leiste.** Sie erscheint nicht, wenn Sie den Bildschirm in Zoom, Teams, Meet, Discord oder OBS teilen, und auch nicht auf Screenshots und in Bildschirmaufnahmen.

## Funktionen

- **Zuhören**. Hört den Systemton des Computers (die Stimme des Gegenübers im Anruf), erkennt Sätze, zeigt eine Übersetzung in Ihre Muttersprache und, wenn Sie angesprochen werden, eine fertige Antwort in der Gesprächssprache mit Übersetzung. Klicken Sie auf eine Antwort, um sie zu kopieren. Der Modus „Nur wenn eine Antwort nötig ist“ zeigt nur die Zeilen, auf die Sie antworten sollten.
- **Bildschirm**. Ein Screenshot wird an das Modell geschickt: Lösen einer Aufgabe, Beantworten einer Testfrage, Code-Review.
- **Beobachten**. Beobachtet den Bildschirm und antwortet, wenn dort eine neue Frage oder Aufgabe erscheint. Schaltet sich nach 10 Minuten selbst aus.
- **Chat**. Gewöhnliche Fragen. Eine Ziffer am Anfang wählt einen Befehl: `1` Schnell (kurze Antwort, schnelles Modell), `3` Antwort (Antwort auf die zuletzt gehörte Frage unter Berücksichtigung des Gesprächs), `5` Übersetzen.
- Das Modell sieht die letzten Sätze des Gesprächs, deshalb können Sie im Chat fragen: „Wie antworte ich auf ihre letzte Frage?“.
- **Wissensbasis**. Ihre eigenen Dateien `.txt` und `.md` mit fertigen Antworten auf häufige Fragen. Eine passende Antwort wird auf dem Computer ohne Internet gefunden und sofort angezeigt, während das Modell noch antwortet.
- **Eigene Befehle**. Fügen Sie eigene Befehle mit Ziffern hinzu, mit eigenen Anweisungen, eigenem Modell sowie Bildschirm- oder Toneinstellungen.
- **Verlauf und Export**. Optionales, verschlüsseltes Speichern der Gespräche und Export in eine Textdatei.

## Installation

In jeder Version werden zwei fertige Dateien veröffentlicht:

- `Polymath-Setup-<Version>.exe` - der Installer, er richtet sich nach der Windows-Sprache und unterstützt 22 Sprachen. Sie können den Ordner wählen, Administratorrechte sind nicht nötig, Verknüpfungen landen auf dem Desktop und im Startmenü, und das Programm startet nach der Installation.

Windows SmartScreen kann vor einem unbekannten Herausgeber warnen, da die Datei noch nicht signiert ist. Klicken Sie auf „Weitere Informationen“ und dann auf „Trotzdem ausführen“.

Voraussetzungen: Windows 10 ab Version 2004 (Mai 2020) oder Windows 11. Auf älteren Systemen funktioniert das Verbergen vor der Bildschirmfreigabe nicht.

Updates: Eine installierte Kopie prüft diese Seite wenige Sekunden nach dem Start auf neue Versionen. Erscheint eine neuere Version, zeigt das Programm eine Karte und lädt das Update erst mit Ihrer Zustimmung herunter. Das Update wird in denselben Ordner installiert, und das Programm startet neu.

## Erster Start

1. Öffnen Sie die Einstellungen (das Zahnrad an der Leiste).
2. Wählen Sie einen Modellanbieter, fügen Sie den API-Schlüssel ein und klicken Sie auf „Schlüssel speichern“. Der Link „Schlüssel holen“ öffnet die Seite des Anbieters.
3. Klicken Sie auf „Verbindung testen“. Es erscheint eine Liste verfügbarer Modelle, ein Klick auf ein Modell setzt es ins Feld.
4. Legen Sie Ihre Muttersprache fest. Beschreiben Sie sich im Abschnitt „Wissensbasis“ kurz im Feld „Über Sie“ (Beruf, Erfahrung). Das Modell nutzt das in seinen Antworten.
5. Klicken Sie auf „Speichern“ (oder drücken Sie Strg+S).

### Anbieter

| Anbieter                       | Standardmodell           | Bilder (Bildschirm/Beobachten) | Ton direkt |
| ------------------------------ | ------------------------ | ------------------------------ | ---------- |
| Google Gemini                  | gemini-flash-lite-latest | ja                             | ja         |
| OpenAI                         | gpt-5-mini               | ja                             | nein       |
| Anthropic Claude               | claude-sonnet-5-5        | ja                             | nein       |
| OpenRouter                     | openrouter/auto          | ja                             | nein       |
| Groq                           | openai/gpt-oss-120b      | nein                           | nein       |
| Mistral                        | mistral-medium-latest    | ja                             | nein       |
| Ollama (lokal)                 | llama3.2                 | nein                           | nein       |
| Benutzerdefiniert (OpenAI-kompatibel) | beliebig          | modellabhängig                 | nein       |

Anbieter benennen ihre Modelle um. Wird ein Modell nicht gefunden, klicken Sie auf „Verbindung testen“ und wählen Sie eines aus der Liste.

Das „Schnellmodell“ wird von den Befehlen „Schnell“ und „Übersetzen“ verwendet. Das Feld darf leer bleiben, dann wird das Hauptmodell genutzt.

Antwortet ein Modell mit 503 (überlastet) oder 429 (Kontingent erschöpft), fragt das Programm sofort das zweite Modell des Paares.

### Reservemodell

Im Abschnitt „Reservemodell“ der Einstellungen legen Sie einen weiteren Anbieter fest, den das Programm fragt, wenn beide Hauptmodelle mit 503 oder 429 antworten. Zum Beispiel Anthropic Claude (standardmäßig `claude-haiku-5-5`, ein schnelles Modell). Der Reserveschlüssel wird separat gespeichert. Fehlt er, wird der Schlüssel desselben Anbieters aus dem Abschnitt „Modell“ verwendet. Die Reserve wird übersprungen, wenn sie das Gesendete nicht lesen kann, etwa ein Bild vom Bildschirm (Bildschirm/Beobachten) oder Ton.

## Spracherkennung (für „Zuhören“)

In den Einstellungen „Spracherkennung“ stehen vier Varianten zur Auswahl:

1. **Über das Modell** (Standard). Der Satz geht direkt an das Chatmodell. Funktioniert mit Google Gemini, mit demselben Schlüssel.
2. **Whisper-API in der Cloud**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, schnell und günstig) oder Ihr eigener, mit OpenAI kompatibler Server. Der Erkennungsschlüssel wird getrennt vom Modellschlüssel gespeichert.
3. **Lokal (whisper.cpp)**. Der Ton verlässt den Computer nie. Die Installation erfolgt mit einem Befehl, die Dateien landen in `%APPDATA%\Polymath\whisper`. Wählen Sie dann „Lokal“ und klicken Sie auf „Erkennung testen“. Standardmäßig wird das kleine Modell verwendet (466 MB). Andere Größen und die Beschleunigung auf NVIDIA-Grafikkarten sind als Optionen des Installationsskripts verfügbar.
4. **Lokal (NVIDIA Parakeet)**. Ebenfalls auf diesem Computer, auf dem Prozessor schneller als whisper.cpp und meist genauer. Das Modell kennt 25 europäische Sprachen (Englisch, Russisch, Ukrainisch, Deutsch, Französisch, Spanisch und weitere), aber kein Türkisch und kein Chinesisch. Die Schaltfläche „Parakeet herunterladen“ in den Einstellungen richtet das Modell ein. Insgesamt sind es etwa 520 MB. Wählen Sie danach „Lokal (NVIDIA Parakeet)“ und klicken Sie auf „Erkennung testen“. Der erste Satz nach einer Pause wartet 7-10 Sekunden, bis das Modell geladen ist, die folgenden brauchen weniger als eine Sekunde. Ohne Sprache 10 Minuten lang stoppt der Server und gibt den Speicher frei.

Beim ersten Start auf einem neuen Computer fragt die Leiste einmal, wie gesprochen werden soll: über Gemini (nichts herunterzuladen) oder mit Parakeet auf diesem Computer (das Programm lädt etwa 520 MB, mit Fortschrittsanzeige und Abbrechen-Schaltfläche). Die Antwort lässt sich später in den Einstellungen ändern.

Die Schaltfläche „Erkennung testen“ funktioniert für alle vier Varianten.

## Bedienung

| Aktion                           | Tastenkürzel                   |
| -------------------------------- | ------------------------------ |
| Leiste zeigen / verbergen        | `Strg` + `Alt` + `P`           |
| Aufgabe vom Bildschirm lösen     | `Strg` + `Alt` + `2`           |
| Bildschirm beobachten (ein/aus)  | `Strg` + `Alt` + `4`           |
| Anruf anhören (ein/aus)          | `Strg` + `Alt` + `7`           |
| Klicks durch die Leiste (ein/aus)| `Strg` + `Alt` + `T`           |
| Senden                           | `Enter`                        |
| Neue Zeile                       | `Umschalt` + `Enter`           |
| Antwort stoppen                  | `Strg` + `.` oder die Taste `■` |
| Neues Gespräch                   | `Strg` + `N` oder die Taste `+` |
| Vorherige Anfrage                | `↑` / `↓` im leeren Feld       |
| Leiste verbergen                 | `Esc`                          |

Die Tastenkürzel ändern Sie in den Einstellungen: Klicken Sie auf das Feld und drücken Sie die gewünschte Kombination. Nutzt bereits ein anderes Programm das Kürzel, meldet die Leiste das.

Die Leiste ziehen Sie an ihrer Titelzeile, ihre Position wird gespeichert. Breite, Deckkraft und Schriftgröße sind einstellbar.

### Aussehen und Maus

Der Abschnitt „Oberfläche“ in den Einstellungen:

- **Design**: dunkel (Graphit, Standard) oder hell (Elfenbein).
- **Deckkraft der Leiste**: die ganze Leiste mit Text (30-100 %).
- **Deckkraft des Hintergrunds**: nur der Hintergrund der Leiste, der Text bleibt scharf (20-100 %).
- **Klicks durch die Leiste**: Klicks gehen durch die Hilfsleiste hindurch auf das Fenster darunter. Die Leiste lässt sich dann nicht mit der Maus verschieben oder anklicken, Tastatur und Kürzel funktionieren aber weiter. Umgeschaltet wird mit `Strg` + `Alt` + `T`, in der Titelzeile erscheint dann die Markierung „Klicks durch“. Das Einstellungsfenster ist immer ein normales Fenster.
- **Tasten per Hover drücken**: Legen Sie den Mauszeiger auf eine Schaltfläche der Leiste (standardmäßig 3 Sekunden, möglich sind 1,5 bis 5), und sie drückt sich selbst. Unter der Schaltfläche füllt sich ein Balken. Funktioniert auch im Modus „Klicks durch“.

„Zuhören“ erfasst den Ton des gesamten Systems. Verwenden Sie Kopfhörer, dann wird nur das Gegenüber aufgenommen und nicht Ihre eigene Stimme.

## Eigene Befehle

Die Befehle mit Ziffern liegen in `%APPDATA%\Polymath\commands.json` (Schaltfläche „commands.json öffnen“ in den Einstellungen). Die Datei wird bei jedem Aufruf neu gelesen, ein Neustart ist nicht nötig. Beispiel:

```json
{
  "1": {
    "name": "Vorstellungsgespräch",
    "instructions": "Antworte wie ein erfahrener Java-Entwickler im Vorstellungsgespräch. Antworte auf {conversation_language} und gib danach eine kurze Übersetzung auf {native}.",
    "model": "main"
  }
}
```

Felder: `name`, `instructions` (Pflicht), `model` (`main` oder `small`), `screen: true` (Screenshot anhängen), `watch: true` (Bildschirm beobachten), `listen: true` (Zuhören einschalten). Platzhalter: `{native}` ist Ihre Sprache, `{conversation_language}` die Sprache des Gesprächs.

## Verbergen vor der Bildschirmfreigabe

Die Fenster werden mit dem Windows-Mechanismus erstellt, der sie von der Aufnahme ausschließt (`WDA_EXCLUDEFROMCAPTURE`). Bei einer Bildschirmaufnahme sieht man stattdessen, was sich unter dem Fenster befindet. Zoom, Teams, Google Meet im Browser, Discord, OBS, das Snipping Tool, PrintScreen und die Xbox Game Bar berücksichtigen dies.

Außerdem:

- kein Symbol in der Taskleiste und kein Eintrag in Alt+Tab;
- das Infobereich-Symbol ist standardmäßig aus (der Infobereich ist sichtbar, wenn der ganze Bildschirm geteilt wird);
- keine Systemfenster: Hinweise, Listen und Menüs werden innerhalb der Leiste gezeichnet, das Kontextmenü ist deaktiviert.

Grenzen:

- Das Verbergen schützt nicht vor einer Kamera, die auf den Monitor gerichtet ist, und nicht vor einer HDMI-Hardwareaufnahme.
- Teilen Sie ein **Fenster** eines Programms (nicht den ganzen Bildschirm) und liegt die Leiste darüber, sieht die Gegenseite, was sich unter der Leiste befindet. Das ist erwartungsgemäß.
- Unter Windows älter als 10 Version 2004 erscheint in der Aufnahme statt der Leiste ein schwarzes Rechteck.
- Geöffnete Links und Dateien (commands.json, Datenordner) öffnen sich in gewöhnlichen Programmen und sind bei der Bildschirmfreigabe sichtbar.

## Wissensbasis

Der Abschnitt „Wissensbasis“ in den Einstellungen:

- **Über Sie**: allgemeine Informationen über Sie. Das Modell nutzt sie in jeder Antwort.
- **Dateien**: die Schaltfläche „Dateien hinzufügen“ oder das Ziehen von `.txt`- und `.md`-Dateien in den Abschnitt. Die Dateien werden nach `%APPDATA%\Polymath\knowledge` kopiert (Schaltfläche „Ordner öffnen“). Dort dürfen Sie sie bearbeiten, das Programm übernimmt die Änderungen selbst. Eine Datei mit demselben Namen wird ersetzt. Das Limit liegt bei 2 MB pro Datei, Kodierungen UTF-8, UTF-16 oder Windows-1251.
- **Wissensbasis in Antworten verwenden**: wird aktiv, sobald die Basis eine Datei enthält.
- **Passenden Treffer aus der Basis sofort zeigen, vor der Antwort des Modells**: dasselbe.

So funktioniert es. Bei einer Chatfrage und bei jedem Satz des Gegenübers im Modus „Zuhören“ sucht das Programm zuerst in Ihren Dateien nach einer Antwort, ohne Internet und ohne Modell. Ein Treffer erscheint sofort als blauer Block „Aus der Wissensbasis“ über der Antwort des Modells, daneben gibt es die Schaltfläche „Kopieren“. Gleichzeitig erhält das Modell diese Daten (die ganze Basis, wenn sie klein ist, sonst die gefundenen Teile) und antwortet darauf gestützt. Die Suche erkennt verschiedene Wortformen. Die lokale Suche findet eine Frage in einer anderen Sprache nicht, das Modell antwortet aber trotzdem aus der Basis.

Drei Möglichkeiten, die Dateien zu schreiben:

```markdown
# Welches Gehalt erwarten Sie?
Ab 5.000 USD netto, über alles weitere reden wir gern.

# Warum verlassen Sie Ihre aktuelle Stelle?
Ich möchte mehr Architekturarbeit machen.
```

```text
Q: Wie lang ist Ihre Kündigungsfrist?
A: Zwei Wochen.
```

Oder einfach Absätze, getrennt durch eine Leerzeile. Die kurze erste Zeile eines Absatzes ist sein Thema.

## Verlauf und Export

Der Abschnitt „Verlauf“ in den Einstellungen:

- **Verlauf auf Datenträger speichern**. Standardmäßig aus: Der Verlauf lebt dann nur im Speicher, bis das Programm geschlossen wird. Ist es an, wird jede Frage und Antwort in die Tagesdatei unter `%APPDATA%\Polymath\history` angehängt, und jede Zeile wird mit Windows DPAPI verschlüsselt, sodass nur Ihr Windows-Konto sie lesen kann.
- **Name im Verlauf**. Kennzeichnet Ihre Fragen im Export. Leer bedeutet der Windows-Benutzername.
- **Aufbewahren, Tage**. Ältere Tage werden beim Start gelöscht. 0 bedeutet alles behalten.
- **Export** dieser Sitzung, von heute, 7 Tagen, 30 Tagen oder der ganzen Zeit. „Als .txt exportieren“ speichert eine Datei in `Dokumente\Polymath`, „Als Text kopieren“ legt denselben Text in die Zwischenablage.
- **Verlauf löschen** entfernt die Verlaufsdateien und die Einträge dieser Sitzung (die Schaltfläche muss zweimal gedrückt werden).

Was aufgezeichnet wird:

- Chat: die Frage (mit Befehl und Screenshot-Markierung) und die Antwort des Modells;
- Zuhören: der Satz des Gegenübers und seine Übersetzung sowie die vorgeschlagene Antwort und ihre Übersetzung, wenn eine Antwort nötig war;
- Beobachten: Antworten auf Aufgaben vom Bildschirm. Leere Durchläufe werden nicht aufgezeichnet.

Die Exportdatei ist nicht verschlüsselt. Explorer und Notepad, geöffnet über die Schaltfläche „Datei anzeigen“, sind bei der Bildschirmfreigabe sichtbar.

## Datenschutz

- API-Schlüssel werden von Windows verschlüsselt gespeichert (DPAPI) in `%APPDATA%\Polymath\settings.json`.
- Standardmäßig liegt der Verlauf nur im Speicher und ist nach dem Schließen des Programms weg. Das Speichern auf Datenträger schalten Sie in den Einstellungen ein, die Verlaufsdateien werden dann mit DPAPI verschlüsselt.
- Dateien der Wissensbasis liegen unverschlüsselt in `%APPDATA%\Polymath\knowledge` und werden auf dem Computer durchsucht. Zum Modell gelangen sie nur zusammen mit einer Frage: die ganze Basis, wenn sie klein ist, sonst die passenden Teile.
- Ton und Screenshots gehen nur an den gewählten Anbieter (oder den Reserveanbieter) und nur, solange „Zuhören“, „Bildschirm“ oder „Beobachten“ eingeschaltet ist. Mit lokalem whisper.cpp oder Parakeet verlässt der Ton den Computer nie.
- Das Fehlerprotokoll liegt in `%APPDATA%\Polymath\logs\app.log`. Es enthält keinen Gesprächstext.

## Start im Hintergrund

Das Kästchen „Beim Anmelden an Windows starten“ startet Polymath versteckt. Die Leiste rufen Sie mit `Strg` + `Alt` + `P` auf.

## Voraussetzungen und Grenzen

- Windows 10 ab Version 2004 oder Windows 11.
- Internet für Cloud-Modelle nötig. Die lokale Spracherkennung funktioniert nach der Installation ohne Netz.
- Ein Schlüssel mindestens eines Modellanbieters. Die Schlüssel gehören Ihnen, abgerechnet werden sie vom Anbieter.
