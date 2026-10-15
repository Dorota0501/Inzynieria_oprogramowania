---
layout: default
title: "Spotkanie 1. Dokumentacja techniczna (RFI i RFP)"
---

# Spotkanie 1. Dokumentacja techniczna (RFI i RFP)

| ⏱ Czas | 🎓 Efekt | 📝 Do oddania |
|---|---|---|
| ok. 80 min | Opis problemu, zakres, RFI i RFP | Rozdział 1 + RFI i RFP jako załączniki |

## 🎯 Cele spotkania

Po zajęciach potrafisz:

- wyjaśnić, czym jest dokumentacja techniczna w cyklu życia oprogramowania i jakie dokumenty powstają na wczesnym etapie projektu,
- odróżnić RFI od RFP i wiedzieć, kiedy stosuje się każdy z nich,
- opisać problem biznesowy, interesariuszy i zakres systemu,
- przygotować RFI i RFP dla własnego systemu.

## 📖 1. Wprowadzenie teoretyczne (ok. 20 min)

**Dokumentacja techniczna** to uporządkowany zbiór dokumentów opisujących potrzeby, wymagania, projekt, sposób testowania i eksploatacji systemu. Wczesne dokumenty (RFI, RFP) służą do tego, by zamawiający i wykonawca rozumieli problem w ten sam sposób, zanim powstanie jedna linijka kodu.

**RFI (Request for Information, zapytanie o informację)** to dokument wysyłany do potencjalnych dostawców, gdy zamawiający dopiero rozpoznaje rynek. Pyta o możliwe technologie, rozwiązania, orientacyjne koszty i doświadczenie dostawcy. Nie prowadzi jeszcze do zawarcia umowy.

**RFP (Request for Proposal, zapytanie ofertowe)** to dokument, w którym zamawiający szczegółowo opisuje potrzebę, wymagania, ograniczenia i kryteria oceny, a dostawcy odpowiadają konkretną ofertą (rozwiązanie, harmonogram, cena).

| Cecha | RFI | RFP |
|---|---|---|
| Cel | rozpoznanie rynku i możliwości | wybór wykonawcy i rozwiązania |
| Poziom szczegółowości | ogólny | szczegółowy |
| Oczekiwana odpowiedź | informacje, opis możliwości | oferta: rozwiązanie, termin, koszt |
| Zobowiązanie | brak | oferta stanowi podstawę umowy |
| Kolejność w procesie | pierwszy | po RFI |

<details markdown="1">
<summary><b>Typowa struktura RFI</b> (kliknij, aby rozwinąć)</summary>

1. Informacje o zamawiającym i kontekst biznesowy
2. Opis problemu i celu
3. Wstępny zakres systemu
4. Pytania do dostawców (technologie, doświadczenie, orientacyjny koszt i czas)
5. Termin i forma odpowiedzi

</details>

<details markdown="1">
<summary><b>Typowa struktura RFP</b> (kliknij, aby rozwinąć)</summary>

1. Streszczenie i cel projektu
2. Opis organizacji zamawiającej i interesariuszy
3. Zakres projektu (w zakresie / poza zakresem)
4. Wymagania wstępne: funkcjonalne, niefunkcjonalne, ograniczenia (technologiczne, prawne, budżetowe)
5. Oczekiwane rezultaty (deliverables) i harmonogram z kamieniami milowymi
6. Wymagania wobec oferty (co ma zawierać odpowiedź)
7. Kryteria oceny ofert wraz z wagami
8. Warunki formalne i terminy

</details>

## 🛠 2. Zadania na zajęciach (ok. 60 min)

