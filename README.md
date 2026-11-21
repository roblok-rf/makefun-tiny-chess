[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/roblok-rf/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/roblok-rf/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-01: a 4 KB Python chess engine

`main.py` (4,059 bytes) is the whole engine: 0x88 negamax, alpha-beta + PVS, transposition table, quiescence, MVV-LVA/killer/history ordering, null-move pruning, LMR, tapered piece-square eval. Fixed 50,000-node budget per move: deterministic, no clock, no randomness. Speaks UCI over HTTP to the make.fun env.

Python 3.13 stdlib only. `python3 main.py`. Perft start 20/400/8902/197281 (depths 1-4); kiwipete 48/2039/97862 (1-3).
