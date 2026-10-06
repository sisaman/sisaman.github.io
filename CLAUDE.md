# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Sina Sajadmanesh's personal academic website, served by GitHub Pages at the domain in `CNAME`. It is a customized fork of the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template (itself derived from Minimal Mistakes). `README.md` is the upstream template's README, not project-specific documentation.

## Running locally

```bash
bundle install
bundle exec jekyll serve -l -H localhost   # http://localhost:4000, live reload
# or
docker compose up                          # same, in a container (uses _config_docker.yml overlay)
```

There are no tests or linters. GitHub Pages builds the site on push to `master` (there are no workflows in `.github/workflows`). `_site/`, `.sass-cache/`, and `Gemfile.lock` are gitignored build artifacts.

`npm run build:js` regenerates `assets/js/main.min.js` from the JS sources; this is only needed when editing `assets/js/`.

## Content model

Almost all edits are content edits to Markdown files with YAML front matter. Each collection is rendered by a listing page in `_pages/` through the shared `_includes/archive-single.html`, which decides what to show based on front-matter fields — check that include before adding a new field.

- **`_posts/`** — short news items shown on `/updates/`. Filename `YYYY-MM-DD-Slug.md` sets the date. Front matter is just `type: update` and a `title` that contains inline Markdown (links, bold); there is no body. The `type: update` branch in `archive-single.html` renders the title as the whole entry.
- **`_publications/`** — one file per paper, listed on `/publications/` grouped by year and sorted by the `date` field (not filename). Fields used: `collection: publications`, `title`, `authors` (Markdown string), `venue`, `date`, `paperurl` (title link), and optional link buttons `pdf`, `code`, `slides`, `video`, `media` (map of label → URL). Unused fields are commonly left commented out.
- **`_talks/`** — `layout: talk`, with `venue`, `date`, `location`, `slides`, `video`.
- **`_teaching/`** — uses `semester` and `venue`.
- `slides:` values (in publications and talks) are bare filenames resolved against `files/slides/` (naming convention `YY.MM.DD-Venue.pdf`).

Other key places:
- `_pages/about.md` is the homepage (`permalink: /`).
- `_data/navigation.yml` controls the header menu order.
- `_config.yml` holds site-wide settings, the author sidebar profile (`author:` block), and collection defaults. Jekyll does not hot-reload `_config.yml`; restart the server after changing it.

## CV PDF

`sina-sajadmanesh-cv.pdf` at the repo root (linked from `_pages/resume.md` and `about.md`) is pushed automatically from the separate `sisaman/cv` repository, producing the frequent "Update CV PDF from sisaman/cv@<sha>" commits. Don't edit it here; changes belong in that repo.
