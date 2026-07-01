# Akshay & Amrita Save the Date

Static wedding save-the-date site for GitHub Pages.

## Local preview

Open `index.html` directly, or run:

```sh
python3 -m http.server 4173
```

Then visit `http://localhost:4173/`.

## GitHub Pages

This repo includes a GitHub Actions workflow that publishes the site from the repository root.

After pushing to `main`, enable Pages in GitHub:

1. Go to the repository on GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. The site will publish at:

```text
https://akshaysharma0302.github.io/save-the-date/
```

## Optional music

If you want the music button to appear, add a `music.mp3` file beside `index.html`.

