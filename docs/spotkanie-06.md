---
layout: default
title: "Spotkanie 6. Dokumentacja techniczna i automatyzacja"
---

# Spotkanie 6. Dokumentacja techniczna i automatyzacja

| Czas | Zakres | Wynik pracy |
|---|---|---|
| ok. 85 min | Dokumentacja techniczna systemu, automatyzacja dokumentacji, automatyzacja wytwarzania (CI) | Struktura dokumentacji, README, automatyczne budowanie dokumentacji, działający potok CI |

## Cele spotkania

Po zajęciach student potrafi:

- wskazać rodzaje dokumentacji technicznej systemu i ich odbiorców,
- zaprojektować strukturę dokumentacji własnego systemu na podstawie artefaktów ze spotkań 1–5,
- wyjaśnić ideę „dokumentacji jako kodu” i uruchomić automatyczne budowanie dokumentacji,
- wyjaśnić pojęcia ciągłej integracji i ciągłego dostarczania (CI/CD),
- skonfigurować prosty potok, który uruchamia testy i buduje dokumentację przy każdej zmianie w repozytorium.

Spotkanie ma charakter praktyczny: automatyzacja jest realizowana na gotowych szablonach dostosowywanych do technologii własnego systemu.

## 1. Wprowadzenie teoretyczne (ok. 20 min)

### Dokumentacja techniczna systemu

Dokumentacja techniczna jest zbiorem dokumentów opisujących system w sposób umożliwiający jego zrozumienie, utrzymanie i rozwój. Rodzaje różnią się odbiorcą:

| Rodzaj | Odbiorca | Typowa zawartość |
|---|---|---|
| Dokumentacja dla deweloperów | programiści | architektura, model klas, opis modułów, API, instrukcja uruchomienia (README), konwencje |
| Dokumentacja dla administratora | osoby wdrażające i utrzymujące | wymagania środowiska, instalacja, konfiguracja, kopie zapasowe |
| Dokumentacja dla użytkownika | użytkownicy końcowi | instrukcja obsługi, opis funkcji |
| Dokumentacja decyzji | zespół i przyszli twórcy | uzasadnienia wyborów (np. zapisy decyzji architektonicznych, ADR) |

**Przykładowa struktura dokumentacji technicznej systemu**, zbudowana z artefaktów z poprzednich spotkań:

1. Cel, zakres i kontekst systemu (spotkanie 1)
2. Wymagania i przypadki użycia (spotkanie 2)
3. Architektura: komponenty, pakiety (spotkania 3–4)
4. Model danych i klas (spotkanie 3)
5. Kluczowe scenariusze i procesy (spotkania 4–5)
6. Strategia i przypadki testowe (spotkanie 5)
7. Instrukcja instalacji i uruchomienia
8. Ograniczenia i kierunki rozwoju

**Cechy dobrej dokumentacji:** aktualna, przechowywana blisko kodu, wersjonowana razem z kodem, pisana dla konkretnego odbiorcy, bez powielania tej samej informacji w wielu miejscach.

### Automatyzacja dokumentacji (dokumentacja jako kod)

Dokumentacja jako kod oznacza traktowanie dokumentów jak kodu źródłowego: tekst w formacie Markdown, diagramy w postaci kodu (PlantUML, Mermaid), przechowywanie w repozytorium, przegląd zmian i automatyczne generowanie wersji do odczytu (strona WWW, PDF). Elementy:

- **format źródłowy:** Markdown i diagramy tekstowe, dzięki którym zmiany są widoczne w historii repozytorium,
- **generatory stron dokumentacji:** np. MkDocs, Sphinx, Jekyll (z tego narzędzia korzysta strona z tymi materiałami),
- **dokumentacja z kodu:** komentarze w kodzie przekształcane w dokumentację (np. Javadoc, Doxygen, docstringi w Sphinx),
- **automatyczne budowanie:** dokumentacja przebudowuje się przy każdej zmianie w repozytorium.

### Automatyzacja wytwarzania oprogramowania (CI/CD)

**Ciągła integracja (CI)** polega na automatycznym budowaniu i testowaniu zmian w kodzie przy każdym wprowadzeniu zmiany do repozytorium. **Ciągłe dostarczanie (CD)** rozszerza to o automatyczne przygotowanie (lub wdrożenie) gotowej wersji. Korzyści: szybkie wykrywanie błędów, powtarzalność, brak ręcznych kroków.

Podstawowe pojęcia potoku (na przykładzie GitHub Actions):

| Pojęcie | Znaczenie |
|---|---|
| Wyzwalacz (trigger) | zdarzenie uruchamiające potok, np. wysłanie zmian lub pull request |
| Zadanie (job) | zestaw kroków wykonywanych na jednej maszynie |
| Krok (step) | pojedyncza komenda lub gotowa akcja |
| Artefakt | wynik zadania, np. zbudowana dokumentacja |

Dodatkowe praktyki wspierające automatyzację: kontrola wersji z gałęziami i pull requestami, analiza statyczna kodu, automatyczne sprawdzanie stylu.

<details markdown="1" open>
<summary><b>Przykład potoku CI: testy i budowanie dokumentacji (GitHub Actions)</b></summary>

Plik `.github/workflows/ci.yml`:

```yaml
name: ci
on:
  push:
    branches: [main]
  pull_request:

jobs:
  testy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
      - run: pip install -r requirements.txt
      - run: pytest

  dokumentacja:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
      - run: pip install mkdocs
      - run: mkdocs build --strict
```

Minimalny plik `mkdocs.yml`:

```yaml
site_name: Dokumentacja systemu
nav:
  - Wprowadzenie: index.md
  - Wymagania: wymagania.md
  - Architektura: architektura.md
```

