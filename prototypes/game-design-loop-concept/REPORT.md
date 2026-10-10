# Concept Prototype Report: Pętla projektowania gry (Kronika Studia)

> **Date**: 2026-10-10
> **Prototype Path**: HTML
> **Concept File**: design/gdd/game-concept.md

---

## Hypothesis

Jeśli gracz wybiera temat, gatunek, platformę i rozkład fokusu w 3 etapach, to
żadna pojedyncza kombinacja nie dominuje. Poznamy to po tym, że w 6 grach
zagranych ręcznie optimum zmienia się na co najmniej 3 różne kombinacje, a w
symulacji 1000 stanów rynku najlepsza kombinacja wygrywa w mniej niż 25% stanów.

---

## Riskiest Assumption Tested

**Głębia kombinacji**: że więcej wyborów daje realnie różne wyniki, a nie jedną
oczywistą „najlepszą grę”. Założenie w większości się potwierdziło (patrz Result),
ale ujawniło dwa słabsze punkty: silny wpływ trendu i rozwiązywalny fokus.

---

## Approach

Jeden plik HTML (`prototype.html`) z modelem reguł i prostym interfejsem. Budowa
i test automatyczny: około 1 godziny. Rozgrywka trwa 6 lat; co rok gracz wybiera
temat (6), gatunek (5), platformę (3) i rozdziela po 10 punktów fokusu
(Mechanika / Oprawa / Fabuła) w 3 etapach. Po premierze widzi ocenę, przychód,
raport „dlaczego” i optimum danego roku. Osobny przycisk uruchamia symulację
1000 losowych stanów rynku.

**Path chosen:** HTML
**Reason for path:** testowaliśmy, czy reguły i kombinacje są ciekawe, a nie
„czucie” sterowania; HTML pozwala też uruchomić symulację dominacji.

**Shortcuts taken (intentional):**
- Wszystkie wartości zahardkodowane (synergie, profile gatunków, mnożniki).
- Brak pracowników, biura, historii świata, rywali, zapisu gry, grafiki, dźwięku i menu.
- Jeden wzór oceny i sprzedaży, celowo prosty; to nie jest docelowy balans.
- Brak samouczka; raport po premierze to jedyne źródło wiedzy o regułach.

---

## Result

**Symulacja (wzory nie były strojone przed pierwszym uruchomieniem):**
- 41 z 90 kombinacji wygrywa w co najmniej jednym stanie rynku; najczęstsza
  (Cyberpunk · Akcja · Konsola) w 15,1% stanów — poniżej progu 25%.
- Najlepsza stała kombinacja grana co rok osiąga tylko 49% optimum, więc
  dostosowanie się do rynku ma znaczenie.
- Udział w zwycięstwach: tematy 12–22%, gatunki 14–24%, platformy 22–43%
  (PC najczęściej). Żaden pojedynczy wybór nie dominuje.
- Zwycięzca zawiera gorący temat w 75% stanów i gorący gatunek w 61%: podążanie
  za trendem to bardzo silna heurystyka.
- Optymalny fokus da się policzyć dla każdego gatunku (dopasowanie ~100%), więc
  suwaki fokusu nie dają głębi, tylko układankę z jednym rozwiązaniem.

**Playtest (1 tester, twórca projektu, rozgrywka 6 lat):**
- Optimum zmieniło się na 5 różnych kombinacji (hipoteza: co najmniej 3).
- Wynik gracza rósł z czasem: 26% → 51% → 34% → 72% → 48% → 72% optimum;
  łącznie 51% optimum, 3 gry z oceną ≥ 8.
- Para Miasto · Logiczna była optimum w 3 z 6 lat (na Konsoli i Telefonie),
  czyli jedna para temat + gatunek wyraźnie wracała.
- Najlepszy moment: rok 4. Gracz poprawił fokus na podstawie raportu z roku 2
  i świadomie powtórzył kombinację Miasto · Symulacja · PC; ocena wzrosła
  z 8.6 do 8.8, przychód z 97,7 tys. do 125,8 tys. zł.
- Najgorszy moment: rok 3. Piraci · Logiczna dostali 5.7 mimo trendu, a optimum
  to Piraci · Przygodówka. Przyczyna (synergia −0,2, najgorsza w tabeli) była
  w raporcie, ale gracz jej **nie zauważył**.
- Zaskoczenie (pozytywne): rynek wydawał się realistyczny. Jednak trudno było
  przewidzieć wynik, gdy optimum nie pasowało do trendu, a raport nie mówił dlaczego.

Cytat testera o werdykcie: „Rdzeń działa, trzeba tylko poprawić czytelność raportu.”

---

## Metrics

