# REVISION_REPORT.md (v0.2 -> v0.3)
| File | Problem | Revision | Source/evidence | Status |
|---|---|---|---|---|
| background.tex | MLP equation applied activation to output layer | Hidden layers use sigma; output linear logits; BP indices consistent; delta^(L)=p-e_y only for softmax-CE | Standard derivation | Fixed |
| background.tex | Exact RSS multiplication message/round claim | Formula labelled illustrative; exact pattern not asserted; Shamir/additive/RSS/trusted-dealer kept distinct | Dossier | Fixed |
| background.tex | Ambiguous fixed-point notation | round(2^f x); sfix(16,31) range ~[-16384,16384), step 2^-16 | Pinned MP-SPDZ source (set_precision) | Fixed |
| background.tex | Truncation/use_split claims, leakage | Probabilistic truncation described per source; leakage qualified; ePrint 2024/1127 not over-generalised; use_split = three-way share split, not party count | Pinned source | Fixed; executed branch unresolved (OPEN 9) |
| background.tex | "Computation = wall-clock" | Cost terminology section rewritten; compiler VM rounds not online rounds | Dossier | Fixed |
| background.tex | Unsupported numbers (0.03/67 s, 30%, 70-94%, 63%, 73%) | Removed | Not in dossier | Fixed |
| background.tex, all chapters | \pending markers / editor language | Removed from reader-facing chapters (kept only in working conclusion placeholder) | - | Fixed |
| literature_review.tex | "Six papers not read" | Replaced: all read by the author; PDFs absent from project archive | Student statement | Fixed |
| literature_review.tex | SWIFT scope | LR training/inference + DNN inference (LeNet, VGG16); DNN training future work (not "no DNN") | arXiv 2005.10296 text + dossier | Verified |
| literature_review.tex | SpyKing "FHE inference only" | PyTorch training then BFV evaluation; decrypt/re-encrypt around nonlinear layers; FHE not MPC | Dossier + online record | Fixed |
| literature_review.tex | SecP-Tuning 73%, Comet scope, ESMPC 29-65% | 73% removed; abstract figures used; Comet = inference; ESMPC abstract-level figures with baseline | Dossier | Fixed |
| literature_review.tex | Missing recent work; gap wording | Added Zhou 2026, Elnady 2026; gap narrowed to matched FF-vs-BP under one MPC configuration | Dossier | Fixed |
| references.bib | 26 entries with editorial notes; wrong Comet pages | Rewritten: 28 entries, no audit notes, Comet pages 2827-2845, full author lists | Dossier + prior verification | Fixed; some metadata to confirm (OPEN 13) |
| results.tex | "15 runs per method" for accuracy | 5 seeds (accuracy, SD) vs 15 timing observations separated; spread statistic confirmed as sample SD | benchmark.py, summary.csv | Fixed |
| results/discussion | "Three secure runs agree with FP64" | FP64 agreement attributed to BP-COMP-001 only | BP-COMP-001/fp64_reference.json | Fixed |
| methodology/impl/setup | BP-COMP-001 not reflected; hardware unknown | Added configuration, init details, artifact paths; hardware stated as unrecorded (localhost) | Raw artifacts | Fixed |
| bachelor.tex | Duplicate PDF metadata | hypersetup only; author unset | Template | Fixed |
| appendix.tex | Bookmark anchor warning; empty LoF; undefined acronyms | phantomsection; LoF suppressed; acronyms audited | Build log | Fixed |
| review_background_literature.tex | No advisor-review build | New entry point, same class/packages/style; no title page, declaration, placeholders | - | Added |
| Unresolved | Author/ID/date, AI declaration, logo, double title page, hardware, C0-C2, truncation branch | Logged in OPEN_QUESTIONS.md | - | Open |
