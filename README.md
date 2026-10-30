# depeiyu.com

Personal site. Plain HTML and CSS, no build step.

## Edit

- `index.html`: content. Placeholders are in `[square brackets]`; search for `[` to find them.
- `style.css`: look.
- Add `resume.pdf` to this folder to make the Résumé link work.

Preview locally:

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy

Hosted on Cloudflare Pages, connected to this repo. Every push to `main`
publishes to depeiyu.com within about a minute; pushes to other branches get
a preview URL.

Cloudflare Pages settings: framework preset **None**, build command **empty**,
build output directory **`/`**.
