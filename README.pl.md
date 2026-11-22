# Polymath dla Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**
(Twój cichy partner AI w każdej rozmowie)

Polymath siedzi obok ciebie i pomaga, gdy zabraknie ci słów albo wiedzy. Słyszy, co mówi rozmówca, widzi, co masz na ekranie, i podpowiada, co zrobić dalej. Nikt poza tobą go nie widzi i nigdy nie mówi za ciebie.

### Do czego służy

- **Rozmowy z ludźmi, których języka nie znasz.** Polymath słucha rozmówcy i pokazuje, co powiedział. Potem podpowiada, co odpowiedzieć w jego języku i w twoim ojczystym (żebyś zawsze wiedział, co dokładnie mu mówisz). Sam zostajesz w rozmowie, zamiast chować się za tłumaczem.
- **Randki online.** Polymath może obserwować twój ekran i podpowiadać, jak odpowiedzieć w języku rozmówcy i w twoim ojczystym (żebyś zawsze wiedział, co dokładnie piszesz). Piszesz wiadomość, która brzmi jak ty, tylko lepiej.
- **Flirt.** Dostań pomysł na odpowiedź, żart albo komplement dokładnie wtedy, gdy go potrzebujesz.
- **Codzienne sprawy.** Zadaj pytanie, zrób zrzut ekranu za pomocą aplikacji i dostań odpowiedź dopasowaną do twojej sytuacji.
- **Trudne i niezrozumiałe rzeczy.** Nie wiesz, gdzie kliknąć albo dlaczego coś nie działa? Pokaż ekran Polymathowi, a wskaże błąd i powie, jak go naprawić.

### Co kiedyś przerażało, z Polymath jest w zasięgu ręki

- Pójść na rozmowę kwalifikacyjną online i wiedzieć, co powiedzieć.
- Ustawić reklamy w Google lub Meta bez marnowania budżetu.
- Zrobić swoją pierwszą stronę internetową i wrzucić ją na dowolny hosting.
- Zrozumieć umowę najmu lub kredytu i nie przeoczyć drobnego druku.
- Wypełnić zeznanie podatkowe albo złożyć wniosek wizowy bez błędów w dokumentach.
- Napisać CV i list motywacyjny, które się wyróżnią, także w obcym języku.
- Negocjować cenę lub rabat, omówić warunki z właścicielem mieszkania, wykonawcą albo klientem.
- Zrozumieć pismo z banku, urzędu skarbowego lub od ubezpieczyciela i dowiedzieć się, czego naprawdę od ciebie chcą.
- Skonfigurować router Wi-Fi, drukarkę lub telefon, gdy nic nie działa, a fachowiec jest drogi albo niedostępny.
- Napisać przekonującą reklamację do sklepu, linii lotniczej albo zarządcy nieruchomości.
- Przygotować się do trudnej rozmowy z szefem, partnerem lub rodzicami i znaleźć właściwe słowa.

Kiedyś potrzebny był specjalista obok albo telefon do znajomego. Teraz masz Polymath, który zna się na każdej dziedzinie i jest zawsze pod ręką.

---

Mały pasek-pomocnik do rozmów i spotkań. Słucha rozmówcy i tłumaczy jego głos na Twój język, podpowiada odpowiedź w języku rozmowy, rozwiązuje zadanie z ekranu i odpowiada na dowolne pytanie na czacie.

**Pasek widzisz tylko Ty.** Nie pojawia się podczas udostępniania ekranu w Zoom, Teams, Meet, Discord i OBS, ani na zrzutach ekranu i nagraniach.

## Funkcje

