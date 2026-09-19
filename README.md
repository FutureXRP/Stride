# Stride

Run/walk interval timer with voice cues, GPS pace, a pace calculator and a mileage log. It is a single HTML file with no build step and no backend; runs and settings are saved in the browser.

## Open the app

**https://futurexrp.github.io/Stride/**

On a phone, open that link in Safari or Chrome, then use *Share → Add to Home Screen* so it launches like a regular app.

## Hosting

The site is served by GitHub Pages from the `index.html` at the root of this repository. A workflow in `.github/workflows/pages.yml` redeploys it on every push to `main`.

One-time setup (repo admin): go to **Settings → Pages** and set **Source** to **GitHub Actions**. The next push to `main` (or a manual run of the "Deploy to GitHub Pages" workflow) publishes the site.

## Run it locally

Any static file server works, for example:

```sh
python3 -m http.server 8000
```

then open http://localhost:8000/. GPS, the screen wake lock and voice cues need a secure context, which localhost and the Pages URL both provide.
