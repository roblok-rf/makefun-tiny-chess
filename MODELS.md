# Models

15 variants studied; model 11 (Combined Best) is `main.py`.

- 1-5: negamax, + alpha-beta, + PVS, + transposition table, + quiescence
- 6-10: MVV-LVA/killer/history ordering, null-move pruning, late-move reductions
- 11: all of the above + tapered piece-square eval, 50,000-node budget
- 12-15: further variants of the combined engine; none beat 11 within 4 KB

Model 11 is the entry: strongest play at 4,059 bytes, fully deterministic.
