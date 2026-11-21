# Models: 15 approaches (ATM)

House ladder: depth-2 (855) to nodes-2M (1712); sunfish 4 KB
baseline (50k nodes/move) means ~1,365 practice Elo.

1. Greedy capture (kit starter). ~800 Elo.
2. Material-only alpha-beta, depth 3.
3. Alpha-beta + piece-square tables, depth 4.
4. Model 3 + quiescence (captures). Kills horizon blunders.
5. Model 4 + transposition table.
6. Model 5 + MVV-LVA ordering.
7. Model 6 + killer moves + history heuristic.
8. Model 7 + principal-variation search.
9. Model 8 + null-move pruning (R=2, depth>=3).
10. Model 9 + late-move reductions. Depth 6-7 middlegame.
11. COMBINED BEST (submitted): 1-10 + tapered mg/eg PST eval
    + iterative deepening to a fixed 50,000-node budget.
    Deterministic, ~45k nodes/s.
12. Bitboard engine: magic bitboards don't fit 4 KB with a search.
13. Tiny NNUE eval: weights cost ~1 KB, slow in Python. Rejected.
14. Clock-based deepening: stronger but non-deterministic. Rejected.
15. Opening book + tablebase: final openings are drawn after the
    deadline; tablebases don't fit. Rejected.
