# Game Concept: Kronika Studia (tytuł roboczy)

*Created: 2026-10-10*
*Status: Draft (zrewidowany po design review 2026-10-10)*

---

## Elevator Pitch

> To symulator studia gier, w którym projektujesz gry głębiej niż w Game Dev
> Tycoon, budujesz żywe biuro pełne ludzi z charakterem i walczysz na
> realistycznym rynku w fikcyjnym świecie z własną historią — a Twoje hity
> i porażki zmieniają bieg tej historii.

---

## Core Identity

| Aspect | Detail |
| ---- | ---- |
| **Genre** | Symulacja / tycoon (management), z elementami strategii ekonomicznej |
| **Platform** | PC (Steam) na premierę; port na mobile (Android / iOS) **warunkowy** — tylko po udanym spike'u technicznym (eksport C# na mobile jest w Godot eksperymentalny) |
| **Target Audience** | Twórcy i Osiągacze — fani GDT i symulatorów zarządzania (patrz Target Player Profile) |
| **Player Count** | Single-player |
| **Session Length** | 30–120 min (naturalny punkt przerwy: koniec roku w grze) |
| **Monetization** | Premium (jednorazowy zakup), bez mikropłatności |
| **Estimated Scope** | Large (16–22 miesiące pełna wizja, solo); MVP 3–4 miesiące, Vertical Slice 6–7 miesięcy, Wersja 1.0 10–13 miesięcy |
| **Comparable Titles** | Game Dev Tycoon, Mad Games Tycoon 2, Two Point Hospital |

---

## Core Fantasy

**„Od garażu do legendy.”** Zaczynasz w garażu z jednym komputerem, a kończysz
jako studio, którego gry zapisały się w historii branży. Każda wydana gra jest
*Twoja* — Twój pomysł, Twoje decyzje, Twój zespół. Świat zapamiętuje Twoje hity:
trendy, które zapoczątkowałeś, rywali, których pokonałeś, i wojnę konsol, którą
rozstrzygnąłeś. Na końcu dostajesz Kronikę — alternatywną historię branży,
którą współtworzyłeś.

---

## Unique Hook

**Jak Game Dev Tycoon, A DO TEGO świat z własnym lore, który pamięta Twoje
gry** — fikcyjna branża z korporacjami, epokami technologicznymi i punktami
zwrotnymi, w których Twoje gry przestawiają przełączniki historii (2–3 możliwe
wyniki na punkt zwrotny). Rywale z charakterem reagują na Twoje hity, a każda
rozgrywka kończy się inną Kroniką. Do tego żywe, animowane biuro, gdzie chemia zespołu wpływa na
jakość gier.

---

## Tone & Voice

**Ton: ciepła satyra z nostalgią, z dramatem w kluczowych momentach.** Każdy
rejestr ma swoje miejsce, żeby się nie mieszały:

| Rejestr | Gdzie występuje | Przykład |
| ---- | ---- | ---- |
| **Satyra** (domyślny) | Nazwy firm i produktów, recenzje, newsy roku, komentarze rywali | Recenzent narzeka, że „kolejna gra o piratach to już piractwo” |
| **Nostalgia** | Kronika, przejścia między epokami, podsumowania roku | „Pamiętasz garaż i pierwszy komputer? Branża też pamięta.” |
| **Dramat** | Wyłącznie punkty zwrotne: kryzysy, wojny konsol, upadki studiów | Wojna konsol rozstrzyga się na oczach gracza |

- **Język oryginału:** polski. Lore i humor piszemy najpierw po polsku; inne
  wersje językowe to lokalizacja, a nie tłumaczenie 1:1.
- **Fikcyjne firmy:** każda ma własną tożsamość (charakter, ambicję, styl), której
  nie da się zmapować 1:1 na prawdziwą markę. Parodia branży tak, parodia
  konkretnej firmy nie.

---

## Player Experience Analysis (MDA Framework)

### Target Aesthetics (What the player FEELS)

