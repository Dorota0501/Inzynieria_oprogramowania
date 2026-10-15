---
layout: default
title: "Spotkanie 1. Dokumentacja techniczna (RFI i RFP)"
---

# Spotkanie 1. Dokumentacja techniczna (RFI i RFP)

| Czas | Zakres | Wynik pracy |
|---|---|---|
| ok. 80 min | Opis systemu, wykaz funkcjonalności i aktorów, RFI i RFP | Karta systemu, wykaz funkcjonalności i aktorów, RFI i RFP (ćwiczenie) |

## Cele spotkania

Po zajęciach student potrafi:

- zdefiniować pojęcia: system informatyczny, funkcjonalność, aktor, interesariusz, zakres systemu,
- wyjaśnić, czym jest dokumentacja techniczna w cyklu życia oprogramowania i jakie dokumenty powstają na wczesnym etapie projektu,
- odróżnić RFI od RFP i wskazać, kiedy stosuje się każdy z nich,
- opisać problem, interesariuszy, funkcjonalności i zakres własnego systemu,
- przygotować RFI i RFP dla analizowanego systemu oraz ocenić, czy takie dokumenty są potrzebne w pracy dyplomowej.

## 1. Podstawowe pojęcia (ok. 15 min)

**System informatyczny** to zbiór powiązanych elementów (oprogramowanie, dane, sprzęt, procedury, użytkownicy) wspierających realizację określonych zadań.

**Funkcjonalność** to wyodrębniona możliwość oferowana przez system, pozwalająca użytkownikowi lub innemu systemowi osiągnąć określony cel, np. rejestracja konta, wyszukiwanie produktów, złożenie zamówienia. Funkcjonalność odpowiada na pytanie, co system potrafi zrobić. Nie jest tożsama:

- z funkcją lub metodą w kodzie (jedna funkcjonalność jest zwykle realizowana przez wiele metod i klas),
- z cechą jakościową, np. szybkością działania czy bezpieczeństwem (te należą do wymagań niefunkcjonalnych).

Funkcjonalności grupuje się w moduły (np. moduł zamówień), a następnie uszczegóławia w postaci wymagań funkcjonalnych (spotkanie 2).

**Aktor** to rola, w której człowiek lub inny system pozostaje w interakcji z analizowanym systemem. Aktor jest zawsze zewnętrzny wobec systemu. Przykłady: Klient, Administrator, zewnętrzny system płatności. Istotne uwagi:

- aktor jest rolą, a nie konkretną osobą (jedna osoba może pełnić kilka ról, np. Klient i Administrator),
- elementy wewnętrzne systemu (baza danych, moduł raportowy) nie są aktorami,
- wyróżnia się aktora głównego (inicjuje interakcję, aby osiągnąć cel) i aktora wspierającego (np. system zewnętrzny, z którego system korzysta).

Formalny zapis aktorów w języku UML jest tematem spotkania 2.

**Interesariusz** to osoba lub grupa, na którą system wpływa lub która wpływa na system. Pojęcie jest szersze niż aktor: interesariuszem może być osoba, która nie korzysta z systemu bezpośrednio, ale ma wobec niego oczekiwania lub ograniczenia (np. zamawiający, dział prawny, administrator infrastruktury).

**Zakres systemu** określa, co system obejmuje (w zakresie), a czego nie obejmuje (poza zakresem). Jasne wskazanie granic zapobiega rozrastaniu się projektu.

| Pojęcie | Przykład (sklep internetowy) |
|---|---|
| System | sklep internetowy z panelem administracyjnym |
| Moduł | zamówienia, katalog produktów, konta użytkowników |
| Funkcjonalność | złożenie zamówienia, zarządzanie asortymentem, rejestracja konta |
| Aktor | Klient, Administrator, zewnętrzny system płatności |
| Interesariusz | właściciel sklepu (zamawiający), klienci, dział prawny (wymagania dotyczące ochrony danych) |
| Poza zakresem | obsługa magazynu, księgowość |

