---
layout: default
title: "Spotkanie 7. Kolokwium zaliczeniowe"
---

# Spotkanie 7. Kolokwium zaliczeniowe

| Zakres | Forma | Wynik |
|---|---|---|
| Materiał spotkań 1–6 | Część teoretyczna i część praktyczna | Zaliczenie laboratorium |

## 1. Zakres kolokwium

Kolokwium obejmuje materiał spotkań 1–6, w zakresie wskazanym poniżej.

| Spotkanie | Zagadnienia |
|:---:|---|
| 1 | system informatyczny, funkcjonalność, aktor, interesariusz, zakres; dokumentacja techniczna; różnice między RFI i RFP, ich struktura i zastosowanie |
| 2 | wymagania funkcjonalne i niefunkcjonalne, cechy dobrego wymagania, priorytetyzacja MoSCoW, kryteria akceptacji; diagram przypadków użycia (aktor, include, extend, granica systemu); scenariusze; macierz śledzenia |
| 3 | analiza struktury klas z opisu scenariuszy; diagram klas (relacje, krotności, widoczność); diagram pakietów i zasady podziału |
| 4 | diagram komponentów (interfejsy dostarczane i wymagane); diagram sekwencji (komunikaty, fragmenty alt, opt, loop); spójność modeli |
| 5 | diagram aktywności (decyzje, tory, fork/join); poziomy testowania; projektowanie przypadków testowych (klasy równoważności, wartości brzegowe); struktura testu automatycznego |
| 6 | rodzaje dokumentacji technicznej; dokumentacja jako kod; CI/CD, elementy potoku |

## 2. Forma i punktacja

| Część | Charakter | Punkty |
|---|---|:---:|
| A. Teoretyczna | pytania zamknięte i krótkie pytania otwarte: definicje, rozróżnienia, notacja | 40 |
| B. Praktyczna | zadanie na krótkim opisie systemu: wykonanie wybranych fragmentów modelu i przypadków testowych | 60 |

Wynik końcowy z laboratorium wynika z kolokwium oraz z artefaktów oddawanych na spotkaniach 1–6. Proporcje, próg zaliczenia i skala ocen są podawane przez osobę prowadzącą zajęcia.

## 3. Przykładowe pytania części A

1. Czym jest funkcjonalność i czym różni się od wymagania niefunkcjonalnego?
2. Czym różni się aktor od interesariusza? Czy baza danych jest aktorem?
3. Czym różni się RFI od RFP? W jakich pracach dyplomowych są zasadne?
4. Przeformułować wymaganie „System ma być szybki” tak, aby było weryfikowalne.
5. Kiedy stosuje się relację `include`, a kiedy `extend`?
6. Czym różni się kompozycja od agregacji? Podać przykład.
7. Czym różni się komponent od pakietu i od klasy?
8. Do czego służą fragmenty `alt`, `opt` i `loop` w diagramie sekwencji?
9. Jak ścieżki diagramu aktywności wykorzystuje się do projektowania testów?
10. Wskazać klasy równoważności i wartości brzegowe dla pola „wiek” z dopuszczalnym zakresem 18–65.
11. Czym różni się ciągła integracja od ciągłego dostarczania?
12. Na czym polega idea dokumentacji jako kodu?

## 4. Przykładowe zadanie części B

**Opis systemu.** Uczelniany system rezerwacji sal dydaktycznych. Pracownicy dydaktyczni zgłaszają rezerwacje sal na wybrane terminy. Każda sala ma pojemność i wyposażenie (np. projektor, komputery). System nie dopuszcza kolizji terminów. Rezerwacje wymagają zatwierdzenia przez administratora sal, a po decyzji system wysyła powiadomienie e-mail do zgłaszającego. Administrator zarządza listą sal i może anulować rezerwację.

**Polecenia (zakres do dostosowania w danym terminie):**

1. Zapisać 3 wymagania funkcjonalne i 2 niefunkcjonalne w formie tabeli (ID, opis, priorytet, kryterium akceptacji).
2. Sporządzić diagram przypadków użycia z aktorami i co najmniej jedną relacją `include` lub `extend`.
3. Zaprojektować fragment diagramu klas (min. 4 klasy) z relacjami i krotnościami.
4. Narysować diagram sekwencji lub diagram aktywności dla zgłoszenia i zatwierdzenia rezerwacji, z uwzględnieniem odrzucenia.
5. Zapisać 4 przypadki testowe (w tym przypadek negatywny i przypadek z wartością brzegową).

**Kryteria oceny części B:**

| Element | Co jest oceniane |
|---|---|
| Wymagania | jednoznaczność, weryfikowalność, kryteria akceptacji |
| Diagram przypadków użycia | poprawność notacji, poziom ogólności przypadków |
| Diagram klas | trafne klasy, poprawne relacje i krotności |
| Diagram sekwencji lub aktywności | poprawność notacji, ścieżki alternatywne |
| Przypadki testowe | kompletność opisu, różnorodność (pozytywne i negatywne), powiązanie z wymaganiem |

## 5. Podsumowanie: artefakty z laboratorium a praca inżynierska

Artefakty z laboratorium są pełnym, roboczym zapleczem projektowym. Do pracy dyplomowej trafia ich selekcja, zależna od tematu i uzgodniona z promotorem. Poniższe zestawienie ma charakter orientacyjny.

| Artefakt | Typowe wykorzystanie | Zwykle pomijane lub przenoszone do załącznika |
|---|---|---|
| Opis problemu, cel, zakres | wstęp pracy | – |
| Wykaz funkcjonalności i aktorów | opis zakresu systemu | – |
| RFI i RFP | tylko przy konkretnym zamawiającym lub wyborze dostawcy | w pozostałych pracach |
| Wymagania | kluczowe w treści | pełna tabela w załączniku |
| Diagram przypadków użycia | jeden diagram ogólny | diagramy szczegółowe |
| Diagram klas | wersja uproszczona | pełny diagram |
| Diagram pakietów i komponentów | opis architektury | przy małym systemie |
| Diagramy sekwencji i aktywności | 1–3 najważniejsze | pozostałe |
| Plan i przypadki testowe | strategia i wybrane przypadki | pełna tabela |
| README, instrukcja uruchomienia | załącznik i odnośnik do repozytorium | – |
| Potok CI, dokumentacja jako kod | krótka wzmianka | opis konfiguracji |

---

**Wstecz:** [Spotkanie 6. Dokumentacja techniczna i automatyzacja](spotkanie-06.md) · [Strona główna](../)