| Aesthetic | Priority | How We Deliver It |
| ---- | ---- | ---- |
| **Expression** (self-expression, creativity) | 1 | Głębokie projektowanie gier, nazywanie gier i studia, budowa biura i zespołu po swojemu |
| **Discovery** (exploration, secrets) | 2 | Lore odkrywane przez wydarzenia, odblokowania epok, ukryte zależności rynku |
| **Challenge** (obstacle course, mastery) | 3 | Czytanie rynku, timing premier, finanse, konkurencja |
| **Narrative** (drama, story arc) | 4 | Szkielet historii świata + Kronika generowana z decyzji gracza |
| **Fantasy** (make-believe, role-playing) | 5 | Fantazja szefa studia — bez elementów RPG |
| **Sensation** (sensory pleasure) | 6 | Żywa animacja biura, „juice” przy premierach i recenzjach |
| **Submission** (relaxation, comfort zone) | 7 | Spokojne tempo, pauza w każdej chwili |
| **Fellowship** (social connection) | N/A | Single-player; więź budowana z postaciami w grze |

### Key Dynamics (Emergent player behaviors)
- Gracze wybierają własną drogę studia (nisza kontra trend, jakość kontra tempo) i budują wokół niej reputację.
- Gracze eksperymentują z kombinacjami temat/gatunek/fokus, szukając przepisu na hit, i zapisują odkryte synergie w notatniku.
- Gracze śledzą trendy i planują premiery pod wydarzenia świata (nowa konsola, boom gatunku).
- Gracze przywiązują się do konkretnych pracowników i budują wokół nich zespoły.
- Gracze grają ponownie, by zobaczyć inną Kronikę (inny wynik wojny konsol, inne losy rywali).
- Gracze dzielą się swoimi Kronikami i najlepszymi grami w społeczności.

### Core Mechanics (Systems we build)
1. **Projektowanie gry** — temat, gatunek, platforma, etapy produkcji z rozkładem fokusu, polerowanie, premiera. **Fokus to kompromis bez jednego optimum:** każde ustawienie (np. więcej mechaniki kontra więcej fabuły) przyciąga inny segment graczy i buduje inną reputację studia, zamiast dopasowywać się do jednego „idealnego” profilu gatunku.
2. **Rynek i ekonomia** — segmenty graczy, trendy z cyklem życia, konkurencja, udziały platform, recenzje i sprzedaż. **Trend ma swoją cenę:** gorący gatunek przyciąga rywali (nasycenie), a trend może wygasnąć w trakcie produkcji. Gracz decyduje, czy gonić trend, czy budować niszę.
3. **Żywe biuro i zespół** — pracownicy z cechami, zmęczeniem i relacjami; chemia zespołu wpływa na jakość; widoczne w animacjach.
4. **Historia świata „szkielet + przełączniki”** — liniowa, napisana oś czasu (epoki, technologie, wydarzenia lore) z kilkoma punktami zwrotnymi; każdy ma 2–3 wyniki zależne od działań gracza. Świat zapisuje jawną listę **flag stanu** (np. „wojnę konsol wygrał X”, „rywal Y upadł”), a lore jest skutkiem mechanicznym (zmienia trendy, platformy, rywali) i pojawia się w raporcie po premierze oraz w newsach roku, nie w bocznej zakładce.
5. **Rywale z charakterem** — każdy rywal ma jedną wyraźną cechę (np. kopiuje hity, stawia na jakość, goni trendy) i jedną reakcję na gracza (np. komentuje Twoją poprzednią grę, wchodzi w Twój gatunek). To najtańsza droga do „świat pamięta”.
6. **Rozwój i tożsamość studia** — garaż → biuro → korporacja; badania technologii, własne silniki, odblokowania. Studio buduje **reputację i bazę fanów** w wybranych segmentach i gatunkach; to one pamiętają Twój styl i nagradzają konsekwencję (serie, sequele).

### Ekonomia (zasady — liczby ustali GDD ekonomii)

