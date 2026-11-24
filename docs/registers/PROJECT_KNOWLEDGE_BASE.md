# PROJECT_KNOWLEDGE_BASE.md (v0.3, 4 Nov 2026)
**Title:** Biologically Plausible Secure Multi-Party Computation for Efficient Privacy-Preserving AI Training I. GIU, Faculty of Informatics and Computer Science, B.Sc. CS (IT Security). Supervisors: Dr. Nada Sharaf (Egypt), Dr. Mayar Elfares (Germany). Author name/ID/date: unresolved (OPEN_QUESTIONS.md).
**RQs:** as in the approved proposal (main question; RQ1 comparison, RQ2 bottlenecks, RQ3 co-design). FF is the mandatory primary mechanism; SNN etc. optional. No new protocol/security model.
## Status
| Item | Status |
|---|---|
| Stage A | Complete |
| Stage B (bounded secure BP prototype) | Complete (feasibility gate met; low utility on 30-example sets is a limitation) |
| BP-COMP-001 | Completed; raw artifacts inspected in v0.3 (single run) |
| Stage C secure FF | Implemented, executed (seed 42) and verified 24 Nov 2026 (SECURE-FF-MATCHED-v1); single seed |
| Stage D profiling (BP and FF) | Not started |
| Stage E modification + ablation | Not started |
| Stage F optional | Not started |
| Main secure BP-vs-FF comparison | Preliminary raw single-seed values only; not controlled (flags, scopes, workload, checkpoint policy differ) |
## Evidence in hand
Repository (graduation-mpc-ff) and BP-COMP-001 directory inspected; pinned MP-SPDZ source (commit 113c4e47...) fetched and read for sfix, truncation and split semantics. PT-BENCH-v1 spread = sample SD over 5 seeds. Hardware/network not recorded (localhost). `figures/giu_logo.png` is a placeholder, not the official logo. Literature: 23 proposal references (all read by the author; six PDFs absent from the project archive) + Zhou 2026 + Elnady 2026 (supplementary) + Salam, He, Glorot. Registers: EXPERIMENT_REGISTRY.csv, EVIDENCE_AND_CLAIM_REGISTER.csv.

## Update 24 November 2026
Secure FF seed 42: 60.9 % test (609/1000), selected layer-2 epoch 1 (608/1000 val); 253.451 s MP-SPDZ time; 14,748.1 MB global; 1,799,138 party-0 rounds; 240.3 MB max party RSS; 13/13 hard checks, 17/17 bands. Secure BP seed 42: 77.2 %, 933.263 s, 5,224.49 MB. No speed-up or efficiency claim. Author Abdelmonem Elsayed; date 15 January 2027. Abstract/Acknowledgments deferred (empty bodies). See docs/reports/CURRENT_RESEARCH_STATUS.md.
