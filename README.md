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

## RSVP responses

The RSVP form is ready to send submissions through Formspree, which works with GitHub Pages and does not need a backend.

1. Create a form at [Formspree](https://formspree.io/).
2. Copy the form endpoint. It will look like:

```text
https://formspree.io/f/abcdwxyz
```

3. Open `index.html` and find:

```js
const RSVP_FORM_ENDPOINT='';
```

4. Paste the endpoint between the quotes:

```js
const RSVP_FORM_ENDPOINT='https://formspree.io/f/abcdwxyz';
```

Until that endpoint is filled in, the RSVP is only saved in the guest's browser.

## Changing the address

Open `index.html` and find the `eventDetails` object. Update these fields:

```js
location:'New Delhi, India',
shortLocation:'Delhi',
mapQuery:'New Delhi India',
description:"Akshay and Amrita are getting married in New Delhi, India. We'd love to celebrate with you."
```

`location` updates the visible venue text and calendar location. `mapQuery` controls the Open map button. `shortLocation` is used in the RSVP thank-you message.

## Optional music

If you want the music button to appear, add a `music.mp3` file beside `index.html`.
