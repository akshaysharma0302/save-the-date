# Project Memory

Last updated: July 1, 2026

## Project

This is a static wedding save-the-date website for Akshay & Amrita.

Primary site file:

- `index.html`

Primary published URL:

```text
https://akshaysharma0302.github.io/save-the-date/
```

## Current Direction

The current visual and copy direction is:

- Elegant invitation feel rather than a generic event landing page.
- Soft blush, sage, cream, and warm gold palette.
- Natural, personal copy instead of formal wedding boilerplate.
- Canada framed as home.
- Delhi framed as roots, family, and the wedding location.
- Delhi travel suggestions should feel helpful and warm, not like a tourist brochure.

Current key copy themes:

- “Canada is home. We’re celebrating in Delhi.”
- “We’re getting married in Delhi.”
- Helpful, understated travel guidance for guests visiting Delhi for the first time.

## What Changed Recently

The site has been updated beyond the original static invitation version.

Recent major changes include:

- Mobile layout improvements across the page, especially the hero.
- Better mobile typography for the Akshay and Amrita names.
- Anchor scroll offset fixes so section jumps do not land too tightly against the previous section.
- Front-page hero now uses a custom background artwork image.
- Hero palette and button styling were adjusted to match the front-page background art.
- Added a Delhi visitor section before RSVP with landmark recommendations.
- Delhi visitor section now includes external planning/resource links.
- Delhi visitor images now use vertical tile styling so portrait-oriented images fit better.

## Current Site Features

The page currently includes:

- Hero section with custom background artwork, names, date, location, and action buttons.
- Calendar download button that generates an `.ics` invite.
- Google Maps link for Chattarpur, New Delhi.
- Wedding week section for Mehendi, Haldi, Sangeet, and Pheras.
- Canada/Delhi section.
- Countdown to January 31, 2027.
- Story section about Delhi, Canada, and the couple.
- Delhi first-time visitor section with landmark tiles and curated reading links.
- RSVP form that saves locally in the browser with `localStorage`.
- Optional music support. The music button only appears if `music.mp3` exists beside `index.html`.

## Delhi Visitor Section

The Delhi visitor section currently lives between the story section and the RSVP section.

It currently includes:

- `Akshardham Mandir`
- `Lotus Temple`
- `Qutub Minar`
- `Taj Mahal` as a nearby day-trip option

External links currently included there:

- Emma's Daydream: `Top 10 things to do in New Delhi`
- Sunshine Seeker: `The ultimate 2 day New Delhi itinerary`
- Condé Nast Traveller India: `Places to visit in Delhi that are not tourist traps`

## Assets

Primary hero artwork:

- `images/front-page-background.png`

Current Delhi trip images in use:

- `images/trip/akshardham-mandir.jpg`
- `images/trip/lotus-temple.jpg`
- `images/trip/qutub-minar.jpeg`
- `images/trip/taj-mahal.jpg`
- `images/trip/humayun-tomb.jpeg`
- `images/trip/red-fort.jpeg`

The Lotus Temple and Taj Mahal photos were converted from WebP to JPG for better compatibility on older or locked-down PCs.

Additional WebP originals still present:

- `images/trip/lotus-temple.webp`
- `images/trip/taj-mahal.webp`

Source-style/input asset currently still present:

- `input/images/front-page-background.png`

## Deployment Notes

GitHub Pages-related files currently present:

- `.github/workflows/pages.yml`
- `.github/workflows/jekyll-gh-pages.yml`
- `.nojekyll`
- `README.md`

The page itself is still rooted at `index.html`.

## Git State Note

Current local git state at the time of this memory update:

- Branch: `main`
- Local `main` is currently aligned with `origin/main`
- Untracked files currently include:
  - `images/trip/humayun-tomb.jpeg`
  - `images/trip/red-fort.jpeg`

Recent commits on `main`:

- `db042c3` `vertical tilt to the images`
- `7b53c26` `added delhi landmark things`
- `1c41c36` `changes added background`
- `668c884` `Improve mobile layout and anchor scrolling`

## File Structure

See `FILE_STRUCTURE.md` for the current repo layout and notes on what each path is used for.

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

Check the published site:

```sh
curl -I -L https://akshaysharma0302.github.io/save-the-date/
```
