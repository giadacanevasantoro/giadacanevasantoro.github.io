# giadacanevasantoro.github.io

Personal / research site. Plain HTML + CSS, no build step, no framework — GitHub Pages serves it as-is.

## Publish it

1. Create a new **public** GitHub repo named exactly `giadacanevasantoro.github.io` (the `username.github.io` name is what makes GitHub Pages serve it at the root domain instead of a `/reponame/` subpath — it must match your GitHub username exactly).
2. Push these files to the repo's default branch (`main`):
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/giadacanevasantoro/giadacanevasantoro.github.io.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages** and confirm the source is "Deploy from a branch", branch `main`, folder `/ (root)`. For a `username.github.io` repo this is usually already selected by default.
4. Wait a minute or two, then visit `https://giadacanevasantoro.github.io`.

No Jekyll config, no `_config.yml`, nothing to install — it's just static files.

## Structure

```
index.html              Home / bio
research.html           Research overview, links to the demo below
publications.html       Publication list
talks.html              Talks, teaching, outreach, CV link
assets/style.css        Shared stylesheet (light + dark mode)
demos/reading-the-remnant.html   Interactive QNM explainer (self-contained, no dependencies on the rest of the site)
```

## Before you publish, fill in

Every placeholder is marked with a dashed "Fill in" callout on the page itself, and also listed here:

- **index.html** — email address (`mailto:` link), ADS/INSPIRE profile URL, ORCID URL, Google Scholar URL.
- **talks.html** — add a real CV PDF to the repo root (or a `files/` subfolder) and point the "Download CV" link at it. Check the seminar/school/outreach list against your actual record — it was drafted from memory and may have wrong dates or missing items.
- **publications.html** — this list only has two papers plus one in-prep item. Replace it with your full list from ADS or INSPIRE; keeping ADS/INSPIRE as the canonical source and this page as a curated subset is also reasonable.
- **research.html** — expand each project paragraph in your own words; I kept these short and may have oversimplified.

## Adding more pages later

Copy any existing page as a template — the `<nav>` block, fonts link, and `assets/style.css` link at the top are identical across pages except for which nav item has `aria-current="page"`. Reusable components (`.card`, `.pub`, `.tl-item`, `.todo`, `.pill-link`) are documented by example in `research.html`, `publications.html`, and `talks.html`.

## The demo page

`demos/reading-the-remnant.html` is fully self-contained (inline CSS/JS, no external calls except Google Fonts) — you can open it directly, embed it via `<iframe>` elsewhere, or link to it as-is, as `index.html` and `research.html` already do.