## 2. Dokumentacja techniczna, RFI i RFP (ok. 15 min)

**Dokumentacja techniczna** to uporządkowany zbiór dokumentów opisujących potrzeby, wymagania, projekt, sposób testowania i eksploatacji systemu. Wczesne dokumenty (RFI, RFP) służą do tego, by zamawiający i wykonawca rozumieli problem w ten sam sposób, zanim powstanie kod.

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
<summary><b>Typowa struktura RFI</b> (sekcja zwijana)</summary>

1. Informacje o zamawiającym i kontekst biznesowy
2. Opis problemu i celu
3. Wstępny zakres systemu
4. Pytania do dostawców (technologie, doświadczenie, orientacyjny koszt i czas)
5. Termin i forma odpowiedzi

</details>

<details markdown="1">
<summary><b>Typowa struktura RFP</b> (sekcja zwijana)</summary>

1. Streszczenie i cel projektu
2. Opis organizacji zamawiającej i interesariuszy
3. Zakres projektu (w zakresie / poza zakresem)
4. Wymagania wstępne: funkcjonalne, niefunkcjonalne, ograniczenia (technologiczne, prawne, budżetowe)
5. Oczekiwane rezultaty (deliverables) i harmonogram z kamieniami milowymi
6. Wymagania wobec oferty (co ma zawierać odpowiedź)
7. Kryteria oceny ofert wraz z wagami
8. Warunki formalne i terminy

</details>

## 3. Zadania na zajęciach (ok. 60 min)

| # | Zadanie | Czas |
|---|---|:---:|
| **1.1** | **Wybór systemu.** Wybór systemu informatycznego, który będzie analizowany i projektowany w całym semestrze. System powinien dawać się opisać min. 8 funkcjonalnościami, 3 aktorami i 6–8 klasami, a jednocześnie być na tyle prosty, by zmieścić się w semestrze. Zalecana jest zbieżność z tematem planowanej pracy dyplomowej. Temat jest uzgadniany z osobą prowadzącą zajęcia. | 10 min |
| **1.2** | **Opis kontekstu i interesariuszy.** Opis w 5–8 zdaniach: kim jest zamawiający, jaki problem rozwiązuje system, kto z niego korzysta. Wykaz interesariuszy wraz z ich oczekiwaniami. Dla systemów bez rzeczywistego zamawiającego przyjmuje się zamawiającego założonego (firma, instytucja, jednostka uczelni), tak aby kolejne dokumenty miały uzasadnienie. | 10 min |
| **1.3** | **Wykaz funkcjonalności i aktorów.** Min. 8 funkcjonalności pogrupowanych w moduły. Min. 3 aktorów, każdy z jednozdaniowym opisem roli, z zaznaczeniem, który z nich jest aktorem głównym, a który wspierającym (w tym ewentualnym systemem zewnętrznym). Wykaz jest punktem wyjścia do wymagań na spotkaniu 2. | 15 min |
| **1.4** | **RFI (1–2 strony).** Dokument sporządzony według struktury powyżej, z co najmniej 6 pytaniami do dostawców. | 10 min |
| **1.5** | **Szkic RFP.** Streszczenie, zakres (w zakresie / poza zakresem), min. 8 wstępnych wymagań, ograniczenia, harmonogram z min. 4 kamieniami milowymi, kryteria oceny ofert z wagami sumującymi się do 100%. | 15 min |

<details markdown="1">
<summary><b>Szablon karty systemu</b> (sekcja zwijana)</summary>

```text
Nazwa systemu: ...
Zamawiający: ...
Problem: ...
Cel systemu: ...
Interesariusze: ...
Moduły i funkcjonalności: ...
Aktorzy (rola, główny/wspierający): ...
W zakresie: ...
Poza zakresem: ...
Ograniczenia (technologiczne, prawne, budżet, czas): ...
```

</details>

## 4. Wykorzystanie w pracy inżynierskiej