- **Listen** (`7` / `Ctrl` + `Alt` + `7`). Słucha dźwięku komputera (głosu rozmówcy podczas rozmowy), rozpoznaje frazy, pokazuje tłumaczenie na Twój język ojczysty, a gdy zwracają się do Ciebie - gotową odpowiedź w języku rozmowy wraz z tłumaczeniem. Kliknięcie odpowiedzi kopiuje ją. Tryb „Tylko gdy potrzebna jest odpowiedź” pokazuje wyłącznie te wypowiedzi, na które trzeba odpowiedzieć.
- **Screenshot** (`2` / `Ctrl` + `Alt` + `2`). Zrzut ekranu trafia do modelu: rozwiązanie zadania, odpowiedź na pytanie z testu, przegląd kodu.
- **Watch** (`4` / `Ctrl` + `Alt` + `4`). Obserwuje ekran i odpowiada, gdy pojawi się na nim nowe pytanie lub zadanie. Wyłącza się sam po 10 minutach.
- **Czat**. Zwykłe pytania. Cyfra na początku wybiera polecenie: `1` Quick (krótko, model szybki), `3` Answer (jedna odpowiedź na ostatnie usłyszane pytanie, z uwzględnieniem rozmowy), `5` Translate.
- Model widzi ostatnie frazy rozmowy, więc na czacie możesz zapytać „jak odpowiedzieć na ich ostatnie pytanie?”.
- **Baza wiedzy**. Własne pliki `.txt` i `.md` z gotowymi odpowiedziami na częste pytania. Pasująca odpowiedź jest szukana na komputerze, bez internetu, i pokazywana od razu, gdy model jeszcze odpowiada.

## Instalacja

Gotowe pliki są w folderze `dist`:

- `Polymath-Setup-<wersja>.exe` - instalator, dopasowuje się do języka Windows i obsługuje 22 języki: można wybrać folder, nie są potrzebne uprawnienia administratora, skróty na pulpicie i w menu Start, program uruchamia się po instalacji;

Windows SmartScreen może ostrzec o nieznanym wydawcy (plik nie jest podpisany). Kliknij „Więcej informacji” i „Uruchom mimo to”.

Wymagania: Windows 10 w wersji 2004 (maj 2020) lub nowszy, Windows 11. W starszych systemach ukrywanie przed przechwytywaniem ekranu nie działa.

## Pierwsze uruchomienie

1. Otwórz ustawienia (koło zębate na pasku).
2. Wybierz dostawcę modelu, wklej klucz API i kliknij „Zapisz klucz”. Link „Pobierz klucz” otwiera stronę dostawcy.
3. Kliknij „Sprawdź połączenie”. Pojawi się lista dostępnych modeli, kliknięcie modelu wstawia go do pola.
4. Podaj swój język ojczysty. W sekcji „Baza wiedzy” opisz się krótko w polu „O tobie” (praca, doświadczenie). Model używa tego w odpowiedziach.
5. Kliknij „Zapisz” (lub Ctrl+S).

### Dostawcy

| Dostawca                     | Model domyślny           | Obrazy (Screenshot/Watch)   | Dźwięk bezpośrednio |
| ---------------------------- | ------------------------ | ----------------------- | ------------------- |
| Google Gemini                | gemini-flash-lite-latest | tak                     | tak                 |
| OpenAI                       | gpt-5-mini               | tak                     | nie                 |
| Anthropic Claude             | claude-sonnet-5-5        | tak                     | nie                 |
| OpenRouter                   | openrouter/auto          | tak                     | nie                 |
| Groq                         | openai/gpt-oss-120b      | nie                     | nie                 |
| Mistral                      | mistral-medium-latest    | tak                     | nie                 |
| Ollama (lokalnie)            | llama3.2                 | nie                     | nie                 |
| Własny (zgodny z OpenAI)     | dowolny                  | zależy od modelu        | nie                 |

Dostawcy zmieniają nazwy modeli. Jeśli model nie zostanie znaleziony, kliknij „Sprawdź połączenie” i wybierz model z listy.

„Model szybki” jest używany przez polecenia Quick i Translate. Może pozostać pusty, wtedy używany jest model główny.

Gdy model odpowiada 503 (przeciążony) lub 429 (brak limitu), program od razu pyta drugi model z pary.

### Model zapasowy

Sekcja „Model zapasowy” w ustawieniach: kolejny dostawca, którego program pyta, gdy oba powyższe modele odpowiadają 503 lub 429. Na przykład Anthropic Claude (domyślnie `claude-haiku-5-5`, szybki). Klucz zapasowy jest przechowywany osobno. Bez niego używany jest klucz tego samego dostawcy z sekcji „Model”. Model zapasowy jest pomijany, gdy nie potrafi odczytać tego, co jest wysyłane: obrazu z ekranu (Screenshot/Watch) lub dźwięku.

