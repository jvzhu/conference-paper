# figures/

Place all image and diagram files for the paper in this directory.

## Supported formats

| Format | Notes |
|--------|-------|
| `.pdf` | Preferred for vector graphics (plots, diagrams) |
| `.eps` | Alternative vector format |
| `.png` | Raster images (screenshots, photographs) |
| `.jpg` | Photographs where file size matters |

## Usage in `paper.tex`

The `graphicspath` is already set to `figures/`, so you can include
a file called `overview.pdf` like this:

```latex
\begin{figure}[htbp]
  \centering
  \includegraphics[width=\linewidth]{overview.pdf}
  \caption{Caption text here.}
  \label{fig:overview}
\end{figure}
```

## Tips

- Export plots at **300 dpi** or higher for print quality.
- Use descriptive filenames (`overview.pdf`, `results-bar.pdf`).
- Keep source files (e.g., `.svg`, scripts) in a `figures/src/` subdirectory.