| Metric | Value |
|--------|-------|
| Path used | HTML |
| Iterations to playable | N/A (playable za pierwszym razem, 0 błędów JS w teście automatycznym) |
| Prototype duration | ok. 1 godzina budowy + 1 sesja gry (6 lat) |
| Playtesters | 1 internal (twórca projektu) / 0 external |
| Feel assessment | Nie dotyczy (test reguł, nie sterowania). Raport po premierze był za płaski: kluczowa linijka nie została zauważona. |
| Hypothesis verdict | PARTIALLY CONFIRMED |

---

## Recommendation: PROCEED

Rdzeń działa: optimum zmienia się z roku na rok (5 różnych kombinacji w 6 latach,
41 zwycięzców w symulacji, najczęstszy tylko w 15% stanów), a gracz poprawił
wynik z 26% do 72% optimum, ucząc się z raportów. Najlepszy moment sesji to
dokładnie zamierzona pętla „przeczytaj raport → popraw → zbierz nagrodę”.
Słabości nie dotyczą samego rdzenia, tylko czytelności i balansu: raport nie
wyróżnia głównej przyczyny wyniku, trend zbyt często wskazuje odpowiedź, a fokus
ma jedno policzalne rozwiązanie. Te rzeczy poprawimy w dokumentach GDD.

---

## If Proceeding

- **Core tuning values discovered:**
  - Mnożnik trendu tematu ×1,35 i gatunku ×1,30 jest za silny w stosunku do
    synergii (zwycięzca zawiera gorący temat w 75% stanów). Do zmniejszenia albo
    zrównoważenia w GDD rynku.
  - Kara za zmęczenie (×0,8 temat, ×0,85 gatunek) wystarcza, by stała kombinacja
    osiągała tylko 49% optimum. Warto ją zachować.
  - Powtarzająca się para Miasto · Logiczna (synergia +0,3 i Telefon ×1,25 dla
    gier logicznych) pokazuje, że kumulacja synergii z dopasowaniem platformy
    tworzy „pewniaki”. Do sprawdzenia w balansie.
- **Assumptions confirmed:**
  - Filar „Głęboko, ale czytelnie”: gracz uczy się z raportów i świadomie poprawia wyniki.
  - Rynek z trendami i udziałami platform wydaje się realistyczny.
  - Kara za zmęczenie zachęca do zmieniania kombinacji.
- **Assumptions disproved:**
  - Że lista czynników w raporcie wystarczy do zrozumienia wyniku. Gracz nie
    zauważył głównej przyczyny złej oceny.
  - Że suwaki fokusu dają głębię. W obecnej formie to układanka z jednym rozwiązaniem
    na gatunek.
- **Emergent mechanics:**
  - Świadome „sprawdzone przepisy”: gracz wracał do kombinacji, która zadziałała,
    przeplatając je innymi grami, by uniknąć zmęczenia. Warto to sformalizować
    (np. sequele, notatnik odkrytych synergii).

**Wnioski do GDD (priorytety):**
1. Raport po premierze ma wyróżniać **jeden główny czynnik** wyniku zwykłym
   językiem (np. „Główny problem: Piraci nie pasują do gier logicznych”), a resztę
   pokazywać mniejszą czcionką.
2. Raport ma wyjaśniać, **dlaczego optimum było inne niż trend**.
3. Zmniejszyć siłę trendu względem synergii albo dodać koszt podążania za trendem
   (np. konkurencja w gorącym gatunku).
4. Przebudować fokus tak, by nie miał jednego rozwiązania (np. zależność od
   umiejętności pracowników, budżetu albo platformy).

> Note: HTML path; feel (animacje biura, „juice” premiery) nie był testowany.
> Przed GDD nie jest potrzebny osobny prototyp feel, bo rdzeń to decyzje, nie sterowanie.

**Next steps:**
1. `/design-review design/gdd/game-concept.md`
2. `/gate-check`
3. `/map-systems`
4. `/design-system [mechanic]` (use learnings in Tuning Knobs and Formulas sections)

---

## If Pivoting

N/A (werdykt PROCEED).

---

## If Killing

N/A (werdykt PROCEED).

---

## Lessons Learned

- **What assumptions were broken by actually building this?**
  Że gracz przeczyta cały raport. W praktyce patrzy na ocenę i przychód, a
  linijki czynników pomija, nawet gdy kluczowa jest oznaczona na czerwono.

- **What surprised us that didn't show up in the brainstorm?**
  Że trend tak mocno wskazuje odpowiedź (75% zwycięzców), a jednocześnie gracz
  odbiera rozbieżność między trendem a optimum jako trudną do przewidzenia.
  Oba problemy mają to samo źródło: niewidoczne synergie i dopasowanie platformy.

- **What would we test differently next time?**
  Dać prototyp co najmniej jednej osobie z zewnątrz (twórca zna intencję reguł)
  i od razu testować dwie wersje raportu: listę czynników kontra jeden wyróżniony
  główny powód.

---

> *Prototype code location: `prototypes/game-design-loop-concept/`*
> *This code is throwaway. Never refactor into production.*
> *Playable copy: https://claude.ai/artifact/XWsZQXwVQWULn9vZMSUp3D*
