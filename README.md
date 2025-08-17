# Signalworks — Static Site

A single-file static site for Signalworks (game studio). No build step. Ready for GitHub Pages.

## Features
- Clean dark UI, responsive cards
- External links hardened with `rel="noopener noreferrer"`
- Email obfuscation (JS hydrator builds `mailto:` at runtime)
- No trackers, no frameworks

## Quick Start
1. Upload this repo to GitHub.
2. Enable **GitHub Pages**: Settings → Pages → Deploy from branch → `main` → `/ (root)`.
3. Your site will be served at `https://<your-username>.github.io/<repo-name>/`.

### Local Preview
Just open `index.html` in a browser.

## Editing Emails
The HTML uses attributes instead of exposing a raw address:
```html
<a class="link"
   href="#"
   data-email-user="signalworksbusiness"
   data-email-domain="gmail.com"
   data-email-subject="Application">[email protected]</a>
```
The small script near the bottom assembles the clickable address at runtime.

## Notes
- Thumbnails are loaded from Imgur; consider hosting on your own domain/CDN if desired.
- Update the JSON-LD `sameAs` links and `<title>`/`description` for production.
