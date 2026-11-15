# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/alealvian/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/alealvian/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty. 0x88 negamax alpha-beta with iterative deepening under a fixed 100,000-node budget per move (deterministic — no wall clock, no unseeded randomness), quiescence over captures/promotions (all evasions when in check), transposition table, MVV-LVA + TT-move ordering, and a piece-square-table evaluation mirroring the house gauntlet (P100/N320/B330/R500/Q900 + bishop pair). Practice Elo (3 trials, 6 games each): 1451, 1451, 1099 — mean 1334.

## Run it

```sh
python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=x811hdnh&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
