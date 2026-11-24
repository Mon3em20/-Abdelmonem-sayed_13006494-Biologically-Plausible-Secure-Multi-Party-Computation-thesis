# CURRENT_RESEARCH_STATUS.md (24 November 2026)

(The 16 November 2026 snapshot, in which Secure FF was "NOT implemented", is superseded by this file; the historical report `CHANGELOG_v0.4.md` / `OPEN_ISSUES_v0.4.md` keep their v0.4 wording.)

| Track | Status | Evidence |
|---|---|---|
| Plain BP | Complete, 5 seeds (42-46) | PT-BENCH-v1; 75.96 +/- 2.89 % (sample SD); seed 42: 77.2 % |
| Plain FF | Complete, 5 seeds | 59.76 +/- 3.18 %; 400 updates vs 200; seed 42: val 62.0 %, test 62.7 % (620 / 627 correct) |
| Secure BP, bounded (784-8-10, 90/30/30) | Complete, historical | A0, A1, BP-COMP-001 (single runs) |
| Secure BP, full size (784-128-128-10, 5000/1000/1000) | Complete for ONE seed (42) | 77.2 % test, 933.263 s MP-SPDZ time, 5224.49 MB global |
| Secure FF (784-128-128, 116,992 params), full size | **Implemented, executed and verified for ONE seed (42)** (SECURE-FF-MATCHED-v1, run 22 Nov 2026) | 60.9 % test (609/1000); selected layer-2 epoch 1, 60.8 % validation (608/1000); 253.451 s MP-SPDZ time; 254.07 s external run wall; 18.76 s compile; 4,501 MB party-0 / 14,748.1 MB global; 1,799,138 party-0 rounds; max party peak RSS 240.3 MB; hard checks 13/13, bands 17/17; mini rehearsal 13/13 |
| Profiling (RQ2), FF modification (RQ3) | Not started | none |

Main RQ is open. RQ1 partially addressed (raw single-seed measurements of both secure methods exist; no controlled comparison). RQ2 not yet adequately addressed (only phase-level party-0 timer deltas; per-operation profiling needed). RQ3 not yet adequately addressed (no MPC-aware modification, no ablation). Central hypothesis neither supported nor refuted.

Key caveats of the Secure BP vs Secure FF raw comparison (not controlled): compiler flags (-l for Secure BP only); external wall time encloses compilation for Secure BP only; RSS scope differs (tree maximum vs maximum of three party processes); architecture/parameters (118,282 vs 116,992); workload (200 updates, ~25,000 presentations vs 400 updates, ~100,000 presentations); checkpoint policy (epoch 5 vs validation-selected). Secure FF sent more data (14,748.1 MB vs 5,224.49 MB global) and reached lower accuracy (60.9 % vs 77.2 %). No speed-up or efficiency ratio is claimed.

Other caveats: one seed per secure method; localhost only, hardware not in run artifacts; 103-bit truncation message unresolved (also printed by the Secure FF run); Secure FF validation/test counts are 10-19 below the Plain FF seed-42 run (cause not isolated; negative labels and arithmetic differ); H13 verifier false failure corrected offline on 24 Nov 2026 (audit_trail/); the Secure FF program, configuration, scripts and results were untracked in the research repository when recorded.

Administrative: author Abdelmonem Elsayed; submission date 15 January 2027; supervisors Dr. Nada Sharaf and Dr. Mayar Elfares; Abstract and Acknowledgments headings present with empty bodies (to be written by the student).

Next steps: aligned and repeated Secure BP / Secure FF runs (flags, scopes, checkpoint policy, seeds 43-46); per-operation profiling; one MPC-aware FF modification with ablation; truncation-domain analysis; commit Secure FF sources and evidence.
