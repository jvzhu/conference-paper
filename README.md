# Conference Paper

[![Build LaTeX Paper](../../actions/workflows/ci.yml/badge.svg)](../../actions/workflows/ci.yml)

A repository for drafting, revising, and submitting a conference paper.

## Contents

| File / Directory | Description |
|---|---|
| `paper.tex` | Main manuscript source (LaTeX) |
| `references.bib` | Bibliography database (BibTeX) |
| `figures/` | Images and diagrams used in the paper |
| `.github/workflows/ci.yml` | GitHub Actions workflow to compile the manuscript |
| `LICENSE` | Repository license |

## Workflow

1. **Draft** — edit `paper.tex` with your content
2. **References** — add citations to `references.bib`
3. **Figures** — place image files (`.pdf`, `.png`, `.eps`) in `figures/`
4. **Build** — push to GitHub; Actions will compile `paper.tex` to PDF automatically
5. **Revise** — iterate using pull requests for review and version tracking

## Local Build

You need a LaTeX distribution installed (e.g., [TeX Live](https://www.tug.org/texlive/) or [MiKTeX](https://miktex.org/)).

```bash
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex
```

Or with `latexmk`:

```bash
latexmk -pdf paper.tex
```

## CI Artifacts

Every successful build uploads `paper.pdf` as a GitHub Actions artifact named **`paper-pdf`**, retained for **30 days**. Download it from the [Actions tab](../../actions/workflows/ci.yml) after any successful run. The PDF is intentionally excluded from version control via `.gitignore`.

## Privacy and Data Note

> **Do not commit confidential, embargoed, or personally identifiable information.**
> This includes participant data, proprietary datasets, reviewer correspondence, or any content not cleared for public release.
> Treat every commit as potentially public, even in private repositories — access controls can change.

## Policy Note

> Release automation may prepare and validate builds, but human approval is required before submission.
> All significant actions (version tags, camera-ready uploads) must be auditable — including inputs, checks, decisions, and approvals.
> Automation reduces friction; it does not remove accountability.

## License

This repository scaffold is released under the [MIT License](LICENSE).

