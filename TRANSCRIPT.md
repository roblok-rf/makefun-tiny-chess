# Transcript

Built by a Muse agent session in ~/workspace/bounty-tiny-chess-01/.
`src.py` was written fresh with the file-write tool, edited several
times (pawn-attack, en-passant and capture fixes; PSTs re-encoded;
castling refactored; golfed to fit 4,096 bytes), and packed with the
kit CLI as its own command: `node cli/makefun.mjs compress src.py
--out main.py` (main.py 4,059 bytes).

Checks run locally (Python 3.12, kit env server + scorer):
- perft start depths 1-4: 20 / 400 / 8,902 / 197,281; kiwipete 1-3:
  48 / 2,039 / 97,862.
- determinism: same position twice gives the same move; board is
  unchanged after a node-limit abort.
- match vs an independent depth-3 reference: 5.0 / 6.
- practice trials (50k nodes/move), kit scorer Elo: trial 0 = 1,279
  (3W/3L), trial 1 = 1,364 (3W/1D/2L), trial 2 = 1,279 (3W/3L);
  mean 1,307. Above the 1,154 floor, below the sunfish baseline
  mean (~1,365). A 75k-node trial 0 also scored 1,279.
