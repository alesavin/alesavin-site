# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio/resume website for Alex Savin. No build system, package manager, or framework is involved — it's plain HTML, CSS, and JavaScript served directly.

## Development

To preview locally, serve the root directory with any static file server, e.g.:

```bash
python3 -m http.server 8080
```

There are no build, lint, or test commands.

## Architecture

Single-page site (`index.html`) using Bootstrap 3 (vendored in `css/` and `js/`). Custom styles live in `css/alesavin.css`.

- `cv/` — PDF/DOC resume files; `cv/links.sh` creates symlinks to the current version
- `img/` — Profile photos (circle-cropped)
- `fonts/` — Bootstrap Glyphicons font files

The page embeds Google Analytics (ID: `G-V5VZFRWXK2`) and a Twitter timeline widget.

## Common Maintenance Tasks

- **New CV**: Add the PDF to `cv/`, update the symlink in `cv/links.sh`, and update the download link in `index.html`
- **Profile photo**: Add new image to `img/`, update the `<img>` src in `index.html`
- **Copyright year**: Update the year in the `<footer>` of `index.html`
