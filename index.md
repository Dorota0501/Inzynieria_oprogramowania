---
layout: default
title: Inżynieria oprogramowania – laboratorium
---

# Inżynieria oprogramowania – laboratorium

Materiały dla studentów · Uniwersytet Rzeszowski, Instytut Informatyki

## O laboratorium

Laboratorium obejmuje 7 spotkań: sześć tematycznych i kolokwium zaliczeniowe na zakończenie. W trakcie semestru jeden, własny system informatyczny jest analizowany i projektowany kolejnymi technikami inżynierii oprogramowania. Powstające artefakty (opis systemu, wymagania, diagramy UML, testy, dokumentacja) mają wspierać pisanie pracy inżynierskiej. Do pracy trafia wybór zależny od jej tematu i charakteru, a pełna dokumentacja pozostaje w repozytorium lub w załącznikach.

## Spotkania

| Spotkanie | Temat | Materiał użyteczny w pracy inżynierskiej |
|:---:|---|---|
| **1** | [Dokumentacja techniczna: RFI i RFP](docs/spotkanie-01.md) | Opis problemu, cel i zakres systemu; RFI i RFP tylko tam, gdzie jest to zasadne |
| **2** | [Wymagania i diagram przypadków użycia](docs/spotkanie-02.md) | Wymagania kluczowe i diagram przypadków użycia; pełna specyfikacja jako załącznik |
| **3** | [Struktura klas: diagram klas i diagram pakietów](docs/spotkanie-03.md) | Model statyczny systemu |
| **4** | [Diagram komponentów i diagram sekwencji](docs/spotkanie-04.md) | Architektura systemu i kluczowe scenariusze działania |
| **5** | [Procesy biznesowe i projektowanie testów automatycznych](docs/spotkanie-05.md) | Opis procesów, plan i scenariusze testów |
| **6** | [Dokumentacja techniczna i automatyzacja](docs/spotkanie-06.md) | Dokumentacja techniczna, instrukcja uruchomienia, opis procesu wytwórczego |
| **7** | [Kolokwium zaliczeniowe](docs/spotkanie-07.md) | Podsumowanie i mapa artefaktów do wykorzystania w pracy |

Zakres i układ rozdziałów pracy dyplomowej wynikają z wymagań wydziału i ustaleń z promotorem. Materiały z zajęć mają ten proces wspierać, a nie narzucać strukturę pracy.

## Zasady pracy

- Wszystkie pliki są przechowywane we własnym repozytorium Git (GitHub/GitLab).
- Tekst jest pisany w formacie Markdown, a diagramy w PlantUML lub w narzędziu z eksportem do PNG/SVG. Dzięki temu na spotkaniu 6 możliwa jest automatyzacja budowania dokumentacji.
- Po każdym spotkaniu oddawane są artefakty wskazane w materiale danego spotkania oraz pliki źródłowe diagramów.
- Kolokwium zaliczeniowe na spotkaniu 7 obejmuje materiał spotkań 1–6.

**Proponowana struktura repozytorium:**

```text
/docs
  /01-opis-systemu
  /02-wymagania
  /03-projekt
  /04-testy
  /zalaczniki
/src
README.md
```
