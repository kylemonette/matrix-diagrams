# Matrix Diagrams

### Author: Kyle Monette, [kylemonette.github.io](https://kylemonette.github.io)

#### Updated: August 14, 2026

---
`matrixdiagrams` is a LaTeX package that draws schematic matrix diagrams in TikZ for the purposes of illustrating structure in matrices.

Every diagram is built with one command,
`\matrixdiagram{...}`, which takes as input a sequence of drawing commands (`\mdFill`, `\mdLabel`,
`\mdDiagBand`, etc.) working in a normalized coordinate system that
automatically adapts to the diagram's scale and aspect ratio.

This easily allows one to visualize structure in matrices such as bidiagonal, tridiagonal, upper triangular, and Hessenberg varieties.

## Sample Use

| Command | Draws |
| --- | --- |
| `\matrixdiagram[2]{\mdBlank}` | An empty bracketed matrix, twice as tall as wide. |
| `\matrixdiagram{\mdDiagBand}` | A tridiagonal band. |
| `\matrixdiagram{\mdHessenberg}` | An upper-Hessenberg outline. |
| `\matrixdiagram{\mdFill[red!20]{0}{0.5}{1}{1}}` | The top half of the matrix shaded red. |
| `\matrixdiagram{\mdLabel{0.5}{0.5}{A}}` | The label $A$ centered in the matrix. |

See `matrixdiagrams.pdf` for the full command reference and a runnable example
of every command.

## Requirements

`matrixdiagrams` requires a standard LaTeX2e installation plus:

- `tikz`
- `xparse`
- `calc`

All three ship with any full TeX distribution (TeX Live, MiKTeX, MacTeX).

## Installation

**From CTAN (once accepted):** install `matrixdiagrams` through your TeX
distribution's package manager (`tlmgr install matrixdiagrams`, MiKTeX's
package manager, etc.).

**From this repository:** the package is distributed as a `.dtx`/`.ins` pair,
the standard format for LaTeX packages. To build and install it by hand:

```sh
tex matrixdiagrams.ins        # generates matrixdiagrams.sty
pdflatex matrixdiagrams.dtx   # generates matrixdiagrams.pdf (run twice)
```

Then move `matrixdiagrams.sty` into a directory TeX searches (for example,
your local texmf tree, or simply the same folder as your `.tex` document).

## Contents of Repository

- `matrixdiagrams.dtx` &mdash; the documented source: package code and manual
  text in one file, following the standard LaTeX `.dtx` literate-programming
  format. This is the canonical source; edit this, not the generated files
  below.
- `matrixdiagrams.ins` &mdash; the installer script that extracts
  `matrixdiagrams.sty` from `matrixdiagrams.dtx` via `tex matrixdiagrams.ins`.
- `matrixdiagrams.sty` &mdash; the generated package; add
  `\usepackage{matrixdiagrams}` to use it.
- `matrixdiagrams.pdf` &mdash; the generated manual (quick reference plus a
  runnable example of every command, plus the annotated source).
- `LICENSE` &mdash; the project's MIT License.

## Contributing

This project continues to be a work in progress as more commands are added, and existing ones are revised.
Everyone is welcome to make a PR and contribute! Edit `matrixdiagrams.dtx`
(not `matrixdiagrams.sty`, which is generated from it) and regenerate the
`.sty`/`.pdf` as described in Installation above before committing.

## License

This project is licensed under the [MIT License](LICENSE).