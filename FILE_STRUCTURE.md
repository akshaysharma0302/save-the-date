# File Structure

Last updated: July 1, 2026

## Overview

```text
save-the-date/
├── .github/
│   └── workflows/
│       ├── jekyll-gh-pages.yml
│       └── pages.yml
├── .gitignore
├── .nojekyll
├── FILE_STRUCTURE.md
├── PROJECT_MEMORY.md
├── README.md
├── images/
│   ├── front-page-background.png
│   └── trip/
│       ├── akshardham-mandir.jpg
│       ├── humayun-tomb.jpeg
│       ├── lotus-temple.jpg
│       ├── lotus-temple.webp
│       ├── qutub-minar.jpeg
│       ├── red-fort.jpeg
│       ├── taj-mahal.jpg
│       └── taj-mahal.webp
├── index.html
├── input/
│   └── images/
│       └── front-page-background.png
└── main.py
```

## Path Notes

- `index.html`
  - Main site file. Most styling, markup, and behavior live here.

- `images/front-page-background.png`
  - Active hero background artwork used on the front page.

- `images/trip/`
  - Delhi visitor/travel image assets.
  - Current in-use images:
    - `akshardham-mandir.jpg`
    - `lotus-temple.jpg`
    - `humayun-tomb.jpeg`
    - `qutub-minar.jpeg`
    - `red-fort.jpeg`
    - `taj-mahal.jpg`

- `input/images/front-page-background.png`
  - Source or earlier storage location for the hero art.
  - The live page currently uses the copy in `images/`.

- `PROJECT_MEMORY.md`
  - Ongoing project state, design direction, feature notes, and recent git context.

- `FILE_STRUCTURE.md`
  - Repo layout reference.

- `README.md`
  - Local preview and deployment instructions.

- `.github/workflows/pages.yml`
  - GitHub Pages workflow intended for the static site.

- `.github/workflows/jekyll-gh-pages.yml`
  - Additional Pages-related workflow file currently present in the repo.

- `.nojekyll`
  - Prevents GitHub Pages from treating the site like a Jekyll project.

- `main.py`
  - Present in the repo root but not part of the static site flow.

## Working Notes

- This is still a simple static site project, not a framework app.
- There is no asset pipeline; image paths are referenced directly from `index.html`.
- If more Delhi travel tiles are added later, `images/trip/` is the natural place for them.
