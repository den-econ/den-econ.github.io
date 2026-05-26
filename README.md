# DEN Economics Lab — website

Source for [den-econ.github.io](https://den-econ.github.io), the public site
for DEN Economics Lab (the research arm of Indonesia's Dewan Ekonomi Nasional).

Built with [Quarto](https://quarto.org).

## Local development

```bash
# Install Quarto from https://quarto.org/docs/get-started/
quarto preview         # live-reloading dev server
quarto render          # build static site into _site/
```

## Project layout

```
_quarto.yml            # site config + navigation
theme.scss             # custom DEN-branded SCSS (colors from fig-den)
styles.css             # small CSS overrides
index.qmd              # home page
research.qmd           # publications & projects
people.qmd             # team
news/
  index.qmd            # blog listing
  posts/               # one folder per post
```

## Publishing

A GitHub Actions workflow (`.github/workflows/publish.yml`) renders the site
and publishes it to the `gh-pages` branch on every push to `main`. Make sure
GitHub Pages is set to serve from the `gh-pages` branch in repo settings.

## Adding a news post

```bash
mkdir news/posts/YYYY-MM-slug
# then create news/posts/YYYY-MM-slug/index.qmd with the front-matter below
```

```yaml
---
title: "Post title"
description: "One-line teaser shown on the listing."
date: "YYYY-MM-DD"
categories: [tag-one, tag-two]
author: "DEN Economics Lab"
---
```

## Brand colors

The custom SCSS theme uses the official DEN palette from
[`fig-den`](https://github.com/den-econ/fig-den). When updating the palette,
keep `theme.scss` and `fig-den/fig_den.py` aligned.
