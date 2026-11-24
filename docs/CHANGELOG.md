# Changelog of the single master thesis project

This project (`D:\GIU_Bachelor_Thesis`) is the only active thesis. It replaces the earlier working folders `giu_thesis_v0.3` and `thesis_v0.4_current_progress_2026-11-16`, which are kept untouched as backups.

## 2026-11-16 - consolidation
- Sources taken from the v0.4 working folder (a strict superset of v0.3: all chapters rewritten or extended there; title page, acknowledgments, logo, template files identical in both).
- Entry point: `bachelor.tex` (pdfLaTeX / BibTeX plain). Nine chapters via `\include`: introduction, background, literature_review, methodology, implementation, setup, results, discussion, conclusion; plus abstract, acknowledgments, title page, appendix (Evidence Manifest), `references.bib` (30 entries, all cited).
- Version labels removed from the build files (hyperref subject now "working draft"); MP-SPDZ "v0.4.4" untouched.
- Fixes found by the first real compile: TikZ style `out` in Chapter 5 clashed with TikZ's `out` key (renamed `outbox`); appendix manifest table converted to `longtable` (was too tall/wide); path strings given break points; Table 7 seed header shortened; results table caption now points to the repository file `results/baselines/bp.csv` instead of the provenance CSV.
- Added `\usepackage{longtable}`.
- Not carried into the root: stale build outputs (`.aux`, `.bbl`, old PDFs), the standalone `review_background_literature.tex` and `acronyms_review.tex` (auxiliary only; remain in the v0.3 and v0.4 folders), duplicate registers.
- `docs/registers/` holds the registers (still describing v0.3 status except `RESULTS_PROVENANCE_MATRIX.csv`), `docs/reports/` the status/open-issue/changelog reports of the v0.4 pass, `docs/history_v0.3/` the v0.3 records, `docs/template/` template notes.

## Not done
- Registers (EXPERIMENT_REGISTRY, EVIDENCE_AND_CLAIM_REGISTER, DECISION_LOG, OPEN_QUESTIONS, PROJECT_KNOWLEDGE_BASE, STRUCTURE PLAN) still need migration to the current status.
- pdfLaTeX build and visual check of figures in Overleaf.
- Secure FF remains pending (not implemented, not run). Administrative placeholders (author name, date, supervisors, AI declaration) unchanged.

## 2026-11-24 - Secure FF update (in place; no new thesis version)
- Thesis chapters updated in place: introduction (status, objectives O3/O4, contributions), methodology (figure, comparison table C3/C3', Secure FF experiment, known confounds, evaluation policy, measurement definitions), implementation (Secure Forward-Forward Program, verification of the program, compile/run commands, status), setup (Secure FF configuration, difference table), results (Secure FF validation/test, weighted and per-sample loss, cost, phase-level, verification, Plain FF seed-42 reference, raw Secure BP vs Secure FF table), discussion (what the run establishes, preliminary comparison, RQ status, limitations), conclusion (interim), appendix (Secure FF evidence manifest). Background and literature review were searched for stale statements and left unchanged.
- Front matter: Abstract and Acknowledgments headings and TOC entries kept, bodies empty; single title page; Declaration clauses (i) and (ii) only.
- Registers updated: CURRENT_RESEARCH_STATUS (rewritten for 24 Nov 2026), EXPERIMENT_REGISTRY, RESULTS_PROVENANCE_MATRIX, EVIDENCE_AND_CLAIM_REGISTER (rows appended; the "Secure FF anything: Not implemented" row replaced), DECISION_LOG, OPEN_QUESTIONS, PROJECT_KNOWLEDGE_BASE, THESIS_STRUCTURE_AND_WRITING_PLAN (dated additions; earlier rows keep their wording). CHANGELOG_v0.4.md and OPEN_ISSUES_v0.4.md deliberately untouched (historical).
- Evidence read (read-only) from the research repository, `results/mpc/ff/matched/SECURE-FF-MATCHED-v1/`: seed42_run_20261122_212319, rehearsal_mini_run_20261122_212103, comparison_post_run, reference, audit_trail. No MPC program, training job or compilation was run.
- Not done: PDF build (no TeX engine available in this environment).
