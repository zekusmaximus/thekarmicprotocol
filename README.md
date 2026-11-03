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

Hosted on Vercel (framework preset "Other", no build step). Every push to `main` deploys to production; other branches get preview URLs.

The primary address is `https://www.thekarmicprotocol.com`. Vercel redirects the bare `thekarmicprotocol.com` to it, and `vercel.json` sends `karmicprotocol.com` and `www.karmicprotocol.com` there too. Canonical tags, Open Graph tags, structured data, `sitemap.xml` and `robots.txt` all use the `www` address, so keep them in step if the primary domain ever changes.