- **Koszty:** pensje (co miesiąc gry), koszt produkcji gry (zależny od skali i długości), czynsz biura, badania technologii i silników, licencje platform.
- **Jednostka czasu:** miesiąc gry; jedna gra powstaje przez kilka miesięcy, więc trend w chwili premiery może być inny niż na starcie produkcji.
- **Ochrona przed spiralą bankructwa:** klapa ma kosztować, a nie kończyć grę. Gracz ma wyjścia awaryjne (np. kredyt, zlecenia dla wydawcy, tańsza „gra poboczna”, zwolnienia). Bankructwo jest możliwe dopiero po serii złych decyzji, nie po jednej klapie.
- **Wydatki w późnej grze:** droższe produkcje, własne silniki, przejęcia rywali i ryzykowne projekty AAA, żeby gotówka nie traciła znaczenia po zbudowaniu dużego biura.
- **Skala w czasie:** rozmiar rynku, budżety i pensje rosną wspólnie między epokami (jedna krzywa skali), żeby decyzje miały podobną wagę w każdej epoce.
- **Hamulce snowballu:** rosnące koszty utrzymania, rywale reagujący na lidera rynku i nasycenie gatunków.

---

## Player Motivation Profile

### Primary Psychological Needs Served

| Need | How This Game Satisfies It | Strength |
| ---- | ---- | ---- |
| **Autonomy** (freedom, meaningful choice) | Tysiące kombinacji gier, własny styl studia, wybór platform i strategii | Core |
| **Competence** (mastery, skill growth) | Coraz lepsze czytanie rynku; recenzje i sprzedaż potwierdzają rosnące umiejętności | Core |
| **Relatedness** (connection, belonging) | Pracownicy znani z imienia, rywale i krytycy jako postacie świata | Supporting |

### Player Type Appeal (Bartle Taxonomy)

- [x] **Achievers** (goal completion, collection, progression) — How: rozwój studia, rekordy sprzedaży, nagrody branżowe, tytuł Legendy Branży
- [x] **Explorers** (discovery, understanding systems, finding secrets) — How: odkrywanie lore, mechanik rynku i punktów zwrotnych historii
- [ ] **Socializers** (relationships, cooperation, community) — How: drugorzędnie — dzielenie się Kronikami poza grą
- [ ] **Killers/Competitors** (domination, PvP, leaderboards) — How: nie dotyczy (brak PvP); rywalizacja tylko z AI

Dodatkowo (Quantic Foundry): **Twórcy** (Design) i **Stratedzy** (Strategy) jako główna motywacja.

### Flow State Design

- **Onboarding curve**: pierwsze 10 minut to garaż i pierwsza gra z podpowiedziami krok po kroku; każdy system (rynek, zespół, wydarzenia) odblokowuje się stopniowo.
- **Difficulty scaling**: rosnąca konkurencja, droższe produkcje i bardziej wymagający rynek w kolejnych epokach.
- **Feedback clarity**: raport po premierze zawsze wyróżnia **jeden główny powód** wyniku zwykłym językiem (np. „Główny problem: piraci nie pasują do gier logicznych”), a pozostałe czynniki pokazuje mniejszą czcionką. Raport wyjaśnia też, dlaczego optimum było inne niż trend. Przed premierą gracz widzi prognozę sprzedaży jako widełki (filar „Głęboko, ale czytelnie”).
- **Recovery from failure**: klapa boli finansowo, ale uczy — raport pokazuje główny błąd, a wyjścia awaryjne (patrz Ekonomia) chronią przed spiralą bankructwa.

---

## Core Loop

### Moment-to-Moment (30 seconds)
Pojedyncza decyzja projektowa: wybór tematu, gatunku, platformy, rozkład fokusu
w etapie produkcji albo przypisanie pracownika do zadania. Każda decyzja daje
natychmiastowy, widoczny feedback — dymki pomysłów nad pracownikami, rosnące
punkty projektu, animacje w biurze.

### Short-Term (5-15 minutes)
**Pomysł → Projekt → Produkcja (3–4 etapy z decyzjami) → Polerowanie lub
wydanie → Premiera → Recenzje i sprzedaż → Echo w świecie.**
Decyzje: budżet, timing premiery (przed czy po konkurencji), polerować dłużej,
platforma. „Jeszcze jedna gra” zaczyna się po recenzjach i po zobaczeniu,
czy gra ruszyła trend, zaszkodziła rywalowi lub przesunęła udziały platform.

### Session-Level (30-120 minutes)
Kilka gier + jedno wydarzenie świata (często częściowo wywołane przez gracza) +
jeden krok rozwoju studia (nowy pracownik, biuro, technologia, silnik).
Naturalny punkt przerwy: koniec roku z podsumowaniem i nagrodami branżowymi.

