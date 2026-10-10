# Game Concept: Kronika Studia (tytuł roboczy)

*Created: 2026-10-10*
*Status: Draft*

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
| **Platform** | PC (Steam) na premierę, port na mobile (iOS / Android) później |
| **Target Audience** | Twórcy i Osiągacze — fani GDT i symulatorów zarządzania (patrz Target Player Profile) |
| **Player Count** | Single-player |
| **Session Length** | 30–120 min (naturalny punkt przerwy: koniec roku w grze) |
| **Monetization** | Premium (jednorazowy zakup), bez mikropłatności |
| **Estimated Scope** | Large (12–18 miesięcy pełna wizja, solo); MVP 2–3 miesiące, Wersja 1.0 6–9 miesięcy |
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
zwrotnymi, w których Twoje wybory rozgałęziają historię. Każda rozgrywka kończy
się inną Kroniką. Do tego żywe, animowane biuro, gdzie chemia zespołu wpływa na
jakość gier.

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
- Gracze eksperymentują z kombinacjami temat/gatunek/fokus, szukając przepisu na hit.
- Gracze śledzą trendy i planują premiery pod wydarzenia świata (nowa konsola, boom gatunku).
- Gracze przywiązują się do konkretnych pracowników i budują wokół nich zespoły.
- Gracze grają ponownie, by zobaczyć inną Kronikę (inny wynik wojny konsol, inne losy rywali).
- Gracze dzielą się swoimi Kronikami i najlepszymi grami w społeczności.

### Core Mechanics (Systems we build)
1. **Projektowanie gry** — temat, gatunek, platforma, etapy produkcji z rozkładem fokusu, polerowanie, premiera (jak w GDT, ale głębiej: więcej etapów i decyzji).
2. **Rynek i ekonomia** — trendy gatunków, segmenty graczy, konkurencja, cykle rynkowe, recenzje i sprzedaż.
3. **Żywe biuro i zespół** — pracownicy z cechami, zmęczeniem i relacjami; chemia zespołu wpływa na jakość; widoczne w animacjach.
4. **Historia świata „szkielet + reakcje”** — napisana oś czasu (epoki, technologie, wydarzenia lore) + reakcje na gracza (trendy, losy rywali, punkty zwrotne).
5. **Rozwój studia** — garaż → biuro → korporacja; badania technologii, własne silniki, odblokowania.

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
- **Feedback clarity**: raporty po premierze wyjaśniają, *dlaczego* gra dostała taką ocenę (filar „Głęboko, ale czytelnie”).
- **Recovery from failure**: klapa boli finansowo, ale uczy — raport pokazuje błędy; zabezpieczenia przed bankructwem we wczesnej fazie.

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

**Napięcia między filarami**: Filar 1 (swoboda) vs Filar 2 (czytelność) — więcej opcji to trudniejsza analiza. Filar 4 (żywe biuro) vs zakres — animacje są kosztowne.

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
| **Recommended Engine** | Do ustalenia w `/setup-engine` (PC na start, port mobile później; 2D) |
| **Key Technical Challenges** | System zapisu przy rozgałęzionej historii; skalowanie UI między PC a mobile; symulacja rynku z czytelnym feedbackiem |
| **Art Style** | 2D płaski cartoon (wektorowy), grube kontury |
| **Art Pipeline Complexity** | Medium (custom 2D, postacie modułowe, animacja szkieletowa) |
| **Audio Needs** | Moderate (muzyka zmieniająca się z epokami, dźwięki UI i biura) |
| **Networking** | None |
| **Content Volume** | Pełna wizja: 6 epok / 40 lat, ~30 tematów, 8 gatunków, 15–20 platform, 10–15 rywali, ~60 wydarzeń lore, 4 poziomy biura, 15–25 h pierwszego przejścia |
| **Procedural Systems** | Generowani pracownicy (cechy, wygląd z części); Kronika generowana z decyzji gracza; reakcje rynku |

---

## Risks and Open Questions

