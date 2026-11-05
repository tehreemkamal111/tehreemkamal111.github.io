# Tehreem Kamal's portfolio

Academic and software development portfolio, built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme. The site is configured for **https://tehreemkamal111.github.io/** with an empty `baseurl`.

## Content

- `_pages/about.md`: introduction, research interests, and tools.
- `_pages/research.md`: MRI segmentation and industrial computer vision research.
- `_pages/experience.md`: employment history and education.
- `_pages/cv.md`: CV download, skills, certifications, and academic activities.
- `_projects/`: MRI segmentation, bottle inspection, and frontend development contributions.
- `_data/socials.yml`: email, GitHub, LinkedIn, and CV links.
- `files/CV.pdf`: downloadable CV.

All biographical content comes from the supplied CV. No publications are listed. The homepage uses the supplied portrait at `assets/img/profile.jpg`, displayed as a circular head-and-shoulders crop using CSS. The original photograph is preserved unchanged. To replace it, update `profile.image` and `profile.image_alt` in `_pages/about.md`; adjust the crop in `.profile-photo-frame` in `assets/css/main.scss`.

## Local development

Install Ruby 3.3 or later, Bundler 4.0.6, and Node.js 20 or later. From the repository directory:

```sh
bundle install
npm ci
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

Open `http://localhost:4000/`. Stop the server with Ctrl+C.

For a production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
```

The generated site is written to `_site/`, which is ignored by Git. The theme is installed through the version-pinned `al_folio_core` gem; local includes, layouts, and styles override it.

## GitHub Pages

Create a public repository named `tehreemkamal111.github.io` under `tehreemkamal111` and use `master` as its default branch. Push this source to that branch. In **Settings → Pages → Build and deployment**, select **GitHub Actions**.

The included `.github/workflows/deploy.yml` builds pull requests targeting `master` and deploys pushes to `master`. It can also be started manually from the Actions tab. A successful deployment serves the portfolio at **https://tehreemkamal111.github.io/**.

## Credits

Adapted from an al-folio portfolio template. The theme's MIT license is retained in `LICENSE`.