## Rozpoznawanie mowy (dla Listen)

Ustawienia „Rozpoznawanie mowy” oferują cztery silniki:

1. **Przez model** (domyślnie). Fraza trafia bezpośrednio do modelu czatu. Działa z Google Gemini, na tym samym kluczu.
2. **Chmurowe API Whisper**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, szybki i tani) lub własny serwer zgodny z OpenAI. Klucz rozpoznawania jest przechowywany osobno od klucza modelu.
3. **Lokalnie (whisper.cpp)**. Dźwięk nigdy nie opuszcza komputera. Instaluje się jednym poleceniem:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

W zainstalowanym programie skrypt leży w `<folder programu>\resources\scripts`. Opcje: `-Model tiny|base|small|medium|large-v3-turbo` (domyślnie small, 466 MB) oraz `-Cuda` dla kart graficznych NVIDIA. Pliki trafiają do `%APPDATA%\Polymath\whisper`. Potem wybierz „Lokalnie” i kliknij „Sprawdź rozpoznawanie”.

4. **Lokalnie (NVIDIA Parakeet)**. Również na tym komputerze, szybciej niż whisper.cpp na procesorze i zwykle dokładniej. Model `parakeet-tdt-0.6b-v3` zna 25 języków europejskich (angielski, rosyjski, ukraiński, niemiecki, francuski, hiszpański i inne), ale nie turecki ani chiński. Działa przez [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx). Przycisk „Pobierz Parakeet” w ustawieniach ustawia wszystko, albo jedno polecenie:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

W sumie około 520 MB. Opcja `-Model v2` pobiera model tylko angielski, nieco dokładniejszy po angielsku. Pliki trafiają do `%APPDATA%\Polymath\parakeet`. Potem wybierz „Lokalnie (NVIDIA Parakeet)” i kliknij „Sprawdź rozpoznawanie”. Pierwsza fraza po przerwie czeka 7-10 s na załadowanie modelu, kolejne trwają poniżej sekundy. Po 10 minutach bez mowy serwer zatrzymuje się i zwalnia pamięć. Oba pobrania (program i model) są sprawdzane względem SHA-256 publikowanego przez GitHub. Plik, który się nie zgadza, jest usuwany i nic nie jest instalowane. Bez opublikowanego skrótu nie ma instalacji.

Przy pierwszym uruchomieniu na nowym komputerze pasek jednorazowo pyta, jak rozpoznawać głos: przez Gemini (nic do pobrania) czy przez Parakeet na tym komputerze (aplikacja pobiera około 520 MB, z postępem i przyciskiem anulowania). Odpowiedź można później zmienić w ustawieniach.

Przycisk „Sprawdź rozpoznawanie” działa dla wszystkich czterech silników.

## Jak używać

| Działanie                          | Skrót                          |
| ---------------------------------- | ------------------------------ |
| Pokaż / ukryj pasek                | `Ctrl` + `Alt` + `P`           |
| Szybka odpowiedź (krótko, szybki model) | `Ctrl` + `Alt` + `1` |
| Rozwiąż zadanie z ekranu           | `Ctrl` + `Alt` + `2`           |
| Odpowiedź na właśnie usłyszane pytanie | `Ctrl` + `Alt` + `3` |
| Obserwuj ekran (wł./wył.)          | `Ctrl` + `Alt` + `4`           |
| Tłumacz | `Ctrl` + `Alt` + `5` |
| Słuchaj rozmowy (wł./wył.)         | `Ctrl` + `Alt` + `7`           |
| Klikanie przez pasek (wł./wył.)    | `Ctrl` + `Alt` + `T`           |
| Wyślij                             | `Enter`                        |
| Nowy wiersz                        | `Shift` + `Enter`              |
| Zatrzymaj odpowiedź                | `Ctrl` + `.` lub przycisk `■`  |
| Nowa rozmowa                       | `Ctrl` + `N` lub przycisk `+`  |
| Poprzednie zapytanie               | `↑` / `↓` w pustym polu        |
| Ukryj pasek                        | `Esc`                          |

### Polecenia krótkie i długie

Polecenia krótkie działają w pasku, długie (z `Ctrl` + `Alt`) z dowolnego okna. Cyfra w pustym polu wybiera polecenie, działa też `1 twój tekst`.

