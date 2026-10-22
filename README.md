# Jihwan Oh — academic homepage

Academic homepage built with [al-folio v0.14.7](https://github.com/alshedivat/al-folio/tree/v0.14.7), with three navigation items: **about**, **publication**, and **cv**.

## Edit content

- `_pages/about.md`: biography and research interests.
- `_data/venues.yml`: green conference badges with abbreviated venue names and years.
- `_bibliography/papers.bib`: all six publications, in CV order within each year. Set `selected = {true}` to show a paper on the homepage. Author suffixes `*` and `†` preserve equal contribution and corresponding author markers.
- `_pages/cv.md`: displays the CV PDF inside the page, with the site navigation retained and a link to open or download the PDF.
- `_data/cv.yml`: retained structured CV information for future use.
- `_data/socials.yml`: contact and social links.
- `assets/img/profile-20261023.jpg`: profile photo supplied by the owner.
- `assets/pdf/Jihwan_Oh_CV.pdf`: downloadable CV.
- `assets/tex/Jihwan_Oh_CV.tex`: CV source, with template comments removed and the first duplicate Education heading corrected to Research Interests.
- `_config.yml`: site name, URL, theme options, and bibliography settings.

Content follows the CV supplied on October 22, 2026. Commented template examples and unrelated people in the original LaTeX were omitted. The two EMNLP 2026 papers keep the lab publication links supplied in the CV.

## Build locally

Use Ruby 3.0 or later with development headers and a C/C++ compiler:

```sh
gem install bundler -v 2.4.22
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000`. Production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build
```

The published GitHub Pages branch contains the generated static files and `.nojekyll`. Edit and commit the source on `master`; then run `./bin/publish` to build and update `gh-pages`. The Pages setting should use the root of `gh-pages`. Core CSS, JavaScript, and fonts are stored locally so the three pages do not depend on a CDN.

## CV PDF

```sh
pdflatex -interaction=nonstopmode -halt-on-error -output-directory /tmp assets/tex/Jihwan_Oh_CV.tex
```

The theme retains its original MIT license in `LICENSE`.
