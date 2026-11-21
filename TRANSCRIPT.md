# Transcript

A 4 KB Python chess engine (`main.py`, 4,059 bytes) for tiny-chess-01.

- Top entries studied first; 15 models built, model 11 (Combined Best) is the entry.
- 0x88 negamax, alpha-beta + PVS, transposition table, quiescence, MVV-LVA/killer/history ordering, null-move pruning, LMR, tapered eval.
- Verified: perft start 20/400/8902/197281 (depths 1-4), kiwipete 48/2039/97862 (1-3); deterministic.
- Practice trials ran on the kit's env server and scorer before submission.