| Czynność | Krótkie (w pasku) | Długie (z dowolnego okna) |
| --- | --- | --- |
| Szybka odpowiedź (krótko, szybki model) | `1` | `Ctrl` + `Alt` + `1` |
| Rozwiąż zadanie z ekranu | `2` | `Ctrl` + `Alt` + `2` |
| Odpowiedź na właśnie usłyszane pytanie | `3` | `Ctrl` + `Alt` + `3` |
| Obserwuj ekran (wł./wył.) | `4` | `Ctrl` + `Alt` + `4` |
| Tłumacz | `5` | `Ctrl` + `Alt` + `5` |
| Słuchaj rozmowy (wł./wył.) | `7` | `Ctrl` + `Alt` + `7` |
| Pokaż / ukryj pasek | `Esc` | `Ctrl` + `Alt` + `P` |
| Klikanie przez pasek (wł./wył.) | - | `Ctrl` + `Alt` + `T` |
| Ustawienia | `Ctrl` + `,` | `Ctrl` + `,` |
| Nowa rozmowa | `Ctrl` + `N` | - |
| Zatrzymaj odpowiedź | `Ctrl` + `.` | - |
| Pokaż wszystkie skróty | `F1` | - |

**Pasek ukryty?** Naciśnij `Ctrl` + `Alt` + `P` (lub skrót ustawiony w ustawieniach) albo uruchom Polymath ponownie (skrót w menu Start), a pasek wróci. Ikona w zasobniku jest domyślnie wyłączona. Przycisk `?` w pasku (obok ustawień, lub `F1`) pokazuje wszystkie polecenia i skróty.

**Ważne:** krótkie polecenia działają tylko przy aktywnym polu wpisywania i nie działają w trybie klikania przez pasek. Długie polecenia (z `Ctrl` + `Alt`) działają zawsze.

Skróty zmienia się w ustawieniach: kliknij pole i naciśnij kombinację. Jeśli zajmuje ją inny program, pasek o tym poinformuje.

Przeciągaj pasek za tytuł, jego położenie jest zapamiętywane. Szerokość, przezroczystość i rozmiar czcionki można dostosować.

### Wygląd i mysz

Sekcja „Interfejs” w ustawieniach:

- **Motyw** - ciemny (grafit, domyślnie) lub jasny (kość słoniowa);
- **Przezroczystość paska** - cały pasek wraz z tekstem (30-100%);
- **Przezroczystość tła** - tylko tło paska, tekst pozostaje wyraźny (20-100%);
- **Klikanie przez pasek** - kliknięcia przechodzą przez pasek-pomocnik do okna pod spodem. Paska nie da się przesuwać ani klikać myszą, klawiatura i skróty nadal działają. Przełącza się przez `Ctrl` + `Alt` + `T`, a w tytule paska pojawia się wtedy znacznik „klikanie przez”. Okno ustawień jest zawsze zwykłym oknem;
- **Naciskaj przyciski przez najechanie** - zatrzymaj kursor na przycisku paska (domyślnie 3 sekundy, od 1,5 do 5), a zostanie naciśnięty sam. Pod przyciskiem wypełnia się pasek. Działa także w trybie klikania przez pasek.

Listen przechwytuje dźwięk całego systemu. Używaj słuchawek: wtedy nagrywany jest tylko rozmówca, a nie Twój własny głos.

## Własne polecenia

Polecenia cyfrowe znajdują się w `%APPDATA%\Polymath\commands.json` (przycisk „Otwórz commands.json” w ustawieniach). Plik jest czytany ponownie przy każdym wywołaniu, restart nie jest potrzebny. Przykład:

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Pola: `name`, `instructions` (wymagane), `model` (`main` lub `small`), `screen: true` (dołącz zrzut ekranu), `watch: true` (obserwuj ekran), `listen: true` (włącz Listen). Zmienne: `{native}` - Twój język, `{conversation_language}` - język rozmowy.

## Jak niezawodne jest ukrywanie

Okna są tworzone z `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)`. To mechanizm Windows: zrzut ekranu pokazuje w tym miejscu to, co jest pod oknem. Respektują go Zoom, Teams, Google Meet w przeglądarce, Discord, OBS, Narzędzie wycinania, PrintScreen i Xbox Game Bar.

