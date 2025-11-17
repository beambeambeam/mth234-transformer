# Transformer: Linear Algebra That Understands Human Language

MTH234 final project report documenting the mathematical foundations of transformer architectures and the associated LaTeX build artifacts.

## Project Layout

- `main.tex` – root LaTeX source that assembles all chapters in `chapters/`.
- `arxiv.sty` – custom style file used by the report.
- `compile.sh` – helper script that runs the XeLaTeX compilation flow end-to-end.
- `main.pdf` – output that results from a successful build (not tracked if you rebuild locally).

## Prerequisites

1. Install a full TeX distribution (TeX Live or MacTeX) that includes `xelatex` and the fonts required by the document (XeLaTeX is mandatory because the report mixes English and Thai text).
2. Ensure the TeX binaries are on your `PATH` so the shell can find `xelatex`.
3. macOS runners should grant the terminal permission to access fonts the first time XeLaTeX executes.

## Build & Preview

1. From the workspace root `/Users/beam/Workspace/Project/mth234-transformer`, make the script executable (one time):
   - `chmod +x compile.sh`
2. Compile the paper (runs XeLaTeX twice for references):
   - `./compile.sh`
3. Open the generated PDF for review:
   - `open main.pdf` (macOS) or use your preferred PDF viewer.

## Troubleshooting

- **Missing fonts/packages**: run `tlmgr install <package>` or use the TeX Live Utility GUI to add whatever XeLaTeX reports as missing.
- **Stale auxiliary files**: remove build artifacts with `rm -f *.aux *.log *.out *.toc` before re-running `compile.sh`.
- **Script fails with permission denied**: re-run `chmod +x compile.sh` or invoke the script via `bash compile.sh`.

Once teammates can compile locally, they can edit the chapter files under `chapters/` and rerun the same build steps to regenerate `main.pdf`.