### Long-Term Progression
Garaż → małe biuro → duże biuro → korporacja. Odblokowywanie technologii,
tematów i gatunków według epok. Lore odkrywane stopniowo. Cel: dotrwać do końca
osi czasu (pełna wizja: 40 lat) z najlepszym wynikiem — tytuł Legendy Branży —
i otrzymać własną Kronikę. Potem opcjonalny tryb bez końca.

### Retention Hooks
- **Curiosity**: Co przyniesie następna epoka? Która konsola wygra wojnę? Jakie lore kryje kolejne wydarzenie?
- **Investment**: Rozwinięte studio, ulubieni pracownicy, seria gier (sequele).
- **Social**: Dzielenie się Kronikami i najlepszymi grami w społeczności.
- **Mastery**: Lepsze czytanie rynku, wyższe oceny, szybsza droga do Legendy; inna Kronika w kolejnej rozgrywce.

---

## Game Pillars

### Pillar 1: Twoja gra, Twój podpis
Każda wydana gra ma być wyraźnie *Twoja* — wynikać z Twoich decyzji, nie z automatu.

**Gra jest „Twoja”, gdy:** (1) istnieje kilka opłacalnych dróg do sukcesu (nisza
kontra trend, jakość kontra tempo, seria kontra nowość), więc nie ma jednej
„poprawnej” gry roku, oraz (2) świat zapamiętuje tożsamość Twojego studia
poprzez reputację i fanów, którzy nagradzają konsekwentny styl.

*Design test*: Jeśli wybieramy między funkcją dającą graczowi więcej twórczych decyzji a taką, która robi coś za niego, wybieramy decyzje gracza.

### Pillar 2: Głęboko, ale czytelnie
Rynek i ekonomia są głębokie, ale gracz zawsze może zrozumieć, *dlaczego* coś się udało lub nie.

*Design test*: Jeśli wybieramy między kolejną ukrytą zmienną a lepszym raportem lub feedbackiem, wybieramy czytelność.

### Pillar 3: Świat, który pamięta
Świat ma własną historię, ale zapamiętuje Twoje hity, klapy i wybory — każda rozgrywka pisze własną Kronikę.

*Design test*: Jeśli wybieramy między funkcją zostawiającą ślad w historii świata a taką, która znika bez echa, wybieramy ślad.

### Pillar 4: Biuro, które żyje
Ważne systemy widać w biurze — emocje, zmęczenie i chemia zespołu objawiają się zachowaniem i animacją, nie tylko liczbami.

*Design test*: Jeśli coś można pokazać jako animację lub zachowanie albo jako cyfrę w tabelce, wybieramy zachowanie (z tabelką jako dodatkiem).

**Napięcia między filarami i ich rozstrzygnięcie**:
- Filar 1 (swoboda) vs Filar 2 (czytelność): więcej opcji to trudniejsza analiza. **Reguła:** raport zawsze pokazuje jeden główny powód, a odkryte synergie trafiają do notatnika studia, więc wiedza gracza rośnie razem z liczbą opcji.
- Filar 4 (żywe biuro) vs zakres: animacje są kosztowne. **Reguła:** w MVP tylko 3 podstawowe stany postaci (praca, zmęczenie, pomysł); nowe animacje dodajemy dopiero, gdy pokazują stan ważny dla decyzji gracza.

### Anti-Pillars (What This Game Is NOT)

- **NOT RPG**: brak bohatera z poziomami, walki, ekwipunku — odciągałoby od zarządzania i projektowania (Filary 1 i 2).
- **NOT mikrozarządzanie jak w The Sims**: brak potrzeb fizjologicznych i sterowania każdym krokiem pracownika — zabrałoby czas sercu gry, czyli projektowaniu (Filar 1).
- **NOT prawdziwe marki i firmy**: świat jest fikcyjny z własnym lore (Filar 3); unikamy też ryzyka prawnego.
- **NOT multiplayer w pierwszej wersji**: rozbiłby zakres pierwszej gry (Filary 3 i 4).
- **NOT mikropłatności / pay-to-win**: podważyłyby uczciwość rynku i analityki (Filar 2).

---

## Visual Identity Anchor

**Wybrany kierunek: „Płaski Cartoon”**

