# my-portfolio

Personal portfolio site, served by GitHub Pages at
https://swezinlinn.github.io/my-portfolio/

Plain HTML, no build step, no dependencies.

## Files

- `index.html` — the whole site (styles inlined, fonts from Google Fonts)
- `Swe-Zin-Linn-CV.pdf` — linked from the "Get in touch" section
- `robots.txt`, `sitemap.xml` — so search engines index the page

## Turning Pages on (once)

Settings → Pages → Source: **Deploy from a branch** → Branch: `main`, folder
`/ (root)` → Save. The site appears about a minute later.

## Making a change

Edit `index.html`, then:

```bash
cd ~/swezinlinn-portfolio
git add . && git commit -m "Update" && git push
```

Pages redeploys on every push to `main`.

## Updating the CV

The PDF is generated from `~/swezinlinn-cv`. After rebuilding it there:

```bash
cp ~/swezinlinn-cv/out.pdf ~/swezinlinn-portfolio/Swe-Zin-Linn-CV.pdf
cd ~/swezinlinn-portfolio && git add . && git commit -m "Update CV" && git push
```

## If the site ever moves

The URL appears in four places: `<link rel="canonical">` and `og:url` in
`index.html`, the `"url"` field in its JSON-LD block, plus `sitemap.xml` and
`robots.txt`. It is also printed in the CV header, which comes from
`~/swezinlinn-cv/content.py`.
