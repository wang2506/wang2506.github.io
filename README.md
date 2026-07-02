# Personal Academic Website

A clean, warm personal site built with plain HTML + CSS. No build tools, no frameworks — just edit and push.

## File structure

```
.
├── index.html          ← all your content lives here
├── assets/
│   ├── style.css       ← all styles
│   ├── main.js         ← scroll-spy nav
│   ├── photo.jpg       ← your headshot (add this yourself)
│   └── cv.pdf          ← your CV (add this yourself)
├── CNAME               ← custom domain config (see below)
└── README.md
```

## Deploying to GitHub Pages

1. Push this folder to a GitHub repo named `yourusername.github.io`
2. Go to the repo → **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch** → `main` → `/ (root)`
4. Your site will be live at `https://yourusername.github.io` within a minute or two

> If you're replacing an existing Academic Pages site, just delete everything in the repo and push these files instead.

## Editing your content

All the content you need to update is in `index.html`. Search for `✏️` to find every placeholder:

| What | Where in index.html |
|---|---|
| Your name | `<title>` tag + `.name-block` in sidebar + `<h1>` in hero |
| Role / affiliation | `.role` in sidebar + `.subtitle` in hero |
| About blurb | First two `<p>` tags inside `.hero-text` |
| Photo | Uncomment `<img>` in `.photo-wrap`, add `assets/photo.jpg` |
| CV link | `<a href="assets/cv.pdf">` in sidebar |
| Google Scholar / GitHub / Twitter | Links in `.sidebar-links` |
| Papers | Duplicate the `<article class="paper">` block |
| Courses | Duplicate the `<div class="course">` block |
| Contact details | `.contact-grid` section |

## Adding your photo

1. Export a square or portrait crop (at least 400px wide) as `photo.jpg`
2. Put it in the `assets/` folder
3. In `index.html`, find the `.photo-wrap` div and:
   - Uncomment the `<img>` line
   - Delete the `<svg>` placeholder and the `<span>` below it

## Setting up a custom domain

1. Buy a domain (e.g. `yourname.com`) from Namecheap, Cloudflare, Google Domains, etc.
2. Open `CNAME` in this repo and replace the comments with just your domain:
   ```
   yourname.com
   ```
3. At your registrar's DNS settings, add a CNAME record:
   - **Name/Host**: `@` (or `www`)
   - **Value/Target**: `yourusername.github.io`
4. In GitHub repo Settings → Pages, enter your custom domain
5. Check "Enforce HTTPS" once it's verified (takes up to 24h for DNS to propagate)

## Customising the look

All visual tokens are CSS variables at the top of `assets/style.css`:

```css
:root {
  --sand: #F5F1EA;       /* page background */
  --terra: #B86B3E;      /* accent color — links, badges, dots */
  --charcoal: #2C2925;   /* primary text */
  ...
}
```

Change `--terra` to tweak the accent color across the whole site.