### Design Risks
- Balans systemu ocen gier — wyniki muszą być czytelne, nie losowe (Filar 2).
- Czy pętla projektowania pozostaje świeża po 20+ grach w jednej rozgrywce.

### Technical Risks
- Zapis gry przy rozgałęzionej historii i reakcjach świata.
- Skalowanie interfejsu między PC a mobile.

### Market Risks
- Zatłoczona nisza „klonów GDT” — wyróżnikiem muszą być świat i Kronika.
- Porównania z GDT mogą być bezlitosne, jeśli rdzeń nie będzie co najmniej równie dobry.

### Scope Risks
- Pierwsza gra z czterema systemami naraz.
- Lore (pisanie wydarzeń) i animacje mogą pochłonąć większość czasu.

### Open Questions
- Ile etapów produkcji i decyzji na etap utrzymuje głębię bez znużenia? → prototyp pętli projektowania (`/prototype`).
- Jak pokazać graczowi „dlaczego” po premierze, nie zdradzając formuły? → prototyp raportu recenzji.
- Ile wydarzeń lore na rok gry daje poczucie żywego świata bez przytłaczania? → playtest MVP.

---

## MVP Definition

**Core hypothesis**: Gracze uznają pętlę projektowania gry (pomysł → produkcja → premiera → recenzje → echo w świecie) za wciągającą na sesje 30+ minut.

**Required for MVP**:
1. Pętla projektowania gry: temat, gatunek, platforma, 3 etapy fokusu, premiera, recenzje, sprzedaż.
2. Prosty rynek: trendy gatunków i 3 rywali.
3. 1 biuro, 3–5 pracowników z prostymi animacjami (praca, zmęczenie, pomysł).
4. 10 lat osi czasu, 1 epoka, ~10 wydarzeń, 1 punkt zwrotny (wojna konsol).

**Explicitly NOT in MVP** (defer to later):
- Kolejne epoki i poziomy biura.
- Przejęcia rywali, własne silniki, tryb bez końca.
- Pełna Kronika (w MVP: proste podsumowanie).
- Port mobile.

### Scope Tiers (if budget/time shrinks)

| Tier | Content | Features | Timeline |
| ---- | ---- | ---- | ---- |
| **MVP** | 1 epoka, 10 lat, 3 rywali, 1 biuro | Pętla projektowania, prosty rynek, podstawowe biuro | ~2–3 miesiące |
| **Vertical Slice** | 1 epoka w jakości docelowej | MVP + Kronika, rozwój studia, polerowana grafika | ~4–5 miesięcy |
| **Alpha / Wersja 1.0** | 3 epoki (25 lat), 6–8 rywali, 3 poziomy biura, ~30 wydarzeń | Wszystkie systemy, 3 punkty zwrotne, Kronika | ~6–9 miesięcy |
| **Full Vision** | 6 epok (40 lat), 10–15 rywali, 4 poziomy biura, ~60 wydarzeń | Pełne lore, przejęcia rywali, tryb bez końca, port mobile | ~12–18 miesięcy |

Jeśli dostępny czas jest krótszy niż ~6 miesięcy, celem jest MVP wydane jako
Early Access, a następnie rozbudowa.

---

## Next Steps

- [ ] Fill in CLAUDE.md technology stack based on engine choice (`/setup-engine`)
- [ ] Define visual identity (`/art-bible`)
- [ ] Validate concept (`/design-review design/gdd/game-concept.md`)
- [ ] **Prototype core idea** (`/prototype game-design-loop`) — before writing GDDs, validate the concept is worth designing
- [ ] If prototype PROCEEDS: Decompose concept into systems (`/map-systems`)
- [ ] Design each system (`/design-system [system-name]`) — use prototype learnings in Tuning Knobs and Formulas sections
- [ ] Build vertical slice in Pre-Production (`/vertical-slice`) — validate full game loop before committing to Production
- [ ] Validate core loop with playtest (`/playtest-report`)
- [ ] Plan first milestone (`/sprint-plan new`)
