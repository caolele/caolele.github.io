# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal academic website built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme. It generates a static site for showcasing publications, projects, news, and CV information.

## Development Commands

### Local Development with Docker (Recommended)
```bash
docker compose pull
docker compose up
```
Site runs at `http://localhost:8080`. Changes auto-reload.

### Local Development without Docker
```bash
bundle install
pip install jupyter
bundle exec jekyll serve
```
Site runs at `http://localhost:4000`.

### Build for Production
```bash
bundle exec jekyll build
```
Output goes to `_site/`.

### Code Formatting
```bash
npx prettier --check .
npx prettier --write .
```

## Architecture

### Key Configuration
- `_config.yml`: Main site configuration (URL, theme settings, plugins, Jekyll Scholar settings)
- `_data/socials.yml`: Social media links
- `_data/repositories.yml`: GitHub repos to display
- `_data/coauthors.yml`: Co-author links for publications

### Content Directories
- `_bibliography/papers.bib`: Publications in BibTeX format (auto-generates publications page via Jekyll Scholar)
- `_news/`: News items displayed on homepage (markdown files)
- `_pages/`: Site pages (about, cv, publications, etc.)
- `_projects/`: Project pages displayed on projects grid
- `_posts/`: Blog posts (format: `YYYY-MM-DD-title.md`)

### CV Data Sources
Two options (in priority order):
1. `assets/json/resume.json` - JSON Resume format
2. `_data/cv.yml` - YAML format (fallback if JSON not found)

### Styling
- `_sass/_themes.scss`: Theme colors (`--global-theme-color`)
- `_sass/_variables.scss`: Available color options
- `_sass/_base.scss`: Fonts and spacing

### Publications
BibTeX entries in `_bibliography/papers.bib` support special fields:
- `abbr`, `abstract`, `arxiv`, `code`, `pdf`, `poster`, `slides`, `video`, `website`
- Author matching configured via `scholar:last_name` and `scholar:first_name` in `_config.yml`

## Deployment

Site auto-deploys to GitHub Pages on push to `main` branch. The `gh-pages` branch is auto-generated - never edit it directly.
