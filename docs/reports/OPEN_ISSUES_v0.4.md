# OPEN_ISSUES_v0.4.md

## Research / technical
1. **Truncation-domain message (103 bits)** - UNRESOLVED. Source reading (Machine.hpp, TruncPrTuple.h, Replicated.hpp) suggests it reports that the low-round variant is unusable at 64 bits (k+40 > 64), not an error; the executed variant's cost, numerics and leakage are not analysed. Supersedes the v0.3 note (OPEN_QUESTIONS #9/#10). Needs independent review.
2. **Timing scope.** 933.263 s (party-0 timer, includes preprocessing, excludes compilation per source) vs 948.40 s (external, includes compile-run.py). 15.1 s difference not decomposed.
3. **Single seed.** Run seeds 43-46 and repeats; fix checkpoint policy (final epoch vs validation-selected) BEFORE running.
4. **Baseline provenance.** Plain BP seed-42 values are repository-recorded; baseline not re-run; plaintext hardware not recorded.
5. **Hardware of secure runs** not in run artifacts; WSL host was inspected afterwards only. Record host with every future run.
6. **A0 configuration.** A0 log suggests trunc_pr/split not enabled; A0 compile record unavailable; unverified.
7. **Repository state.** Input bundle was generated at commit 974e202 with a dirty tree; evidence commit is ef00de1. Archive complete logs in a controlled location (full.log hash now recorded).
8. Secure FF design, profiling, modification: not started.

## Literature / citations
9. Santos et al. (Curl, ePrint 2024/1127): only the abstract was checked (PDF fetch 403). Verify the exact functionality and leakage qualification before relying on it.
10. Truncation attribution: the pinned MP-SPDZ tree attributes the probabilistic truncation to "Dalskov et al." (README.md: ePrint 2019/131 and 2020/1330; Compiler/instructions.py: 2020/1330), while the implementation comment at Protocols/Replicated.hpp:452 cites ePrint 2018/403. The thesis currently makes no attribution (the Dalskov citation and bib entry were removed pending verification). Read the papers, map each ePrint number to its authors and title, then decide what to cite.
11. Refresh the literature search (last: 11 Oct 2026) and its recorded date.
12. Six proposal PDFs absent from the archive (v0.3 issue, unchanged); other metadata (ESMPC, SecP-Tuning, Comet etc.) not re-verified against publishers.

## Administrative (nothing guessed; all remain placeholders)
13. Author name: `Abdelmonem Sayed Abdelmonem [confirm]` vs `Somida` vs folder name - confirm with registration record.
14. Submission date, third supervisor, AI-use declaration, official GIU logo, double title page, acknowledgements: unchanged.
15. Abstract and conclusion are provisional/interim.

## Build
16. **Build.** The consolidated project was compiled once with Tectonic 0.15.0 (XeTeX engine, not pdfLaTeX): 81 pages, 9 chapters, 30 references, no unresolved references or citations in the final pass. Not yet done: a pdfLaTeX build in Overleaf, and visual inspection of the TikZ figures (Figures 4.1 and 5.1) and tables, because no PDF renderer was available to view pages. One overfull box of 1.8 pt remains (Results, Table 7.x row).
