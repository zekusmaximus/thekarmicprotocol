# thekarmicprotocol.com

Static site for *The Karmic Protocol* by Jeffrey A. Zyjeski. Plain HTML and CSS, no build step, no JavaScript, no third-party requests.

## Files

- `index.html`: the page
- `404.html`: served by Vercel for unknown paths
- `styles.css`: all styling
- `fonts/`: Literata (SIL Open Font License, see `fonts/OFL.txt`), self-hosted
- `images/`: cover at 460, 700, and 925 px wide, JPEG and WebP
- `og.jpg`: 1200×630 link-preview image
- `vercel.json`: clean URLs, redirects for the old `/experience` and `/agent` pages, font caching

## Preview locally

```bash
python -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly from disk won't load the fonts or images, because the site uses root-relative paths.

## Deploy

On Vercel, import this repository as a new project with framework preset "Other". It needs no build command and no output directory. Then move `thekarmicprotocol.com` and `karmicprotocol.com` from the old project to this one under Settings → Domains, and set `karmicprotocol.com` to redirect to `thekarmicprotocol.com`.
