# Jinwei Lu — Academic Website

This repository contains the Jekyll site for Jinwei Lu (Shenzhen University). It uses the Minimal Mistakes theme via the Academic Pages structure.

## What’s included
- Splash-style homepage at `/index.md` with hero image, quick links (Publications / Teaching / Talks), and an automatic “Recent publications” list.
- About page at `/about/` (moved from the template front page).
- Pre-wired sections for:
  - `Publications` (`_publications/` collection)
  - `Talks` (`_talks/` collection)
  - `Teaching` (`_teaching/` collection)
  - `Portfolio` (`_portfolio/` collection)
  - `Blog posts` (`_posts/`)
- Top navigation in `_data/navigation.yml` with Home, About, CV, etc.

## Edit site identity
Update these fields in `_config.yml`:
- `title`, `name`, `description`
- `author` → `name`, `bio`, `location`, `employer`, `email`
- `url` (set to final domain, keep `baseurl: ""` if served from apex)

## Homepage content
- `index.md` controls hero, feature cards, and the highlights section.
- “Recent publications” is generated from the `_publications` collection (latest 5).
- Replace the example items under `highlights:` in `index.md` with real papers once added.

## Publications
Add one markdown file per paper under `_publications/` using this front matter:

```yaml
---
title: "Paper title"
collection: publications
permalink: /publication/2024-paper-title
date: 2024-06-01
venue: "Journal / Conference"
paperurl: "https://..."
citation: "Author, A., Lu, J., ... (2024). Title. Venue."
---

Abstract or extra details shown on the single page.
```

Tips:
- Filename prefix `YYYY-MM-DD-` is used for sorting in lists.
- Use `venue` (journal/conference) and `paperurl` (PDF or DOI) for better listing.

## Talks / Teaching / Portfolio
Use the provided collections (`_talks`, `_teaching`, `_portfolio`) in the same way as publications. Each item is one markdown file with YAML front matter.

## Navigation
Top menu is in `_data/navigation.yml`. Add, remove, or reorder items there. The site header automatically renders these links.

## Assets
Place images in `images/` and general files (PDF, ZIP) in `files/`.

## Local development
Prereqs (Ubuntu/Debian example):
```
sudo apt update && sudo apt install -y ruby-full build-essential nodejs
```
Install gems and serve:
```
bundle install
bundle exec jekyll serve -l -H localhost
```
Browse at `http://localhost:4000`. The server live-reloads on edits.

If you hit gem issues, delete `Gemfile.lock` and retry `bundle install`.

## Deploy
- GitHub Pages: push to the repository configured for Pages; it will build automatically.
- Custom domain: set `CNAME` in repo settings and update `url` in `_config.yml`.

## Structure overview
```
_config.yml                # Site-wide config and metadata
_data/navigation.yml       # Top navigation
index.md                   # Homepage (splash)
_pages/                    # Standalone pages (About, etc.)
_publications/             # One file per publication
_talks/                    # One file per talk
_teaching/                 # Teaching entries
_posts/                    # Blog posts (optional)
images/, files/            # Assets (images, PDFs)
_includes/, _layouts/      # Theme templates
```

## Next steps
- Replace placeholder “Selected Papers” list in `index.md` with actual highlights.
- Add real publication entries under `_publications/`.
- Set `url` and enable analytics if desired in `_config.yml`.

Questions or improvements welcome.
