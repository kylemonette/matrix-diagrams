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

## Contents of Repository

- `matrixdiagrams.sty` &mdash; the package itself; add `\usepackage{matrixdiagrams}` to use it.
- `matrixdiagrams.tex` &mdash; source for the manual (quick reference plus a runnable example of every command).
- `matrixdiagrams.pdf` &mdash; the compiled manual.
- `LICENSE` &mdash; the project's MIT License.

## Contributing

This project continues to be a work in progress as more commands are added, and existing ones are revised.
Everyone is welcome to make a PR and contribute!

## License

This project is licensed under the [MIT License](LICENSE).