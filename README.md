# hest

ASCII "hest" LaTeX package — provides `\hest` to include a bundled ASCII-art figure.

Status
------
This release (v1.0) is currently awaiting CTAN approval. In the meantime you can still use the package immediately by installing it locally or including it in a project (instructions below). Once the CTAN entry is available the package will be installable via standard TeX distributions.

Quick usage
-----------
Put the following in your document:


Usage:

```tex
\documentclass{article}
\usepackage{hest}
\begin{document}
\hest
\end{document}
```

Output:
```ascii
            .''
  ._.-.___.' (`\
 //(        ( `'
'/ )\ ).__. ) 
' <' `\ ._/'\
   `   \     \
```

Sometimes you just need to put a horse on it...

Files in this repository
------------------------
- `hest.sty` — LaTeX package
- `hest.txt` — bundled ASCII-art data file (plain UTF‑8, no BOM)
- `example.tex` — minimal example demonstrating `\hest`
- `LICENSE` — license text for the package
- `CHANGELOG.md` — release notes

How to use now (before CTAN approval)
----------------------------

1. Single-project use (simplest)
   - Copy `hest.sty` and `hest.txt` into your project folder (the same directory as your `.tex` file).
   - Compile normally (pdfLaTeX / XeLaTeX / LuaLaTeX / Overleaf).

2. System-wide local install (makes it available to all documents on your machine)
   - Place files in your local TEXMF tree, e.g.:
     - `.../texmf-local/tex/latex/hest/hest.sty`
     - `.../texmf-local/tex/latex/hest/hest.txt`
   - Refresh the file name database:
     - TeX Live / texmf-local: `sudo mktexlsr` (or `texhash`)
   - Now you may `\usepackage{hest}` from anywhere on that machine.

3. Overleaf
   - Upload `hest.sty` and `hest.txt` to your Overleaf project (use “Upload” or drag-and-drop).
   - Overleaf uses pdfLaTeX by default and the package will work there immediately.

Notes and compatibility
-----------------------
- The package uses `fancyvrb` to read and typeset the bundled ASCII art file verbatim; this avoids fragile verbatim-in-`.sty` issues.
- Works with pdfLaTeX, XeLaTeX and LuaLaTeX.
- Default vertical gap is controlled by `\hestsep` (set in `hest.sty`); change it in your document preamble as shown above.

CTAN and distribution
---------------------
- A CTAN upload for this package is pending review. Once approved, the package will be available from CTAN and will be picked up by TeX Live / MiKTeX in their next distribution cycles.
- CTAN package page (once live / for reference): https://ctan.org/pkg/hest
- Meanwhile you can use the local installation methods above or download the repository files directly from GitHub.

Report issues / contribute
----------
Repository & issues: https://github.com/yourusername/hest  
Feel free to open issues or PRs for improvements (e.g., package options, additional art files, documentation).

License
-------
MIT License — see `LICENSE` for details.

Author
------
FM Westby 
