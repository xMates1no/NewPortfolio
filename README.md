# Mates1no — Portfolio

A single-page portfolio site for Blockbench/3D modeling work for Minecraft servers.
Plain HTML, CSS and JavaScript — no build step, no framework, no dependencies.

## Structure

```
.
├── index.html      # all page content and structure
├── css/style.css   # design tokens, layout, hover/animation styles
├── js/script.js    # nav scroll state, FAQ accordion, contact form, background animation
├── robots.txt
└── sitemap.xml
```

## Running locally

Just open `index.html` in a browser, or serve it so relative asset paths behave
exactly like they will in production:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Things to fill in before you publish

- **Work section**: only one real project (Rajče.pro) is in there. The dashed
  "+" card is a placeholder — replace it with your next real project instead
  of leaving it up.
- **Social links**: GitHub/LinkedIn/X/Dribbble in the footer all point at the
  bare domains — swap in your actual profile URLs.
- **Contact form**: currently opens the visitor's email client addressed to
  `xmates1no@gmail.com` (via a `mailto:` link built in `js/script.js`) — no
  backend required, but it does depend on the visitor having a mail client
  configured. If you'd rather messages land silently with no popup, wire the
  form up to a service like [Formspree](https://formspree.io) or
  [EmailJS](https://www.emailjs.com/) instead — there's a comment above the
  `<form>` in `index.html` showing where that swap goes.
- **Favicon / OG image**: the favicon is an inline SVG star (no extra file to
  host). Consider adding a real Open Graph preview image and pointing
  `og:image` / `twitter:image` at it once you have one.

## Deploying

This is static output, so it works as-is with GitHub Pages, Netlify, Vercel,
Cloudflare Pages, or any static host — just point them at the repo root.

## Getting this into git

```bash
git init
git add .
git commit -m "Initial commit: portfolio site"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```