Dodatkowo:

- brak przycisku na pasku zadań i wpisu w Alt+Tab;
- ikona w zasobniku jest domyślnie wyłączona (zasobnik widać przy udostępnianiu całego ekranu);
- brak systemowych okien wyskakujących: podpowiedzi, listy i menu są rysowane wewnątrz paska, menu kontekstowe jest wyłączone.

Ograniczenia:

- Ukrywanie nie chroni przed kamerą skierowaną na monitor ani przed sprzętowym przechwytywaniem HDMI.
- Jeśli udostępniasz **okno** programu (a nie cały ekran), a pasek leży nad nim, druga strona zobaczy to, co jest pod paskiem. To oczekiwane zachowanie.
- Windows starszy niż 10 w wersji 2004 pokazuje na zrzucie czarny prostokąt zamiast paska.
- Otwierane linki i pliki (commands.json, folder danych) otwierają się w zwykłych programach i są widoczne podczas udostępniania ekranu.

Sprawdź ukrywanie na swoim komputerze:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

Skrypt pokazuje dwa chronione okna testowe i jedno zwykłe, przechwytuje ekran na dwa sposoby i wypisuje wynik. Linia `RESULT: Polymath windows are hidden from screen capture` oznacza, że wszystko działa.

## Baza wiedzy

Sekcja „Baza wiedzy” w ustawieniach:

- **O tobie** - ogólne informacje o Tobie. Model używa ich w każdej odpowiedzi.
- **Pliki** - przycisk „Dodaj plik” lub przeciągnij pliki `.txt` i `.md` na sekcję. Pliki są kopiowane do `%APPDATA%\Polymath\knowledge` (przycisk „Otwórz folder”). Możesz je tam edytować, program sam odbiera zmiany. Plik o tej samej nazwie jest zastępowany, do 2 MB, w UTF-8, UTF-16 lub Windows-1251.
- **Używaj bazy wiedzy w odpowiedziach** - włącza się, gdy w bazie jest plik.
- **Pokaż dopasowanie z bazy od razu, zanim odpowie model** - tak samo.

Jak to działa. Dla pytania na czacie i dla każdej frazy rozmówcy w Listen program najpierw szuka odpowiedzi w Twoich plikach, bez internetu i bez modelu. Dopasowanie pojawia się od razu jako niebieski blok „Z bazy wiedzy” nad odpowiedzią modelu, z przyciskiem „Kopiuj” obok. Jednocześnie model otrzymuje te dane (całą bazę, gdy jest mała, w przeciwnym razie pasujące fragmenty) i odpowiada na ich podstawie. Wyszukiwanie rozumie różne formy słów. Wyszukiwanie lokalne nie znajdzie pytania w innym języku, ale model i tak odpowie na podstawie bazy.

Dowolny z trzech sposobów zapisu plików:

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

Albo po prostu akapity oddzielone pustym wierszem: krótka pierwsza linia akapitu jest jego tematem.

## Historia i eksport

Sekcja „Historia” w ustawieniach:

- **Zapisuj historię na dysku**. Domyślnie wyłączone: historia żyje wtedy tylko w pamięci do zamknięcia programu. Włączone: każde pytanie i odpowiedź jest dopisywane do `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl`, każdy wiersz szyfrowany przez Windows DPAPI (odczyta go tylko Twoje konto Windows).
- **Nazwa w historii**. Podpisuje Twoje pytania w eksportach. Puste oznacza nazwę użytkownika Windows.
- **Przechowywanie, dni**. Starsze dni są usuwane przy uruchomieniu. 0 zachowuje wszystko.
- **Eksportuj** tę sesję, dziś, 7 dni, 30 dni lub cały okres. „Eksportuj do .txt” zapisuje plik w `Documents\Polymath`, „Kopiuj jako tekst” umieszcza ten sam tekst w schowku.
- **Wyczyść historię** usuwa pliki historii i wpisy tej sesji (naciśnij przycisk dwa razy).

Co jest zapisywane:

