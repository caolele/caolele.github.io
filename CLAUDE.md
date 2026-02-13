# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal academic website built with Jekyll using the [al-folio](https://github.com/alshedivat/al-folio) theme. The site is hosted on GitHub Pages at https://caolele.github.io.

## Common Commands

### Local Development with Docker (Recommended)
```bash
docker compose pull
docker compose up
```
Site available at http://localhost:8080

### Local Development without Docker
```bash
bundle install
pip install jupyter
bundle exec jekyll serve
```
Site available at http://localhost:4000

### Build for Production
```bash
bundle exec jekyll build
```
Output goes to `_site/` directory.

### Code Formatting
```bash
npx prettier --check .
npx prettier --write .
```

## Architecture

### Key Configuration
- `_config.yml` - Main site configuration (URL, metadata, Jekyll Scholar settings, plugin configuration)
- Changes to `_config.yml` require restart of Jekyll server

### Content Directories
- `_pages/` - Static pages (about, cv, publications, etc.)
- `_news/` - News announcements displayed on homepage
- `_projects/` - Project pages displayed in grid layout
- `_posts/` - Blog posts (format: `YYYY-MM-DD-title.md`)
- `_bibliography/papers.bib` - Publications in BibTeX format (auto-generates publications page)

### Data Files
- `_data/cv.yml` - CV content (fallback if `assets/json/resume.json` not present)
- `_data/repositories.yml` - GitHub repos to display
- `_data/coauthors.yml` - Co-author links for publications
- `assets/json/resume.json` - CV in JSON Resume format (primary)

### Styling
- `_sass/_themes.scss` - Theme colors (`--global-theme-color`)
- `_sass/_variables.scss` - Stock color options
- `_sass/_base.scss` - Fonts and spacing

### Publications System (Jekyll Scholar)
Publications are managed via `_bibliography/papers.bib`. Supported BibTeX fields for buttons:
- `pdf`, `code`, `slides`, `poster`, `video`, `website`, `blog`
- `arxiv` (auto-links), `doi`, `abstract`, `bibtex_show`

Author highlighting configured in `_config.yml` under `scholar:` (currently set to Einstein as example).

## Deployment

Site auto-deploys to GitHub Pages when pushing to `main` branch. The `gh-pages` branch is auto-generated - never edit it directly.
