---
layout: default
title: Inżynieria oprogramowania – laboratorium
---

# 🧩 Inżynieria oprogramowania – laboratorium

Materiały dla studentów · Uniwersytet Rzeszowski, Instytut Informatyki

## 🎯 O co chodzi w tym laboratorium

Laboratorium obejmuje **7 spotkań**. Przez cały semestr pracujesz nad **jednym, własnym systemem informatycznym**, który może stać się tematem Twojej pracy inżynierskiej. Z każdego spotkania powstaje **gotowy fragment rozdziału pracy dyplomowej** (tekst + diagramy).

## 📅 Spotkania

| Spotkanie | Temat | Powstający fragment pracy inżynierskiej |
|:---:|---|---|
| **1** | [Dokumentacja techniczna: RFI i RFP](docs/spotkanie-01.md) | Rozdział 1: Wprowadzenie, cel i zakres pracy, analiza potrzeb |
| **2** | [Wymagania i diagram przypadków użycia](docs/spotkanie-02.md) | Rozdział 2: Specyfikacja wymagań |
| 3 | Struktura klas, diagram klas *(wkrótce)* | Rozdział 3: Projekt – model statyczny |
| 4 | Diagramy komponentów i pakietów *(wkrótce)* | Rozdział 3: Projekt – architektura |
| 5 | Diagramy sekwencji i aktywności *(wkrótce)* | Rozdział 4: Projekt – model dynamiczny i procesy |
| 6 | Projektowanie testów automatycznych *(wkrótce)* | Rozdział 5: Plan i scenariusze testów |
| 7 | Dokumentacja, automatyzacja dokumentacji i wytwarzania (CI/CD) *(wkrótce)* | Rozdział 6: Dokumentacja techniczna i proces wytwórczy |

## ⚙️ Zasady pracy

- Wszystkie pliki trzymasz **we własnym repozytorium Git** (GitHub/GitLab).
- Tekst piszesz w **Markdown**, a diagramy w **PlantUML** lub w narzędziu z eksportem do PNG/SVG. Dzięki temu na spotkaniach 6–7 zautomatyzujemy budowanie dokumentacji.
- Po każdym spotkaniu oddajesz fragment pracy (rozdział) oraz pliki źródłowe diagramów.

**Proponowana struktura repozytorium studenta:**

```text
/docs
  /01-wprowadzenie
  /02-wymagania
  /03-projekt
  /04-testy
  /zalaczniki
/src
README.md
```
