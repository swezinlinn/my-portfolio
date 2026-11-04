# swezinlinn.github.io

Personal portfolio site. Plain HTML, no build step, no dependencies.

## Files

- `index.html` — the whole site (styles inlined, fonts from Google Fonts)
- `Swe-Zin-Linn-CV.pdf` — linked from the "Get in touch" section
- `robots.txt`, `sitemap.xml` — so search engines index the page

## Publish it on GitHub Pages

1. On github.com, create a **public** repository named exactly `swezinlinn.github.io`.
   Do not add a README, .gitignore or licence — keep it empty.
2. In this folder:

   ```bash
   git init -b main
   git add .
   git commit -m "Portfolio site"
   git remote add origin https://github.com/swezinlinn/swezinlinn.github.io.git
   git push -u origin main
   ```

3. Wait about a minute, then open https://swezinlinn.github.io

The site rebuilds on every push. To change text, edit `index.html`, then
`git add . && git commit -m "Update" && git push`.

## Updating the CV

Replace `Swe-Zin-Linn-CV.pdf` with a newer export, keeping the same filename,
then commit and push. The link on the page keeps working.
