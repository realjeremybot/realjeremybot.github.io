# Zhuoyi (Jeremy) Peng — Academic Homepage

Personal academic website built on the
[academic-homepage](https://github.com/luost26/academic-homepage) Jekyll template.

## What to edit

| Content | File |
| --- | --- |
| Name, bio, positions, email, social links, education, experience, awards | `_data/profile.yml` |
| Publications (one file each) | `_publications/*.md` |
| News / updates on the homepage | `_news/*.md` |
| Bold-self + co-author links | `_data/authors.yml` |
| Navbar links | `_data/navigation.yml` |
| Portrait & institution logos | `assets/images/photos/`, `assets/images/badges/` |

## Deploy to GitHub Pages (branch-based)

This repo is set up to build with GitHub Pages' **default (branch-based) builder**.
The `jekyll-email-protect` plugin was removed for compatibility (that builder runs in
safe mode and disallows it).

1. Repo: **`realjeremybot.github.io`** (a *user site* served at
   `https://realjeremybot.github.io`).
2. Push this folder to the `main` branch.
3. In the repo: **Settings → Pages → Build and deployment → Source =
   "Deploy from a branch" → Branch: `main` / `/ (root)` → Save**.
4. Every push to `main` rebuilds automatically (first build takes ~1 min).

### Optional: re-enable email obfuscation via GitHub Actions
If you want the `jekyll-email-protect` plugin back (hides your email from scrapers),
switch to an Actions-based build: re-add the plugin to `_config.yml` + `Gemfile`,
restore the `encode_email` filter in `_includes/widgets/profile_card*.html`, add a
Jekyll Pages workflow under `.github/workflows/`, and set Pages Source = "GitHub
Actions". Pushing workflow files requires a token/login with the **`workflow`** scope.

## Run locally (optional)

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

Template © [luost26](https://github.com/luost26/academic-homepage) (MIT).
