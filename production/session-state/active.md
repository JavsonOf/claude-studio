# Session State

## Current Task
Concept prototype: `game-design-loop` (Kronika Studia)

## Hypothesis
Jeśli gracz wybiera temat, gatunek, platformę i rozkład fokusu w 3 etapach, to
żadna pojedyncza kombinacja nie dominuje. Poznamy to po tym, że w 6 grach
zagranych ręcznie zwycięża co najmniej 3 różne kombinacje, a w symulacji
1000 gier najlepsza kombinacja wygrywa < 25% razy.

## Riskiest assumption
Głębia kombinacji (więcej wyborów = realnie różne wyniki).

## Path
HTML (single file, no install).

## Scope
- 6 tematów x 5 gatunków x 3 platformy, 3 etapy z suwakami fokusu
- Zmienny trend rynkowy per rok
- Ocena + sprzedaż + raport „dlaczego"
- Przycisk „Symuluj 1000 gier" wykrywający dominującą kombinację
- Wycięte: pracownicy, biuro, lore, rywale, zapis, grafika, dźwięk, menu

## Progress
- [x] Phase 1: hypothesis defined
- [x] Phase 3: path chosen (HTML)
- [x] Phase 4: plan approved
- [x] Phase 5: implemented `prototypes/game-design-loop-concept/prototype.html` (smoke-tested in headless Chromium, no JS errors)
- [ ] Phase 6: playtest debrief  <- current (waiting for user to play 6 years and answer 5 debrief questions)
- [ ] Phase 7: REPORT.md + prototypes/index.md

## Open questions
- Review mode: lean (CD-PLAYTEST skipped)

## Automated simulation result (first run, formulas NOT tuned)
- 1000 market states: 41 of 90 combos win at least once; top combo 15.1% (< 25% threshold: PASS)
- Best fixed combo played every year (with fatigue): 49% of per-state optimum
- Marginals: themes 12-22%, genres 14-24%, platforms 22-43% (PC highest)
- Winner contains the hot theme in 75% of states, hot genre in 61% -> trend-following is a strong heuristic (shallow-depth risk)
- Best focus per genre is solvable (match ~1.0): focus allocation is a solved puzzle per genre, not a source of depth
- Caveat: sim tests structure of MY formulas, not fun
- Random play scored ~24% of optimum over 6 years in the UI smoke test
