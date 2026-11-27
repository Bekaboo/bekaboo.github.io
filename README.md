# bekaboo.github.io

Source for https://bekaboo.github.io -- a single static page, no build step, no dependencies.

## Files

- `index.html` -- the page. Edit text here.
- `style.css` -- typography, spacing, and light/dark colors.
- `.nojekyll` -- tells GitHub Pages to serve files as-is instead of running Jekyll.

## Local preview

Open `index.html` in a browser, or serve it over HTTP:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Publishing

```
git add -A
git commit -m "Update site"
git push
```

GitHub Pages rebuilds on push to `main`; the live site updates within a minute.

## First-time setup (only if the repo is not yet on GitHub)

```
gh repo create bekaboo.github.io --public --source . --push
```

Then Settings -> Pages -> Source: `Deploy from a branch`, branch `main`, folder `/ (root)`.

## Custom domain

Add a `CNAME` file at the repo root containing the bare domain, point DNS at GitHub Pages, then enable the domain under Settings -> Pages.