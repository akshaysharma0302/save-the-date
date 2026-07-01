# Project Memory

Last updated: July 1, 2026

## Project

This is a static save-the-date website for Akshay & Amrita.

Main file:

- `index.html`

The site is designed to be hosted on GitHub Pages at:

```text
https://akshaysharma0302.github.io/save-the-date/
```

## Design Direction

The current preferred direction is:

- Clean, elegant wedding invitation style.
- No cartoon-like decorative SVGs.
- Subtle Indian wedding cues through jaali-style texture, mandap-inspired framing, warm gold/vermilion/mehendi accents, and restrained Delhi/Canada references.
- Canada should be framed as home.
- Delhi should be framed as family, roots, and the wedding location.
- Avoid forced phrasing like “from our home in Canada to Delhi.”
- Keep the copy natural and conversational.

Current key copy direction:

- “Canada is home. We’re celebrating in Delhi.”
- “We’re getting married in Delhi.”
- “Canada is home for us. Delhi still holds so much of our story…”

## Site Features

The page currently includes:

- Hero section with names, date, location, and action buttons.
- Calendar download button that generates an `.ics` file.
- Google Maps link for Chattarpur, New Delhi.
- Wedding-week sections for Mehendi, Haldi, Sangeet, and Pheras.
- Canada/Delhi section.
- Countdown to January 31, 2027.
- RSVP form that saves locally in the browser with `localStorage`.
- Optional music support. The music button only appears if `music.mp3` exists beside `index.html`.

## Deployment Setup

Files added for GitHub Pages:

- `.github/workflows/pages.yml`
- `.nojekyll`
- `.gitignore`
- `README.md`

The intended workflow is `.github/workflows/pages.yml`.

That workflow should publish the repository root, where `index.html` lives.

## Important GitHub Pages Status

The GitHub Pages deployment was still returning 404.

What was found:

- GitHub has `index.html`.
- The custom workflow `.github/workflows/pages.yml` uploaded the site successfully.
- The final Pages deploy step was stuck in progress.
- A second workflow, `.github/workflows/jekyll-gh-pages.yml`, was added directly on GitHub. It is not needed for this static HTML site.

Recommended fix:

1. Cancel any stuck Pages workflow runs in GitHub Actions.
2. Delete `.github/workflows/jekyll-gh-pages.yml` from GitHub.
3. Keep `.github/workflows/pages.yml`.
4. In `.github/workflows/pages.yml`, use:

```yaml
uses: actions/deploy-pages@v5
```

instead of:

```yaml
uses: actions/deploy-pages@v4
```

5. Commit the change.
6. Re-run the **Deploy GitHub Pages** workflow.

## Local Git State Note

Local branch and GitHub branch diverged:

- Local `main`: `8a7e9de Prepare static site for GitHub Pages`
- `origin/main`: `4fe782b Create jekyll-gh-pages.yml`

This happened because a workflow file was added directly on GitHub after the local commit.

Before making more commits, reconcile this carefully. The likely desired end state is:

- Keep the latest `index.html` from local.
- Keep `.github/workflows/pages.yml`.
- Remove `.github/workflows/jekyll-gh-pages.yml`.
- Update `actions/deploy-pages` to `v5`.

## Useful Commands

Preview locally:

```sh
python3 -m http.server 4173
```

Then open:

```text
http://localhost:4173/
```

Check JavaScript syntax:

```sh
node -e "const fs=require('fs'),vm=require('vm'); const html=fs.readFileSync('index.html','utf8'); const scripts=[...html.matchAll(/<script>([\s\S]*?)<\/script>/g)].map(m=>m[1]); for (const s of scripts) new vm.Script(s); console.log('inline scripts parse ok:', scripts.length);"
```

Check GitHub Pages URL:

```sh
curl -I -L https://akshaysharma0302.github.io/save-the-date/
```

