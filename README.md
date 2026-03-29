# Zixia Jia Personal Website

This repository contains a deployable personal academic website for **Zixia Jia**, built with **Jekyll + al-folio**.

## Included Content

- About page for Zixia Jia
- Publication list in [`_bibliography/papers.bib`](./_bibliography/papers.bib)
- News timeline in [`_news/`](./_news)
- GitHub Actions workflow for automatic deployment

Latest publication/news entries were refreshed using publicly indexed recent records (aligned with Google Scholar-visible updates) as of **March 29, 2026**.

## Local Preview

### Option 1: Ruby

```bash
bundle install
bundle exec jekyll serve
```

Then open: `http://127.0.0.1:4000`

### Option 2: Docker

```bash
docker-compose up
```

## Public Deployment (GitHub Pages)

1. Create or use repository: `JZXXX/JZXXX.github.io`.
2. Push this project to branch `main` (or `master`).
3. Ensure GitHub Actions is enabled for the repository.
4. The workflow file `.github/workflows/deploy.yml` will:
   - build the site,
   - publish `_site` to `gh-pages` branch.
5. In repository settings, enable GitHub Pages for branch `gh-pages` (root).
6. Visit: `https://JZXXX.github.io`.

## How To Update Papers and News

- Add/modify papers in `_bibliography/papers.bib`
- Add a new markdown file in `_news/` with front matter:

```yaml
---
layout: post
date: 2026-03-29 10:00:00+0800
inline: true
related_posts: false
---
```

## Important Config

Edit `_config.yml` if needed:

- `url`
- `github_username`
- `email`
- `scholar_userid` (optional)
- `dblp_url`
