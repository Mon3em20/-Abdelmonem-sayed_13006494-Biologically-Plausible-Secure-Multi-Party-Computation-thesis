# DECISION_LOG.md (v0.3)
| Decision | Status | Note |
|---|---|---|
| Title = exact approved proposal title (no "(MPC)") | Confirmed | Proposal cover |
| Supervisors: Dr. Nada Sharaf, Dr. Mayar Elfares; third slot empty | Confirmed | |
| FF mandatory; SNN/gating/extra datasets optional | Confirmed | Proposal |
| Stages A-F are workflow labels, not chapters | Confirmed | Student instruction |
| Chapter plan 1-9 (Intro ... Conclusion) | Proposed, pending supervisor | |
| Protocol: MP-SPDZ v0.4.4 (commit 113c4e47...), Rep3 ring, 3 parties, semi-honest honest majority, 64-bit | Current working choice | |
| sfix(16,31), probabilistic truncation, use_split(3) | Current working choice (path defaults) | Source-verified |
| sfix.round_nearest | Candidate (not used) | Separate from selected configuration |
| Per-party shuffled order, ordering seed 42042 | Selected for BP-COMP-001 | Confounded with init; not a proven improvement |
| He (hidden, normal, var 2/784) + Xavier uniform (output, limit sqrt(6/18)) + zero biases, init seed 42 = C3 | Selected for BP-COMP-001 | Chosen from plaintext C0-C3; C0-C2 numbers unavailable; no per-factor attribution |
| Alternatives to C3 (other initialisers/orders) | Candidates / not selected | |
| Causal comparison of A0/A1/BP-COMP-001 runtime or communication | Rejected | Capture/conditions not shown comparable |
| Keep two \titlePage calls | Current working choice | GIU requirement unknown |
| Keep plain BibTeX style | Current working choice | |
| Omit declaration/title page from review PDF | Current working choice | AI statement unresolved |
| Suppress List of Figures until figures exist | Current working choice | |
| Cite Zhou 2026 and Elnady 2026 as supplementary (not among proposal 23) | Current working choice | |
