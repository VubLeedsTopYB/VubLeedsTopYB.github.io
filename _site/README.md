# topYB IJRG website

This repository is a **GitHub Pages / Jekyll** site.

- Page content is written in **Markdown** (`.md`).
- Shared header/footer are **Jekyll includes** in `_includes/`.
- The HTML wrapper is a **Jekyll layout** in `_layouts/`.

> Opening `.md` files directly in a browser (or serving the folder with `python -m http.server`) will **not** render the site. You need to run Jekyll so it can convert Markdown into HTML.

## Local preview

### Option 1: Ruby + Bundler (recommended, matches GitHub Pages)

1. Install Ruby (3.x is fine) and Bundler.
2. In this repo folder:

   ```bash
   bundle install
   bundle exec jekyll serve
   ```

3. Open: http://localhost:4000

### Option 2: Docker (no Ruby install)

From the repo folder:

```bash
docker run --rm -p 4000:4000 -v "$PWD":/srv/jekyll jekyll/jekyll:4 jekyll serve --watch --force_polling --host 0.0.0.0
```

Open: http://localhost:4000
