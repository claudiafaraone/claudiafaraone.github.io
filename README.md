# claudiafaraone.github.io

Personal website of Claudia Faraone, built with [Jekyll](https://jekyllrb.com) and the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, and published with GitHub Pages.

## Preview locally

```bash
cd ~/Documents/claudiafaraone.github.io
bundle install            # only the first time, or after changing the Gemfile
bundle exec jekyll serve
```

Then open http://localhost:4000. Pages reload when files are saved, except `_config.yml`: after editing it, stop the server (Ctrl+C) and start it again.

## Where things are

| What | File |
|---|---|
| Name, sidebar, email, profile links | `_config.yml` (section `author:`) |
| Profile photo | `images/profile.png` |
| Top menu | `_data/navigation.yml` |
| Home page / bio | `_pages/about.md` |
| Research | `_pages/research.md` |
| Publications | `_data/publications.yml` |
| Videos | `_data/videos.yml` |
| Teaching | `_pages/teaching.md` |
| ETICity Venezia | `_pages/eticity-venezia.md` (images in `images/eticity/`) |
| PDF files (CV, papers) | `files/` → published at `/files/name.pdf` |
| Extra styles | `assets/css/main.scss` (end of file) |

## Publish

Commit and push to `main`: the GitHub Actions workflow in `.github/workflows/jekyll.yml` builds the site and publishes it (repository Settings → Pages → Source: GitHub Actions).
