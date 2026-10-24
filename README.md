# Md. Abdullah Al-Fahim — academic website

A personal academic site built with [Jekyll](https://jekyllrb.com/) and the open-source
[al-folio](https://github.com/alshedivat/al-folio) theme (MIT licence, see `LICENSE`).
It has four parts: **about**, **research**, **publications** and **cv**.

## Publish it on GitHub Pages

1. Your repository is `Fahim9646/fahim9646.github.io`; push the contents of this folder to its `main` branch.
2. In the repository go to **Settings → Pages → Build and deployment** and set **Source** to **Deploy from a branch**, branch **`gh-pages`**, folder **`/ (root)`**.
   (The workflow in `.github/workflows/deploy.yml` builds the site on every push and writes the result to the `gh-pages` branch. The first run takes a few minutes; check the **Actions** tab.)
3. `url` in `_config.yml` is already set to `https://fahim9646.github.io`.
4. Your site will be live at `https://fahim9646.github.io`.

## Things to fill in

| What | Where |
|---|---|
| GitHub, LinkedIn, Google Scholar, ORCID links | Uncomment and fill the lines in `_data/socials.yml` |
| CV PDF | Put it at `assets/pdf/CV_Md_Abdullah_Al-Fahim.pdf`. It then appears at the bottom of the home page and on the CV page. Nothing shows until the file exists. |
| Graduation year, extra skills, references | `_data/cv.yml` |
| Favicon | `assets/img/favicon-circle.png` |

## Updating content

- **Bio and headline:** `_pages/about.md`
- **Research cards on the home page:** `_includes/sections/research.liquid` (images in `assets/img/research/`)
- **Publications:** `_bibliography/papers.bib`. The page lists `@inproceedings` and `@article` entries under **published** and `@unpublished` entries under **in preparation**. When the DEM manuscript is accepted, change `@unpublished` to `@article`, add `journal`, `volume`, `pages`, `doi` and `html`, drop the `note`, and change `abbr`. Then update the status line and add figures to its card in `_includes/sections/research.liquid`.
- **CV:** `_data/cv.yml`

## Preview locally (optional)

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

Requires Ruby 3.x and ImageMagick (used to create responsive images).
