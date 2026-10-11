# Checking AI-Generated Proofs: The Human Friendly Form

Siddharth Iyer, October 2026

A short note proposing a way for a human to convince themselves, by reading, that an AI-generated proof is correct, without relying on a proof assistant. It comes with a prototype of the interactive map it describes.

## Contents

| File | What it is |
|---|---|
| `checking_ai_proofs_v2.pdf` | The note (version 2). |
| `checking_ai_proofs_v2.tex` | Its LaTeX source. |
| `hff_map_example.html` | The interactive map for the worked example in Section 7 (infinitely many primes ≡ 3 mod 4). Open it in any web browser. |

## The idea in brief

- The AI writes its proof in **Human Friendly Form (HFF)**: a plain-English overview; then, after the mark ✠, a proof made only of definitions, lemmas and remarks, with each lemma proved directly below its statement in fewer than *L* visible characters of the compiled document (default *L* = 300, formulas included); and finally a list of references.
- If every block is checked, taking the statements it cites as given, the main theorem is proved.
- A separate **map** shows the dependency graph like the map of a strategy game: pan, zoom, travel to the main theorem, open any block. Unverified blocks lie under dense fog. A verified block that still depends on unverified blocks lies under light fog. A block with no fog over it is proved, and when no fog is left anywhere, the main theorem is proved.

## Building the PDF

Run `pdflatex checking_ai_proofs_v2.tex` twice. The note uses standard packages (amsmath, amssymb, tikz, tcolorbox, hyperref, cleveref, enumitem, booktabs, tabularx, microtype, and lmodern when available).

## Using the map

Drag to pan, scroll or pinch to zoom, click a block to open it. Keys: **T** travels to the theorem, **F** shows the whole map, **/** searches, **V** marks the open block verified or unverified again. Your marks are kept in your browser. Formulas are typeset with MathJax when you are online, and shown as plain text otherwise.

## Acknowledgements

The core idea is the author's. Claude, an AI model developed by Anthropic, wrote up the note and built the map under the author's direction; see the note's acknowledgements for details.

## License

Apache License 2.0; see `LICENSE`.