- czat: Q - Twoje pytanie (z poleceniem i znacznikiem zrzutu ekranu), A - odpowiedź modelu;
- Listen: Q - fraza rozmówcy i jej tłumaczenie, A - podpowiedziana Ci odpowiedź i jej tłumaczenie (gdy odpowiedź była potrzebna);
- Watch: odpowiedzi na zadania z ekranu, puste przebiegi nie są zapisywane.

Plik eksportu nie jest szyfrowany. Eksplorator i Notatnik, otwarte przyciskiem „Pokaż plik”, są widoczne podczas udostępniania ekranu.

## Prywatność

- Klucze API są przechowywane zaszyfrowane przez Windows (DPAPI przez Electron safeStorage) w `%APPDATA%\Polymath\settings.json`.
- Domyślnie historia jest tylko w pamięci i znika po zamknięciu programu. Zapis na dysk włącza się w ustawieniach, pliki historii są szyfrowane przez DPAPI.
- Pliki bazy wiedzy są przechowywane w `%APPDATA%\Polymath\knowledge` bez szyfrowania, wyszukuje się w nich na komputerze. Do modelu trafiają tylko wraz z pytaniem: cała baza, gdy jest mała, w przeciwnym razie pasujące fragmenty.
- Dźwięk i zrzuty ekranu trafiają wyłącznie do wybranego dostawcy (lub zapasowego) i tylko wtedy, gdy Listen, Screenshot lub Watch są włączone. Przy lokalnym whisper.cpp lub Parakeet dźwięk nigdy nie opuszcza komputera.
- Dziennik błędów: `%APPDATA%\Polymath\logs\app.log` (bez tekstu rozmów).

## Praca w tle

Pole „Uruchamiaj przy logowaniu do Windows” uruchamia Polymath w ukryciu. Wywołaj pasek przez Ctrl+Alt+P. Ręcznie: `Polymath.exe --background`.

## Aktualizacje

Zainstalowany Polymath (z `Polymath-Setup`) kilka sekund po uruchomieniu szuka nowej wersji. Bez Twojej zgody nic się nie pobiera: pasek pokazuje „Dostępny jest Polymath X” z przyciskami „Zaktualizuj” i „Później”, a po pobraniu „Uruchom ponownie i zaktualizuj”. Polymath zamyka się, instaluje na starej wersji i uruchamia ponownie, ustawienia, klucze i historia zostają. Jeśli ikona w zasobniku jest włączona, jej menu ma pozycję „Check for updates”. Kopia uruchomiona z folderu ze źródłami i kopia przenośna nie aktualizują się same.

Pobrany plik jest sprawdzany względem SHA-512 z `latest.yml` wydania. Wydanie bez tego skrótu jest odrzucane, a plik, który się nie zgadza, nie jest instalowany. Każda kompilacja sprawdza, że `latest.yml` zawiera właściwy skrót. Instalator nie jest jeszcze podpisany, więc Windows SmartScreen nadal może ostrzegać.

## Dla programistów

Wymagany jest Node.js 20 lub nowszy.

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

- `npm test` - testy jednostkowe (detektor fraz, WAV, analiza odpowiedzi, SSE, polecenia, ustawienia, klient modelu, historia).
- `npm run dist` - instalator w `dist`, a potem sprawdzenie, że `latest.yml` zawiera właściwy SHA-512.
- `python scripts/make-installer-art.py` - ponownie rysuje grafiki instalatora (`build/`: obraz boczny, nagłówek, ikona) z `assets/icon.png`. Wymaga Pythona z Pillow.
- `npm run capture-test` - wbudowane sprawdzenie ukrywania (wynik w JSON).
- Zmienna `POLYMATH_VISIBLE=1` wyłącza ukrywanie w trybie deweloperskim, do robienia zrzutów interfejsu. W zbudowanym programie nie ma żadnego efektu.

Struktura:

- `src/main` - proces główny: okna, skróty, model, rozpoznawanie mowy, Listen, Watch;
- `src/renderer` - pasek i okno ustawień, przechwytywanie dźwięku systemowego;
- `src/shared` - kod wspólny: detektor fraz, WAV, analiza tekstu, SSE, tłumaczenia interfejsu;
- `scripts` - instalacja whisper.cpp i Parakeet oraz sprawdzenie ukrywania;
- `tests` - testy.