Laboratorium dostarcza materiału roboczego, z którego do pracy dyplomowej trafia wyłącznie to, co jest potrzebne dla danego tematu. Pełna dokumentacja może pozostać w repozytorium lub w załącznikach, a w treści pracy znajduje się jej zwięzła synteza. Zakres i układ rozdziałów wynikają z wymagań wydziału i ustaleń z promotorem.

RFI i RFP są na zajęciach ćwiczeniem z dokumentacji zamówieniowej i podlegają ocenie niezależnie od tego, czy trafią do pracy. W pracy dyplomowej są zasadne tylko w niektórych przypadkach:

- **Zasadne:** system tworzony dla konkretnego zamawiającego (firma, instytucja, jednostka uczelni), praca obejmująca wybór technologii lub dostawcy, projekt o charakterze wdrożeniowym.
- **Zazwyczaj zbędne:** aplikacja własna bez zamawiającego, biblioteka lub narzędzie, prototyp lub eksperyment badawczy, praca skoncentrowana na algorytmie lub analizie danych.

| Artefakt z zajęć | Możliwe wykorzystanie w pracy | Kiedy pominąć |
|---|---|---|
| Karta systemu (problem, cel, zakres) | Podstawa wstępu: motywacja, cel i zakres pracy (zwykle kilka akapitów) | Praktycznie zawsze przydatna |
| Interesariusze i aktorzy | Krótki akapit lub tabela w opisie systemu | Gdy system ma jeden rodzaj użytkownika i opis niczego nie wnosi |
| Wykaz funkcjonalności | Opis zakresu funkcjonalnego, wejście do rozdziału o wymaganiach | Praktycznie zawsze przydatny |
| RFI | Załącznik lub pominięcie | Brak zamawiającego i brak badania rynku dostawców |
| RFP | Wybrane elementy (założenia, ograniczenia, kryteria) w opisie systemu albo całość jako załącznik | System bez zamawiającego, praca badawcza, biblioteka, narzędzie własne |

## 5. Przedmiot oceny

| Element | Co jest oceniane |
|---|---|
| Karta systemu | spójność problemu, celu i zakresu, jasne granice systemu |
| Wykaz funkcjonalności i aktorów | poprawny poziom ogólności funkcjonalności, aktorzy jako role zewnętrzne wobec systemu |
| RFI | kompletność struktury, jakość pytań do dostawców |
| RFP | jasny zakres, mierzalne wymagania, sensowne kryteria oceny |
| Repozytorium | czytelna struktura katalogów, historia commitów |

## 6. Kryteria kompletności wyniku

- System i temat uzgodnione z osobą prowadzącą.
- Opisany problem, zamawiający (rzeczywisty lub założony) i interesariusze.
- Wykaz zawiera min. 8 funkcjonalności w modułach oraz min. 3 aktorów z opisem roli.
- Funkcjonalności nie są pomylone z metodami w kodzie ani z cechami jakościowymi.
- RFI zawiera min. 6 pytań do dostawców.
- RFP zawiera zakres, ograniczenia, harmonogram i kryteria oceny z wagami.
- Repozytorium jest założone, a pliki znajdują się w odpowiednich katalogach.

<details markdown="1">
<summary><b>Pytania kontrolne (kolokwium)</b> (sekcja zwijana)</summary>

1. Czym jest funkcjonalność i czym różni się od funkcji (metody) w kodzie oraz od wymagania niefunkcjonalnego?
2. Kim jest aktor? Czy bazę danych można uznać za aktora?
3. Czym różni się aktor od interesariusza? Podać przykład interesariusza, który nie jest aktorem.
4. Czym różni się RFI od RFP? Kiedy stosuje się każdy z nich?
5. Co powinno znaleźć się w zakresie, a co poza zakresem projektu?
6. Jakie kryteria oceny ofert można zastosować w RFP i jak dobrać wagi?
7. W jakich pracach dyplomowych RFI i RFP są zasadne, a w jakich zbędne?

</details>

---

**Dalej:** [Spotkanie 2. Wymagania i diagram przypadków użycia](spotkanie-02.md) · [Strona główna](../)