**Zasada wizualna (one-line rule):** *Czytelność przed szczegółem.*

**Zasady wspierające:**
1. **Grube kontury, płaskie kolory** — każdy obiekt i postać czytelne na pierwszy rzut oka, również na małym ekranie (port mobile).
   *Design test:* jeśli wybieramy między dodatkowym detalem a czytelnością sylwetki, wybieramy sylwetkę.
2. **Ruch zamiast detalu** — życie biura pokazujemy animacją (szkieletowa 2D, postacie składane z części), nie gęstością rysunku. Wspiera Filar 4.
   *Design test:* jeśli budżet pozwala na jedno — nową animację zachowania albo bogatszy rysunek — wybieramy animację.
3. **Epoka w palecie** — każda epoka historii świata ma własny akcent kolorystyczny (np. ciepłe beże lat garażowych → chłodne neony ery online), by gracz czuł upływ czasu. Wspiera Filar 3.
   *Design test:* jeśli element UI lub biura może podkreślić epokę bez utraty czytelności, robimy to.

**Filozofia kolorów:** ciepła, przyjazna, nasycona baza z wyraźnymi kolorami funkcyjnymi (zielony = sukces, czerwony = problem, złoty = hit/nagroda) spójnymi w całym UI; paleta akcentów zmienia się z epokami.

---

## Inspiration and References

| Reference | What We Take From It | What We Do Differently | Why It Matters |
| ---- | ---- | ---- | ---- |
| Game Dev Tycoon | Rdzeń: temat + gatunek + fokus, premiera i recenzje | Głębsze etapy, żywy świat z lore, reagujący rynek, animowane biuro | Udowodnił, że temat sprzedaje się w milionach egzemplarzy |
| Two Point Hospital | Żywe, animowane miejsce pracy z humorem | 2D płaski styl, nacisk na projektowanie, nie na obsługę klientów | Pokazuje siłę „widocznego” zarządzania |
| Fortnite (sezony) | Lore odkrywane stopniowo przez wydarzenia | Lore w świecie branży gier, częściowo zależne od gracza | Lore buduje zaangażowanie i powód do powrotów |
| Minecraft | Poczucie nieograniczonych możliwości | Swoboda w projektowaniu gier i budowie studia | Ekspresja jako główna motywacja gracza |
| Mad Games Tycoon 2 | Rozbudowane biuro i więcej opcji niż GDT | Czytelność i żywy świat zamiast samej liczby opcji | Dowód popytu na „więcej GDT” |

**Non-game inspirations**: historia prawdziwej branży gier (wojny konsol, krach
1983, narodziny gier online) jako wzór dla fikcyjnej osi czasu; dokumenty
o studiach gier (np. „Indie Game: The Movie”).

---

## Target Player Profile

| Attribute | Detail |
| ---- | ---- |
| **Age range** | 14–35 |
| **Gaming experience** | Mid-core |
| **Time availability** | Sesje 30–60 min w tygodniu, dłuższe w weekendy |
| **Platform preference** | PC (Steam), później telefony |
| **Current games they play** | Game Dev Tycoon, Minecraft, Two Point Hospital / Mad Games Tycoon 2 |
| **What they're looking for** | „Więcej GDT” — głębszy świat, żywsze biuro, rynek, który nie jest przewidywalny |
| **What would turn them away** | Losowe, nieczytelne wyniki; mikrozarządzanie; mikropłatności; elementy RPG |

---

## Technical Considerations

| Consideration | Assessment |
| ---- | ---- |
| **Recommended Engine** | Godot 4.7.2 + C# (ustalone w `/setup-engine`; szczegóły w `.claude/docs/technical-preferences.md`) |
| **Key Technical Challenges** | Zapis świata (log zdarzeń i flag stanu, wersjonowanie zapisów); osobne układy UI dla myszy i dotyku; symulacja rynku z czytelnym feedbackiem; własne wykresy (Godot nie ma wbudowanych); deterministyczna symulacja (seed) do odtwarzania Kroniki |
| **Art Style** | 2D płaski cartoon (wektorowy), grube kontury |
| **Art Pipeline Complexity** | High dla solo debiutanta (postacie modułowe × animacje × 4 poziomy biura × palety epok); technikę animacji 2D wybierze art bible i spike techniczny |
| **Audio Needs** | Moderate (muzyka zmieniająca się z epokami, dźwięki UI i biura) |
| **Networking** | None |
| **Content Volume** | Pełna wizja: 6 epok / 40 lat, ~30 tematów, 8 gatunków, 15–20 platform, 10–15 rywali, ~60 wydarzeń lore na liniowym szkielecie z ~6 punktami zwrotnymi (2–3 wyniki każdy), 4 poziomy biura, 15–25 h pierwszego przejścia |
| **Procedural Systems** | Generowani pracownicy (cechy, wygląd z części); Kronika składana z ~12 bitów narracyjnych (każdy w 3–4 wariantach tekstu) według flag stanu świata; reakcje rynku i rywali |

