# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A static, single-page HTML/CSS résumé (CV) site for Orlando Chirinos, written in Spanish, meant to be published via GitHub Pages. There is no build system, package manager, framework, or test suite — it's plain HTML/CSS.

## Files

- `index.html` — the entire CV content (single page, no JS).
- `styles.css` — all styling; uses CSS custom properties (`:root` vars like `--bg`, `--accent`, `--max`) for the dark theme and layout.
- `assets/Orlando-Chirinos-CV.docx` — the downloadable CV, linked from the "Descargar CV" button in `index.html`. If this file is renamed, update the corresponding `href` in `index.html`.

## Working locally

No build step — open `index.html` directly in a browser, or serve the directory with any static file server (e.g. `python -m http.server`) to preview.

## Deployment

Published via GitHub Pages, deploying from the `main` branch at `/ (root)`. Pushing to `main` is sufficient to publish — there is no CI/build pipeline.

## Editing notes

- Content is in Spanish; keep new content consistent with that.
- Section numbering in `index.html` (`<span>01</span>`, `<span>02</span>`, ...) is manual — renumber siblings if a section is added, removed, or reordered.
- Color/spacing tokens are centralized in `:root` in `styles.css` — prefer reusing those variables over hardcoding new values.
