# niranjanrajesh02.github.io

Personal academic website of Niranjan Rajesh, built with [Jekyll](https://jekyllrb.com/) on the [al-folio](https://github.com/alshedivat/al-folio) theme. Pushing to `master` builds and deploys the site via `.github/workflows/deploy.yml`.

## Where things live

| What | File |
| --- | --- |
| Bio / homepage | `_pages/about.md` |
| Research interests | `_pages/research.md` |
| Publication list | `_data/publications.yml` |
| CV & résumé PDFs | `assets/pdf/` (file names set in `_pages/cv.md`) |
| Teaching / talks | `_pages/misc.md` |
| Colors | `_sass/_variables.scss`, `_sass/_themes.scss` |
| Site-wide settings, SEO | `_config.yml` |

## Run locally

Requires Ruby 3.x with DevKit.

```bash
bundle install
bundle exec jekyll serve --livereload --config _config.yml,_config_dev.yml
```

Then open http://localhost:4000. `_config_dev.yml` turns off steps that need extra tools (ImageMagick).
