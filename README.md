[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/roblok-rf/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/roblok-rf/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-01: a 4 KB Python chess engine

`main.py` (4,059 bytes) is the whole engine: a 0x88-board negamax
search with alpha-beta + PVS, a transposition table, quiescence
search, MVV-LVA + killer + history move ordering, null-move pruning
and late-move reductions, over a tapered middlegame/endgame
piece-square evaluation. It searches to a fixed budget of 50,000
nodes per move, so it is fully deterministic: no clock, no
unseeded randomness. It talks to the make.fun env over HTTP (UCI).

`src.py` is the readable source `main.py` was packed from with the
kit's `makefun compress` (LZMA payload + stub). Python 3.13
standard library only; it reads no other file.

Verified locally: perft start 20 / 400 / 8,902 / 197,281 (depths
1-4), kiwipete 48 / 2,039 / 97,862 (depths 1-3); same position
twice gives the same move. Practice trials ran on the kit's env
server and scorer; see TRANSCRIPT.md for the measured Elo.
