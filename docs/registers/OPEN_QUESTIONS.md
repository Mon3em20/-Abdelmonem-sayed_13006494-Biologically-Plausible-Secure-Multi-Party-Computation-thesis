# OPEN_QUESTIONS.md (v0.3) - genuine unresolved items only
1. **Author name / ID.** Proposal: "Abdelmonem Sayed Abdelmonem"; also "...Somida"; 13006494 appears only in a filename. Needed: registration record. Working title page shows the proposal name with `[confirm]`.
2. **Submission date.** Unconfirmed (5 Jan 2027 is the project deadline only).
3. **Third supervisor.** None confirmed; slot empty.
4. **AI-use declaration.** Original template wording is not accurate for this project; the true disclosure must be written after checking GIU policy. Working build shows a marker; review PDF omits it.
5. **Double title page** (cover, blank, inner title): GIU requirement or template artifact?
6. **Official GIU logo.** `figures/giu_logo.png` is a placeholder graphic.
7. **Hardware/network of secure runs.** Not recorded in artifacts (only: all parties on localhost). Needed before any cost claim is generalised.
8. **C0-C2 plaintext diagnostic results** are not in the available artifacts.
9. **Truncation path.** The dossier describes the ordinary TruncPrRing path as CdH10-fixed. In the pinned source `non_linear.trunc_pr` uses the native `trunc_pr` instruction (source cites Dalskov-Escudero-Keller) when bit-length conditions hold, and the compile log reports 7,424,425 integer probabilistic truncations, which suggests the native branch. The thesis names both families without asserting the executed branch. Needs a definitive trace.
10. **Run warning** in BP-COMP-001 output: 64-bit domain too small for low-round truncation (needs >=103 bits). Effect on executed path not analysed.
11. **Metadata `initial_parameter_sha256`** (BP-COMP-001) is a payload hash computed by bp_training_reference.py, not the file SHA-256; documented, not an error.
12. **A0 hash mismatch** (embedded vs actual runtime-log SHA-256) preserved unaltered.
13. **Not re-inspected in v0.3:** PDFs of Keller-Sun note, SecP-Tuning, Comet, DP-ULR, SpyKing, PrivateSNN (read by the author; not in the project archive); Zhou 2026 and Elnady 2026 (from the supplied dossier). Salam et al. full author list and ESMPC/other proceedings details to be checked against publisher records. ePrint 2024/1127 is mentioned in prose but not in the bibliography (author/title not supplied).
14. **Test-suite and verifier results** (24 tests, aggregate verifier) are reported, not re-run in this revision.
15. **Isolated ordering-vs-initialisation experiment** and multi-seed repetition are needed before any attribution or utility claim.
16. **Supervisor approval** of the chapter structure and citation style.

## Status update 24 November 2026 (items above keep their original wording)
- Items 1-3 (author name, submission date, supervisors): settled by the student - Abdelmonem Elsayed, 15 January 2027, Dr. Nada Sharaf and Dr. Mayar Elfares; no third supervisor. Registered name still to be checked against the GIU record by the student.
- Item 4 (AI-use declaration): the student decided to have no AI-use clause in the current Declaration.
- Item 5 (double title page): resolved by the student's decision to keep a single title page.
- Items 6, 9, 10, 13-16 remain open (logo, truncation path and message, unverified PDFs, ordering/initialisation experiment, supervisor approval).
- Item 7 (hardware/network): still unrecorded for both secure full runs.

New open questions:
17. **Compiler-flag confound.** Secure BP was compiled with `-l -M -E ring`, Secure FF with `-M -E ring`. Effect of `-l` on either program is unisolated.
18. **Measurement-scope alignment.** External wall time (compile included for Secure BP only) and RSS (tree maximum vs per-party maximum) must be aligned before any cost comparison.
19. **Secure FF vs Plain FF gap.** Seed-42 validation (608 vs 620) and test (609 vs 627) counts differ; negative labels and arithmetic differ; cause not isolated; no variance estimate.
20. **Repeated seeds.** Seeds 43-46 for Secure FF (inputs prepared) and Secure BP not run.
21. **Per-operation profiling (RQ2)** and **MPC-aware modification with ablation (RQ3)** not started.
22. **Checkpoint policy** for the controlled comparison (final epoch vs validation-selected) to be fixed.
23. **Evidence provenance.** Secure FF program, configuration, scripts and results were untracked in the research repository; they should be committed (by the student) so the hashes in the thesis appendix refer to a repository state.
24. **H13 verifier** checks existence, size and mtime of the protected inputs only, not contents.