Szablon wymaga dostosowania do technologii systemu (np. Maven lub Gradle dla Javy, npm dla JavaScriptu). Numery wersji akcji (`checkout`, `setup-python`) oraz języka należy sprawdzić w ich aktualnej dokumentacji.

</details>

## 2. Zadania na zajęciach (ok. 65 min)

| # | Zadanie | Czas |
|---|---|:---:|
| **6.1** | **Struktura dokumentacji.** Spis treści dokumentacji technicznej własnego systemu, z przypisaniem każdej sekcji do istniejącego artefaktu (spotkania 1–5) lub zaznaczeniem braku. | 10 min |
| **6.2** | **README projektu.** Opis systemu, wymagania środowiska, instrukcja instalacji i uruchomienia, struktura repozytorium, sposób uruchamiania testów. | 10 min |
| **6.3** | **Dokumentacja jako kod.** Konfiguracja generatora dokumentacji (np. MkDocs) dla katalogu `docs` i uruchomienie lokalnego budowania. | 15 min |
| **6.4** | **Potok CI.** Dostosowanie szablonu do technologii systemu: uruchamianie testów z spotkania 5 oraz budowanie dokumentacji przy każdej zmianie w gałęzi głównej i pull requestach. | 20 min |
| **6.5** | **Weryfikacja.** Wysłanie zmiany do repozytorium, odczyt wyniku potoku (powodzenie lub błąd) i naprawa ewentualnych błędów. Wyjaśnienie, który krok zawiódł i dlaczego, jeśli potok zakończył się niepowodzeniem. | 10 min |

## 3. Wykorzystanie w pracy inżynierskiej

Pełna dokumentacja techniczna z zajęć zwykle nie jest treścią pracy dyplomowej. Pozostaje w repozytorium, a w pracy znajduje się odwołanie do niej oraz wybrane elementy.

| Artefakt z zajęć | Możliwe wykorzystanie w pracy | Kiedy pominąć lub skrócić |
|---|---|---|
| Struktura dokumentacji | Pomocna jako szkielet rozdziałów projektowych | Układ pracy wynika z wymagań wydziału |
| README i instrukcja uruchomienia | Załącznik (instrukcja instalacji i uruchomienia) oraz odnośnik do repozytorium | Praca bez części implementacyjnej |
| Opis potoku CI | Krótki opis procesu wytwórczego i weryfikacji (kilka zdań lub diagram), jeśli jest istotny dla tematu | Gdy praca nie dotyczy procesu wytwórczego: pominąć |
| Dokumentacja jako kod | Wspomnienie jako narzędzie, bez opisu konfiguracji | Zwykle pomijane w treści |

## 4. Przedmiot oceny

| Element | Co jest oceniane |
|---|---|
| Struktura dokumentacji | kompletność, powiązanie z artefaktami z poprzednich spotkań |
| README | czytelność, możliwość uruchomienia systemu na podstawie instrukcji |
| Dokumentacja jako kod | poprawna konfiguracja generatora, działające budowanie |
| Potok CI | poprawność konfiguracji, uruchamianie testów i budowanie dokumentacji |
| Weryfikacja | umiejętność odczytania wyniku i naprawy błędu potoku |

## 5. Kryteria kompletności wyniku

- Spis treści dokumentacji obejmuje architekturę, wymagania, testy i instrukcję uruchomienia.
- README pozwala osobie z zewnątrz uruchomić system i testy.
- Dokumentacja buduje się lokalnie bez błędów.
- Plik potoku znajduje się w repozytorium, a ostatnie uruchomienie zakończyło się powodzeniem.
- Potok uruchamia testy i buduje dokumentację przy każdej zmianie w gałęzi głównej.

## 6. Częste błędy

- Dokumentacja pisana jednorazowo na koniec i szybko się dezaktualizująca.
- Powielanie tych samych informacji w wielu plikach.
- Instrukcja uruchomienia pomijająca zależności lub wymagane wersje.
- Potok CI uruchamiający testy, które nie przechodzą lokalnie.
- Dane poufne (hasła, klucze) zapisane w plikach potoku lub w repozytorium.
- Ręczne kroki, które mogły zostać zautomatyzowane, a przez to powodują rozbieżności.

<details markdown="1">
<summary><b>Pytania kontrolne (kolokwium)</b> (sekcja zwijana)</summary>

1. Jakie rodzaje dokumentacji technicznej wyróżnia się i kto jest ich odbiorcą?
2. Jakie elementy powinna zawierać dokumentacja techniczna systemu?
3. Na czym polega idea „dokumentacji jako kodu”? Jakie daje korzyści?
4. Czym różni się ciągła integracja od ciągłego dostarczania?
5. Jakie są podstawowe elementy potoku CI (wyzwalacz, zadanie, krok)?
6. Jakie zadania warto automatyzować w procesie wytwarzania oprogramowania?
7. Dlaczego dane poufne nie powinny być przechowywane w repozytorium?

</details>

## Literatura

- I. Sommerville, *Inżynieria oprogramowania*, PWN (dokumentacja, zarządzanie konfiguracją).
- Dokumentacja GitHub Actions: [docs.github.com/actions](https://docs.github.com/actions)
- Dokumentacja MkDocs: [mkdocs.org](https://www.mkdocs.org)
- Dokumentacja Jekyll i GitHub Pages: [docs.github.com/pages](https://docs.github.com/pages)

---

**Wstecz:** [Spotkanie 5](spotkanie-05.md) · **Dalej:** [Spotkanie 7. Kolokwium zaliczeniowe](spotkanie-07.md) · [Strona główna](../)
