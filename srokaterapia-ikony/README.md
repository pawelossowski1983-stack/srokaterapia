# srokaterapia.pl – paczka favicon i ikon

Źródło: Figma „srokaterapia.pl – identyfikacja wizualna”, komponent `Favicon/1 Pióro`.

## Pliki

| Plik | Rozmiar | Do czego |
|---|---|---|
| `favicon.ico` | 16/32/48 px | Starsze przeglądarki, Windows |
| `favicon.svg` | wektor | Nowoczesne przeglądarki (ostry na każdym ekranie) |
| `favicon-16.png`, `favicon-32.png` | 16, 32 px | Fallback PNG |
| `apple-touch-icon.png` | 180 px | iPhone/iPad – „Dodaj do ekranu początkowego” (iOS sam zaokrągla rogi) |
| `icon-192.png`, `icon-512.png` | 192, 512 px | Android, manifest |
| `icon-maskable-512.png` | 512 px | Android – ikona przycinana do kształtu systemu (znak w strefie bezpiecznej) |
| `site.webmanifest` | – | Nazwa, kolory i ikony strony |
| `znak-pioro.svg` | wektor | Sam znak (np. do stopki, wizytówek) |

## Wdrożenie w web360

1. Wgraj wszystkie pliki do **katalogu głównego** serwisu (tak, by były dostępne jako `https://srokaterapia.pl/favicon.ico` itd.).
2. W szablonie strony, w sekcji `<head>`, wklej:

```html
<link rel="icon" href="/favicon.ico" sizes="48x48">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png">
<link rel="manifest" href="/site.webmanifest">
<meta name="theme-color" content="#1E2A32">
```

3. Sprawdź: otwórz stronę w trybie prywatnym (przeglądarki mocno cache'ują favicony).

## Eksport logotypów z Figmy (do zrobienia przez zespół)

Strona **03 Logo – wersja finalna**, komponenty na dole strony:

- `Logo/Poziome`, `Logo/Poziome – negatyw`, `Logo/Pionowe`, `Logo/Pionowe – negatyw`
- Zaznacz komponent → panel **Export** → dodaj: **SVG** (opcja „Outline text” włączona), **PNG 2x**, **PNG 4x** → **Export**.
- Na stronę WWW używaj **SVG** (lekki i ostry), PNG do maili, dokumentów i social mediów.
