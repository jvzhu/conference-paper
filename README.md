# Conference Paper

A repository for drafting, revising, and submitting a conference paper.

## Contents

| File / Directory | Description |
|---|---|
| `paper.tex` | Main manuscript source (LaTeX) |
| `references.bib` | Bibliography database (BibTeX) |
| `figures/` | Images and diagrams used in the paper |
| `.github/workflows/ci.yml` | GitHub Actions workflow to compile the manuscript |

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

## Policy Note

> Release automation may prepare and validate builds, but human approval is required before submission.
> All significant actions (version tags, camera-ready uploads) must be auditable — including inputs, checks, decisions, and approvals.
> Automation reduces friction; it does not remove accountability.
