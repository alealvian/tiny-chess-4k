# tiny-chess-01

A 4 KB Python chess engine for the make.fun bounty
"Build the strongest chess engine in 4 KB of Python".

- `main.py` — the entry point (4,057 bytes, produced by the kit's own
  `makefun compress` from `engine.py`). Python stdlib only.
- `engine.py` — the readable source (not part of the committed
  snapshot; the bundle sends it beside the sessions).
- `RESULTS.md` — practice trial Elo numbers.

Design: 0x88 board, negamax alpha-beta with iterative deepening under a
fixed 100,000-node budget per move (deterministic — no wall clock, no
unseeded randomness), quiescence over captures/promotions (all evasions
when in check), transposition table, MVV-LVA + TT-move ordering, and a
piece-square-table evaluation mirroring the house gauntlet's eval
(P100/N320/B330/R500/Q900 + formula PSTs + bishop pair, tapered king).

Practice Elo (3 trials, 6 games each): 1451, 1451, 1099 — mean 1334.
Floor to enter the final: 1154. House baseline: ~1365.
