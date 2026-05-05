# den-econ.github.io

Website for **DEN Economics Lab** at Universitas Indonesia, built with [Quarto](https://quarto.org) and deployed via GitHub Pages.

## Structure

| File | Purpose |
|------|---------|
| `_quarto.yml` | Site configuration (title, navbar, theme) |
| `index.qmd` | Home page |
| `research.qmd` | Research areas, working papers, publications |
| `people.qmd` | Faculty, researchers, and students |
| `news.qmd` | News and events |
| `contact.qmd` | Contact information and FAQ |
| `styles.css` | Custom style overrides |

## Editing content

All pages are written in **Markdown** (`.qmd` files). To update a page, open
the relevant `.qmd` file and edit the text directly — no HTML knowledge needed.

## Deployment

Pushing to `main` automatically triggers the GitHub Actions workflow
(`.github/workflows/publish.yml`) which renders the site with Quarto and
deploys it to GitHub Pages.

> **One-time setup:** In your repository settings → Pages, set the source to
> **"GitHub Actions"** (not "Deploy from a branch").