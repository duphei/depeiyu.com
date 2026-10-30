# depeiyu.com

Personal site. Plain HTML and CSS, no build step.

## Edit

- `public/index.html`: content.
- `public/style.css`: look.
- Anything else placed in `public/` is published as-is.

Preview locally:

```bash
python3 -m http.server 8000 -d public   # then open http://localhost:8000
```

## Deploy

Hosted on Cloudflare Workers as static assets (`wrangler.jsonc` points at
`public/`). The Worker is connected to this repo, so every push to `main`
publishes to depeiyu.com within a minute or two; other branches get a
preview version.

Cloudflare build settings: build command **empty**, deploy command
**`npx wrangler deploy`**, non-production branch deploy command
**`npx wrangler versions upload`**.
