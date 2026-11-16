# Zihan Wang — personal website

Source for https://yichuishan.github.io, built with Jekyll and Academic Pages.
All content and the downloadable CV are committed here; no cloud workspace or chat is needed to maintain the website.

## Update content

- `_config.yml`: identity, email, affiliation, site settings.
- `_pages/about.md`: homepage and education.
- `_pages/publications.md`: research (including thesis and patent experience).
- `_pages/portfolio.md`: selected projects.
- `_pages/experience.md`: internships.
- `_pages/cv.md`: web CV.
- `files/Zihan_Wang_CV_2026.pdf`: downloadable original CV (includes the contact details in the supplied document).
- `_data/navigation.yml`: navigation links.
- `assets/css/profile.css`: personal styling.

Dates and achievements reflect the supplied 2026 CV. SAMNet is thesis research, not listed as an accepted publication. Chinese patent number ZL 2024 1 0530741.4 was supplied by the author. No verified paper URL has been supplied. The avatar uses initials until a portrait is added. Template example collections and pages are excluded from the published site in `_config.yml`.

## Develop locally

Install Ruby 3.2, Bundler, Node.js, and the compiler/development libraries required by native gems (OpenSSL, YAML, zlib).

```sh
bundle config set --local path vendor/bundle
bundle install
npm install
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Open the local server in your browser. Test `/`, `/research/`, `/projects/`, `/experience/`, `/cv/`, and the PDF download. Restart Jekyll after editing `_config.yml`.

`npm run build:js` rebuilds the tracked JavaScript bundle when JavaScript source changes. Ruby gems and npm packages are needed only for development/builds; visitors receive static files.

## GitHub publishing

Commit and push changes to `master`. GitHub Actions runs the strict Jekyll build on pushes and pull requests. For the public site, GitHub Pages should be enabled for `master` and `/ (root)` in repository Settings → Pages; the build check itself does not change that setting or deploy the site. GitHub Pages hosting continues independently of the development environment.

## Credits

Based on [Academic Pages](https://github.com/academicpages/academicpages.github.io) and Minimal Mistakes. See LICENSE.
