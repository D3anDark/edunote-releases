<p align="center">
  <img src="icon.png" width="96" alt="">
</p>

<h1 align="center">EduNote</h1>

<p align="center">
  Notatki do nauki na tablet z rysikiem i na komputer: pismo odręczne na stronach A4, Markdown na żywo,
  czytnik PDF obok notatki, fiszki i asystent AI.
</p>

<p align="center">
  <a href="https://github.com/D3anDark/edunote-releases/releases/latest"><img src="https://img.shields.io/github/v/release/D3anDark/edunote-releases?label=wersja" alt="Najnowsza wersja"></a>
  <a href="https://github.com/D3anDark/edunote-releases/releases"><img src="https://img.shields.io/github/downloads/D3anDark/edunote-releases/total?label=pobrania" alt="Pobrania"></a>
</p>

<p align="center"><a href="README.md">English</a> · <b>Polski</b></p>

## Pobierz

| System | Plik | |
|---|---|---|
| Android (większość telefonów i tabletów) | `app-arm64-v8a-release.apk` | [Pobierz](https://github.com/D3anDark/edunote-releases/releases/latest/download/app-arm64-v8a-release.apk) |
| Android (starsze urządzenia 32-bitowe) | `app-armeabi-v7a-release.apk` | [Pobierz](https://github.com/D3anDark/edunote-releases/releases/latest/download/app-armeabi-v7a-release.apk) |
| Android (x86_64, emulator) | `app-x86_64-release.apk` | [Pobierz](https://github.com/D3anDark/edunote-releases/releases/latest/download/app-x86_64-release.apk) |
| Linux (x86_64) | `EduNote-x86_64.AppImage` | [Pobierz](https://github.com/D3anDark/edunote-releases/releases/latest/download/EduNote-x86_64.AppImage) |
| Windows (x64) | `EduNote-windows-x64.zip` | [Pobierz](https://github.com/D3anDark/edunote-releases/releases/latest/download/EduNote-windows-x64.zip) |
| macOS | `EduNote-macos.zip` | [Pobierz (1.1.0)](https://github.com/D3anDark/edunote-releases/releases/download/v1.1.0/EduNote-macos.zip) |

Wszystkie wersje, z opisem zmian, są na [stronie wydań](https://github.com/D3anDark/edunote-releases/releases).

## Instalacja

**Android.** Otwórz plik APK i pozwól przeglądarce albo menedżerowi plików instalować aplikacje, gdy Android o to
zapyta.

**Linux.** Nadaj plikowi prawo uruchamiania i uruchom go:

```sh
chmod +x EduNote-x86_64.AppImage
./EduNote-x86_64.AppImage
```

Jeśli się nie uruchamia, dodaj `--appimage-extract-and-run`.

**Windows.** Rozpakuj folder w dowolnym miejscu i uruchom `edunote.exe`. Aplikacja nie jest podpisana, więc SmartScreen
może ostrzec: wybierz *Więcej informacji*, potem *Uruchom mimo to*.

**macOS.** Rozpakuj i przenieś `edunote.app` do *Aplikacji*. Aplikacja nie jest podpisana: jeśli macOS ją zablokuje,
otwórz *Ustawienia systemowe*, *Prywatność i ochrona*, i wybierz *Otwórz mimo to*.

Wersja na macOS to na razie 1.1.0: build 1.2.0 nie mógł pobrać ONNX Runtime z serwera Microsoftu. Następne wydanie
przyniesie aktualną wersję na macOS.

Wersje na Windows i macOS są budowane przy każdym wydaniu, ale nie były jeszcze sprawdzone na prawdziwym komputerze.

## Aktualizacje

Aplikacja przy starcie sprawdza tę stronę i proponuje nową wersję, gdy taka jest; *Ustawienia*, *Aktualizacje*
sprawdzają na żądanie. Na Androidzie pobiera APK i otwiera systemowy instalator, AppImage podmienia sam siebie i przy
następnym starcie uruchamia się nowa wersja. Na Windows (od wersji 1.2.0) pobiera zip i podmienia folder aplikacji po
zamknięciu EduNote; folder musi być zapisywalny, więc nie *Program Files*. macOS dostaje link tutaj. Notatki zostają
w każdym przypadku.

## Co potrafi

- **Notatki mieszane**: strony A4 z tekstem i pismem odręcznym razem. Pióro, zakreślacz, gumka i lasso; kartka czysta,
  w linie, w kratkę lub w kropki. Przytrzymana kreska prostuje się w odcinek, elipsę albo prostokąt. Import PDF jako
  podkład stron, eksport do PDF z prawdziwym tekstem i tuszem na wierzchu.
- **Notatki tekstowe**: Markdown widoczny od razu, jak w Obsidianie. Wzory LaTeX, tabele
  edytowane w miejscu, obrazy, listy zadań, prezentacja slajd po slajdzie i tryb czytania (Ctrl+E), w którym notatka
  wygląda jak gotowa strona. [Podgląd pliku Markdown](https://deandark.me/EduNote/#preview) na stronie pokazuje, jak
  EduNote wyświetli Twój plik. Skróty działają jak w innych edytorach: Tab i Shift+Tab przesuwają punkt listy o poziom,
  Ctrl+H szuka i zastępuje, Alt+strzałki w górę/dół przesuwają linie.
- **Otwórz za pomocą EduNote**: plik `.md` z menedżera plików otwiera się jako notatka, a otwarty ponownie wraca do tej
  samej notatki. Plik na dysku zostaje bez zmian.
- **Czytnik PDF obok notatki**: szukanie, zakreślenia w sześciu kolorach, cytaty z odsyłaczem do strony, numeracja
  z książki. Skany rozpoznaje wbudowany OCR (PaddleOCR), bez instalowania czegokolwiek.
- **Porządek**: foldery, przypinanie, `#tagi`, `[[linki]]` między notatkami, wyszukiwanie pełnotekstowe, kosz na 30 dni
  i szablony (wykład, metoda Cornella, sprawozdanie, konspekt lekcji, sprawdzian i inne).
- **Powtórki**: zadania z terminami zebrane ze wszystkich notatek, fiszki z linii `pytanie :: odpowiedź` i luk
  `{{tak}}` z powtórkami w odstępach, wszystkie zakreślenia na jednej liście.
- **Asystent AI**: przycisk na pasku notatki streszcza ją, robi z niej fiszki, tłumaczy prościej i odpytuje jak
  korepetytor, a każda notatka pamięta swoje rozmowy. Gemini, Claude albo dowolny serwer zgodny z OpenAI, także
  lokalny, jak Ollama i LM Studio, z Twoim kluczem. Nic nie jest wysyłane, dopóki go nie skonfigurujesz.

## Twoje dane

Notatki zostają na urządzeniu, w lokalnej bazie; aplikacja nie ma konta ani kopii w chmurze. Łączy się tylko z
dostawcą AI, którego ustawisz, i z tą stroną, żeby sprawdzić aktualizacje. Kopia zapasowa w pliku zip, codzienna kopia
w aplikacji i eksport do plików Markdown są w *Ustawieniach*.

Aplikacja jest po polsku i po angielsku: wybiera język systemu, a gdy go nie zna, angielski.

## Uwagi

Znalazłeś błąd albo czegoś brakuje? [Zgłoś to tutaj](https://github.com/D3anDark/edunote-releases/issues).
