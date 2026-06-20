# Ting-Ting Gao — academic website

A Jekyll site, pinned to the `github-pages` gem (Jekyll 3.9) so it builds the
same locally and on GitHub Pages, and runs on the system Ruby 2.6.

## Edit content (no code needed)

| What | Where |
|------|-------|
| Name, links, email, nav | `_config.yml` |
| Bio, news, homepage | `index.md` |
| Publications | `_data/publications.yml` |
| Talks & service | `_data/talks.yml` |
| CV page | `cv.md` |
| Colors / styling | `assets/css/style.css` (`--accent` is the redwood color) |
| Profile photo | `assets/img/profile.jpg` (replace this file) |
| CV PDF | `assets/cv/CV_Gao.pdf` (replace this file) |

Adding a publication = add a block to `_data/publications.yml`. Set
`selected: true` to feature it on the homepage.

## Preview locally

```bash
bundle install        # first time only
bundle exec jekyll serve
# open http://localhost:4000
```

## Publish on GitHub Pages

1. Create a repo named `<your-username>.github.io` on GitHub.
2. Push this folder to it:
   ```bash
   git init && git add -A && git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. In the repo: Settings → Pages → Source = `main` branch. Your site appears at
   `https://<your-username>.github.io` within a minute or two.

If you instead use a repo with a different name, set `baseurl: "/<repo-name>"`
in `_config.yml`.
