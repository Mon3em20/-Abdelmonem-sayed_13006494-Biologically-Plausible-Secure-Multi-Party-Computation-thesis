# CURRENT_RESEARCH_STATUS.md (16 November 2026)

| Track | Status | Evidence |
|---|---|---|
| Plain BP | Complete, 5 seeds (42-46) | PT-BENCH-v1; 75.96 +/- 2.89 % (sample SD) |
| Plain FF | Complete, 5 seeds | 59.76 +/- 3.18 %; 400 updates vs 200 |
| Secure BP, bounded (784-8-10, 90/30/30) | Complete, historical | A0, A1, BP-COMP-001 (single runs) |
| Secure BP, full size (784-128-128-10, 5000/1000/1000) | Complete for ONE seed (42) | 77.2 % test, 933.263 s MP-SPDZ time, 5224.49 MB global |
| Secure FF | NOT implemented | none |
| Profiling (RQ2), FF modification (RQ3) | Not started | none |

Main RQ is open. RQ1 partially addressed (Secure BP side only). Central hypothesis neither supported nor refuted.

Key caveats: one secure seed; MP-SPDZ time vs external elapsed are different scopes; localhost only, hardware not in run artifacts; 103-bit truncation message unresolved; checkpoint policy differs (plaintext = validation-selected, secure = epoch 5).

Next steps: see OPEN_ISSUES_v0.4.md.