| # | Zadanie | Czas |
|---|---|:---:|
| **1.1** | **Wybór systemu.** Wybierz system, który będziesz analizować i projektować przez cały semestr. Powinien dać się opisać min. 10 wymaganiami funkcjonalnymi, 3 aktorami i 6–8 klasami, ale być na tyle prosty, by zmieścić się w semestrze. Najlepiej, by był zbieżny z planowanym tematem pracy. Temat uzgodnij z prowadzącą. | 10 min |
| **1.2** | **Analiza kontekstu.** Opisz w 5–8 zdaniach: kim jest zamawiający, jaki problem rozwiązuje system, kto z niego korzysta. Wypisz interesariuszy (użytkownicy, administratorzy, zamawiający, systemy zewnętrzne) i krótko określ ich oczekiwania. | 15 min |
| **1.3** | **RFI (1–2 strony).** Przygotuj dokument według struktury powyżej. Sformułuj co najmniej 6 pytań do dostawców. | 15 min |
| **1.4** | **Szkic RFP.** Streszczenie, zakres (w zakresie / poza zakresem), min. 8 wstępnych wymagań, ograniczenia, harmonogram z min. 4 kamieniami milowymi, kryteria oceny ofert z wagami sumującymi się do 100%. | 20 min |

<details markdown="1">
<summary><b>Szablon dokumentu</b> (kliknij, aby rozwinąć)</summary>

```text
Tytuł systemu: ...
Zamawiający: ...
Problem biznesowy: ...
Cel systemu: ...
Interesariusze: ...
W zakresie: ...
Poza zakresem: ...
Ograniczenia (technologiczne, prawne, budżet, czas): ...
Oczekiwane rezultaty: ...
Kryteria oceny: (kryterium – waga %)
```

</details>

## 📝 3. Fragment pracy inżynierskiej do oddania

Na podstawie zadań przygotuj tekst **Rozdziału 1: Wprowadzenie** (1,5–3 strony):

- **1.1** Motywacja i opis problemu
- **1.2** Cel i zakres pracy (w zakresie / poza zakresem)
- **1.3** Interesariusze
- **1.4** Przegląd istniejących rozwiązań (min. 2–3 systemy konkurencyjne lub podobne, z krótkim porównaniem)
- **1.5** Układ pracy (po jednym zdaniu o każdym rozdziale)

RFI i RFP dołącz jako załączniki (Załącznik A i B).

## ✅ 4. Kryteria oceny

| Element | Co oceniamy |
|---|---|
| RFI | kompletność struktury, jakość pytań do dostawców |
| RFP | jasny zakres, mierzalne wymagania, sensowne kryteria oceny |
| Rozdział 1 | spójność celu z zakresem, przegląd istniejących rozwiązań, język i poprawność edytorska |
| Repozytorium | czytelna struktura katalogów, historia commitów |

**💡 Wskazówka:** załóż repozytorium od razu, np. ze strukturą `docs/01-wprowadzenie`, `docs/02-wymagania`, `docs/03-projekt`, `docs/04-testy`, `docs/zalaczniki`, `src`, `README.md`.

## ☑️ 5. Lista kontrolna

- [ ] Wybrany system i temat uzgodnione z prowadzącą
- [ ] Opisany problem i interesariusze
- [ ] RFI zawiera min. 6 pytań do dostawców
- [ ] RFP zawiera zakres, ograniczenia, harmonogram i kryteria z wagami
- [ ] Rozdział 1 zawiera przegląd min. 2 istniejących rozwiązań
- [ ] Repozytorium utworzone

<details markdown="1">
<summary><b>❓ Pytania kontrolne (na kolokwium)</b></summary>

1. Czym różni się RFI od RFP? Kiedy stosuje się każdy z nich?
2. Kim są interesariusze i dlaczego ich identyfikacja jest ważna?
3. Co powinno znaleźć się w zakresie, a co poza zakresem projektu?
4. Jakie kryteria oceny ofert można zastosować w RFP i jak dobrać wagi?
5. Jakie dokumenty tworzy się na wczesnym etapie procesu wytwarzania oprogramowania?

</details>

---

**Dalej:** [Spotkanie 2. Wymagania i diagram przypadków użycia](spotkanie-02.md) · [Strona główna](../)