---

## Risks and Open Questions

### Design Risks
- Balans systemu ocen gier — wyniki muszą być czytelne, nie losowe (Filar 2).
- Czy pętla projektowania pozostaje świeża po 20+ grach w jednej rozgrywce. Plan: nowe zmienne wraz z epokami (zmiana preferencji segmentów, nowe platformy), sequele jako mechanika i pamięć zmęczenia graczy z kilku ostatnich gier.
- Haczyk „świat pamięta” i Kronika nie zostały jeszcze sprawdzone — prototyp nie miał lore ani rywali.
- Ekonomia (koszty, bankructwo, skala w czasie) nie została jeszcze przetestowana — prototyp liczył tylko przychód.
- Ukryte tabele synergii nie skalują się (30 tematów × 8 gatunków); potrzebny model oparty na cechach, który gracz może odkrywać.

### Technical Risks
- Zapis gry: log zdarzeń i flagi stanu świata, z wersjonowaniem i migracją starych zapisów.
- Port mobilny: eksport C# na Androida i iOS jest w Godot eksperymentalny, a interfejs dotykowy wymaga osobnych układów. Dlatego port jest warunkowy.
- Wydajność żywego biura (wiele animowanych postaci) na słabszym sprzęcie.

### Market Risks
- Zatłoczona nisza „klonów GDT” — wyróżnikiem muszą być świat i Kronika.
- Porównania z GDT mogą być bezlitosne, jeśli rdzeń nie będzie co najmniej równie dobry.

### Scope Risks
- Pierwsza gra z sześcioma systemami naraz.
- Lore (pisanie wydarzeń) i animacje mogą pochłonąć większość czasu; liniowy szkielet z przełącznikami ogranicza liczbę wariantów do napisania.
- Grafika ma złożoność High; to największe ryzyko zakresu (Filar 4).

