# courtney-johnson

Personal academic website for Courtney "CJ" Johnson, Ph.D. — optical physicist and
microscope developer (HHMI Janelia Research Campus).

Static HTML/CSS — no build step. Served by GitHub Pages.

## Structure

```
index.html              Home (hero, about, interests, research, publications, talks, beyond-the-bench, contact)
cv.html                 Full CV (print-to-PDF via the in-page button)
research/
  phase-diversity.html  Phase-diversity adaptive optics
  3d-trim.html          3D-TrIm single-virus tracking
  3d-fastr.html         3D-FASTR rapid point-scan imaging
assets/
  css/site.css          All styles
  img/                  Figures, logos, portraits, project + beyond-the-bench thumbnails
  video/                Visualization clips
.nojekyll               Tells GitHub Pages to serve files as-is (no Jekyll processing)
```

## Deploy

GitHub Pages → serve from the `main` branch root. The `.nojekyll` file disables
Jekyll so the static files are served verbatim. All asset paths are relative, so the
site works at `https://ceej640.github.io/courtney-johnson/`.

## Editing

- **Content & layout:** edit the `.html` files directly.
- **Styles:** `assets/css/site.css` (bump the `?v=NN` query on the stylesheet link in
  each HTML file to bust browser cache after a change).
- **CV:** edit `cv.html`; open it and use the "Save as PDF" button to regenerate a PDF.

Working/source files (`uploads/`, `screenshots/`) are git-ignored and not published.
