# TEMPLATE_AUDIT.md (v0.3, 4 Nov 2026)
Source: file contents pasted by the student + `Overleaf` file-tree screenshot + the template-generated PDF. The original `.zip`/project was NOT supplied as files; `giu_logo.png` is therefore a **placeholder** in this build (replace with the real logo from your Overleaf copy).

## File tree (screenshot, confirmed)
figures/giu_logo.png; sections/{background,conclusion,introduction}.tex; abstract.tex, acknowledgments.tex, appendix.tex, bachelor.tex, references.bib, title_page.tex. No `images/` directory.

## Findings
| # | Finding | Verified how | Action in v0.1 |
|---|---|---|---|
| 1 | `\titlePage` is called twice with a blank page between (cover, blank, inner title page). The sample PDF shows two identical title pages. | Source + PDF | **Kept unchanged.** Cannot tell whether GIU requires it. Open question. |
| 2 | `\includefig*` macros point to `images/`, which does not exist; logo uses `figures/`. Macros unused in the template. | Source + screenshot | **Fixed**: macros now use `figures/`. |
| 3 | No Literature Review chapter. | Source | **Added** `sections/literature_review.tex`, included after Background. |
| 4 | `\pdfinfo` hard-codes `/CreationDate (D:20090707085533)`. | Source | **Removed** that line (metadata only). |
| 5 | Declaration item (iii) states AI was used only for language refinement. | Source/PDF | **Replaced by a visible `[AI-USE STATEMENT PENDING]` marker.** Original wording preserved here: "Artificial intelligence tools were used exclusively for language refinement and presentation purposes. No AI tools were used to generate research ideas, methodology, results, analysis, or conclusions. The author remains fully responsible for all content of this thesis." The student must check this against GIU policy and write an accurate statement. |
| 6 | Title in `\Huge` with `\doublespacing` would be very large for the long approved title. | Reasoning (not compiled at Huge) | Changed to `\LARGE` in `title_page.tex`; title fits on 3 lines. |
| 7 | `\listoftables` was commented out. | Source | Enabled (chapters now contain tables); entry added to ToC like List of Figures. |
| 8 | Math packages missing. | Needed for equations | Added `amsmath, amssymb`. |
| 9 | Abstract is not in the ToC (its `\addcontentsline` is commented out). Acknowledgments is, with page "V". | Compiled ToC | Left as template. |
| 10 | Acronym list sits in Appendix A ("Lists"), listed as a *section* in the ToC. | Compiled ToC | Left as template. `printonlyused` means `\acs{}` before any `\ac{}` use is undefined; avoided. |

## Build (this workspace)
`latexmk -pdf bachelor.tex` (pdfLaTeX + BibTeX, plain style). 36 pages. No undefined citations/references, no missing files, 0 BibTeX warnings, no overfull boxes after fixes. Remaining log lines are `acronym` package "Info" messages (harmless). Title page, declaration and two table pages were inspected visually; the rest was checked from text extraction and the log only.

## v0.3 updates
- Logo: `figures/giu_logo.png` remains a placeholder graphic (not the official logo); replace from the Overleaf copy.
- Title pages: two `\titlePage` calls preserved; author shown as `[confirm]`; date `XX January, 20XX`.
- PDF metadata: duplicate `\pdfinfo`/hyperref keys removed; `\hypersetup` sets title and subject only (author unset).
- Acronyms: `\acs{rq}` removed (plain "RQ"); LLM and STDP added; GPU not used as acronym.
- Appendix: `\phantomsection` added before the List entries to remove the hyperref bookmark-anchor warning.
- List of Figures suppressed (no figures); List of Tables kept.
- New `review_background_literature.tex`: same book class, 12pt A4, packages, plain BibTeX; Background + Literature Review + References + abbreviation list only.