### Open Questions
- ~~Czy pętla projektowania ma głębię?~~ → częściowo potwierdzone prototypem (`prototypes/game-design-loop-concept/REPORT.md`).
- ~~Jak pokazać „dlaczego” po premierze?~~ → jeden wyróżniony główny powód + prognoza widełkowa (z prototypu); do sprawdzenia w MVP.
- Ile wydarzeń lore na rok gry daje poczucie żywego świata bez przytłaczania? → playtest MVP.
- Czy fokus jako kompromis między segmentami graczy daje realne decyzje bez jednego optimum? → GDD projektowania gry + symulacja.
- Czy port mobilny jest wykonalny? → spike techniczny (pusty eksport C# na Androida, 30 animowanych postaci na słabym telefonie).

### Prototype Learnings (game-design-loop, 2026-10-10)

Prototyp HTML potwierdził pętlę „raport → poprawka → nagroda” i zróżnicowane
optima rynku (werdykt PROCEED, hipoteza częściowo potwierdzona, 1 tester).
Wnioski wpisane do tego dokumentu:
- Raport musi wyróżniać jeden główny powód — tester nie zauważył kluczowej linijki.
- Trend był zbyt silny (zwycięzca miał gorący temat w 75% stanów rynku) → trend ma teraz cenę.
- Fokus miał jedno policzalne rozwiązanie → fokus jest teraz kompromisem między segmentami.
- Platforma ważyła więcej niż treść gry, a ocena miała sufit 10 → do rozwiązania w GDD rynku i projektowania gry.
- Kara za zmęczenie patrzyła tylko na poprzednią grę → pamięć kilku ostatnich gier.

---

## MVP Definition

**Core hypothesis 1 (pętla)**: Gracze uznają pętlę projektowania gry (pomysł → produkcja → premiera → recenzje → echo w świecie) za wciągającą na sesje 30+ minut, a żadna pojedyncza heurystyka (np. „idź za trendem”) nie wygrywa w więcej niż 40% stanów rynku.

**Core hypothesis 2 (świat pamięta)**: Po 10 latach gry gracz z zewnątrz potrafi własnymi słowami powiedzieć, co jego studio zmieniło w świecie, a dwie rozgrywki dają zauważalnie różne Kroniki.

**Required for MVP**:
1. Pętla projektowania gry: temat, gatunek, platforma, 3 etapy fokusu jako kompromis między segmentami graczy, premiera, recenzje z jednym wyróżnionym powodem, sprzedaż.
2. Rynek: trendy z cyklem życia i nasyceniem, 3 rywali z jedną cechą i jedną reakcją na gracza.
3. Prosta ekonomia: pensje, koszt produkcji, jedno wyjście awaryjne przed bankructwem.
4. 1 biuro, 3–5 pracowników z 3 podstawowymi animacjami (praca, zmęczenie, pomysł).
5. 10 lat osi czasu, 1 epoka, 10 wydarzeń (z czego 3 reagują na gracza), 1 punkt zwrotny (wojna konsol, 2 strony, 2 wyniki zależne od gracza).
6. Krótka Kronika: 6–8 zdań składanych ze slotów według flag stanu świata.
7. Playtest z co najmniej jedną osobą z zewnątrz (nie twórcą).

**Explicitly NOT in MVP** (defer to later):
- Kolejne epoki i poziomy biura.
- Przejęcia rywali, własne silniki, tryb bez końca.
- Pełna Kronika (w MVP: krótka, 6–8 zdań).
- Port mobile (warunkowy, po spike'u technicznym).

### Scope Tiers (if budget/time shrinks)

| Tier | Content | Features | Timeline |
| ---- | ---- | ---- | ---- |
| **MVP** | 1 epoka, 10 lat, 3 rywali, 1 biuro | Pętla projektowania, rynek z ceną trendu, prosta ekonomia, podstawowe biuro, krótka Kronika | ~3–4 miesiące |
| **Vertical Slice** | 1 epoka w jakości docelowej | MVP + rozwój i reputacja studia, polerowana grafika | ~6–7 miesięcy |
| **Alpha / Wersja 1.0** | 3 epoki (25 lat), 6–8 rywali, 3 poziomy biura, ~30 wydarzeń | Wszystkie systemy, 3 punkty zwrotne, pełna Kronika | ~10–13 miesięcy |
| **Full Vision** | 6 epok (40 lat), 10–15 rywali, 4 poziomy biura, ~60 wydarzeń | Pełne lore, przejęcia rywali, tryb bez końca; port mobile, jeśli spike się powiedzie | ~16–22 miesiące |

Jeśli dostępny czas jest krótszy niż ~6 miesięcy, celem jest MVP sprawdzone
w playtestach (obie hipotezy), a nie wydanie: Early Access ma sens dopiero
wtedy, gdy rdzeń i haczyk są potwierdzone.

---

## Next Steps

- [x] Fill in CLAUDE.md technology stack based on engine choice (`/setup-engine`) — Godot 4.7.2 + C#
- [x] **Prototype core idea** (`/prototype game-design-loop`) — PROCEED (`prototypes/game-design-loop-concept/REPORT.md`)
- [x] Validate concept (`/design-review design/gdd/game-concept.md`) — NEEDS REVISION, revised 2026-10-10
- [ ] Define visual identity (`/art-bible`)
- [ ] Technical spike: C# Android export, 30 animated characters, save/load (before committing to the mobile port)
- [ ] Decompose concept into systems (`/map-systems`)
- [ ] Design each system (`/design-system [system-name]`) — use prototype learnings in Tuning Knobs and Formulas sections
- [ ] Build vertical slice in Pre-Production (`/vertical-slice`) — validate full game loop before committing to Production
- [ ] Validate core loop with playtest (`/playtest-report`)
- [ ] Plan first milestone (`/sprint-plan new`)
