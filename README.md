# REDLINE — the tennis gear guide

Static, dependency-free site (HTML/CSS/JS). No build step.

## Structure
```
index.html                     Homepage (rackets, compare, tools, rankings, players, blog teaser)
styles.css                     Shared design system (red/black/white)
blog/index.html                Blog listing
blog/*.html                    Blog posts (drafts — see "TO VERIFY" notes)
sitemap.xml, robots.txt        SEO
```

## Deploy (pick one — all free)

### Cloudflare Pages (recommended)
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Pages → Connect to Git → pick the repo.
3. Framework preset: **None**. Build command: *(blank)*. Output dir: `/`.
4. Deploy → you get a `*.pages.dev` URL. Add your custom domain under Pages → Custom domains.

### Netlify (fastest)
1. Go to app.netlify.com → drag this folder onto the page. Done.
2. Or: `npx netlify-cli deploy --prod --dir .` (after `netlify login`).

### After deploy
- Buy a domain (~€10/yr) and point it at the host. **Do this before applying to affiliate programs** — they reject `*.pages.dev`/`*.netlify.app`.
- Replace `REPLACE-WITH-YOUR-DOMAIN` in `robots.txt` and `sitemap.xml`.
- Submit the domain + sitemap to Google Search Console.

## Turning on affiliate income
1. Sign up: **Awin** (~€5 refundable deposit; likely hosts Tennis-Point + Decathlon) and **Amazon.de Associates** (~3% sports, easy approval).
2. Inside Awin, apply to Tennis-Point + Decathlon by name; confirm live rate/cookie there.
3. Paste your tracking params into `AFF_TAG` (top of the <script> in index.html) — every Buy button uses `buyLink()` and picks them up automatically.
4. Keep the affiliate disclosure bar (already on every page).
5. Germany: register a Gewerbe, keep "Werbung" labelling, add cookie consent IF you embed a tracking script, and check VAT reverse-charge with a Steuerberater.

## Blog drafts
The 3 posts are honest drafts. Search each for the dashed **"TO VERIFY"** boxes and fill in confirmed facts (champions, dates, the specific racket's name/specs) before publishing.
