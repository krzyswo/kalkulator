<div align="center">

<img src="docs/readme-hero.svg" alt="Kalkulator Zarobków — licznik wynagrodzenia działający lokalnie w przeglądarce" width="100%">

<br>

[![Live application](https://img.shields.io/badge/URUCHOM_APLIKACJĘ-Open-59e0c1?style=for-the-badge&logo=githubpages&logoColor=07111f)](https://krzyswo.github.io/kalkulator/)
[![Deploy GitHub Pages](https://img.shields.io/github/actions/workflow/status/krzyswo/kalkulator/pages.yml?branch=main&style=for-the-badge&label=GitHub%20Pages)](https://github.com/krzyswo/kalkulator/actions/workflows/pages.yml)
[![MIT License](https://img.shields.io/badge/License-MIT-57a8ff?style=for-the-badge)](LICENSE)
[![Static app](https://img.shields.io/badge/Stack-HTML_CSS_JS-f59e0b?style=for-the-badge&logo=javascript&logoColor=111827)](docs/app.html)

**Prosty licznik zarobków działający w całości w przeglądarce.**

[Uruchom aplikację](https://krzyswo.github.io/kalkulator/app.html) · [Zobacz funkcje](#funkcje) · [Jak działa obliczenie](#jak-działa-obliczenie) · [Prywatność](#prywatność)

</div>

---

## Do czego służy

Kalkulator Zarobków pokazuje na bieżąco szacowaną kwotę zarobioną podczas bieżącej sesji pracy. Możesz użyć miesięcznego wynagrodzenia albo stawki godzinowej, zapisać opis sesji, zachować historię w przeglądarce i wyeksportować dane do CSV.

Aplikacja nie wymaga konta, serwera ani instalacji. Wszystkie obliczenia odbywają się lokalnie na urządzeniu.

## Funkcje

- licznik dla miesięcznego wynagrodzenia,
- licznik dla stawki godzinowej,
- rozpoczęcie sesji od bieżącej lub wcześniej wybranej godziny,
- zapis aktywnego licznika po odświeżeniu strony,
- historia sesji przechowywana w `localStorage`,
- opis wykonanej pracy,
- suma zapisanych zarobków,
- usuwanie pojedynczych wpisów i czyszczenie historii,
- eksport historii do pliku CSV,
- responsywny interfejs na komputerze i telefonie,
- brak zewnętrznych bibliotek i usług śledzących.

## Jak działa obliczenie

### Wynagrodzenie miesięczne

Aplikacja przyjmuje uproszczone założenie **160 godzin pracy w miesiącu**:

```text
stawka za sekundę = wynagrodzenie miesięczne / 160 / 3600
zarobiona kwota = stawka za sekundę × czas sesji
```

### Stawka godzinowa

```text
stawka za sekundę = stawka godzinowa / 3600
zarobiona kwota = stawka za sekundę × czas sesji
```

> [!IMPORTANT]
> Wynik jest szacunkiem czasu i wartości pracy. Aplikacja nie oblicza podatków, składek, kosztów pracodawcy, nadgodzin ani zasad konkretnej umowy.

## Uruchomienie

Najprościej otworzyć gotową wersję:

**https://krzyswo.github.io/kalkulator/app.html**

Lokalnie:

```bash
git clone https://github.com/krzyswo/kalkulator.git
cd kalkulator
```

Następnie otwórz `docs/app.html` w przeglądarce. Możesz też uruchomić prosty serwer:

```bash
python -m http.server 8000 --directory docs
```

Strona będzie dostępna pod adresem `http://localhost:8000`.

## Prywatność

- Dane pozostają w pamięci przeglądarki na używanym urządzeniu.
- Repozytorium nie zawiera backendu, logowania ani analityki.
- Eksport CSV powstaje lokalnie.
- Wyczyszczenie danych strony w przeglądarce usuwa zapisaną historię.

## Struktura projektu

```text
docs/
├── index.html          # strona otwierająca
├── app.html            # kalkulator
├── favicon.svg
├── social-card.svg
└── readme-hero.svg
.github/workflows/
└── pages.yml           # wdrożenie GitHub Pages
```

## Rozwój

Projekt jest celowo prosty i nie wymaga procesu budowania. Zmiany w plikach `docs/` są publikowane przez GitHub Actions.

Przed wysłaniem zmiany sprawdź:

1. uruchamianie i zatrzymywanie obu trybów,
2. przywrócenie aktywnej sesji po odświeżeniu,
3. dodawanie i usuwanie wpisów historii,
4. eksport CSV,
5. widok mobilny.

## Licencja

Projekt jest dostępny na licencji [MIT](LICENSE).

---

<div align="center">

### Policz wartość bieżącej sesji pracy

[![Open live app](https://img.shields.io/badge/OTWÓRZ_KALKULATOR-59e0c1?style=for-the-badge&logo=githubpages&logoColor=07111f)](https://krzyswo.github.io/kalkulator/app.html)
[![Browse source](https://img.shields.io/badge/ZOBACZ_KOD-57a8ff?style=for-the-badge&logo=github&logoColor=white)](https://github.com/krzyswo/kalkulator)

</div>
