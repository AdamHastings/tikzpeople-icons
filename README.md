This repository contains SVG and PDF renderings generated from the tikzpeople
LaTeX package.

tikzpeople is copyright 2016 Nils Fleischhacker and is licensed under
the LaTeX Project Public License 1.3.

These SVG and PDF files were generated from unmodified tikzpeople package files.
This repository is not maintained by the tikzpeople author. 

Lucidchart import note: the files in `svgs/` are direct `pdftocairo` vector
exports. Those exports reuse internal SVG IDs such as `clip-0` and
`linear-pattern-0` across files. Some diagram editors inline imported SVGs into
a shared document, which can make those IDs collide and cause icons to use the
wrong clip paths or gradients.

The files in `svgs_lucidchart/` prefix those internal IDs with the shape name.
This fixes cross-file ID collisions, but Lucidchart can still distort the icons
when it converts SVG gradients and nested clipping paths into its editable
internal format.

For Lucidchart fidelity, use `svgs_lucidchart_flat/` or import the PNGs in
`pngs_lucidchart/`. These are rendered from the PDFs at 600 dpi with a
transparent background, so they are not editable vector shapes, but they avoid
Lucidchart's gradient/clip-path conversion issues.
