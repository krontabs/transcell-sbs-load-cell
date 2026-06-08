# Transcell SBS Series — Product Landing Page

Single-page marketing/ecommerce site for the **Transcell SBS Series Single-Ended Shear Beam Load Cell**.

## Stack
- Static **HTML/CSS/JS** — a single `index.html`, no build step, no framework.
- `assets/` — product images, the exploded-view hero video, and the logo.
- `SBS-2 datasheet.pdf` — linked from the Downloads section.

## Local preview
Any static server works:

```bash
npx serve .
# or
python -m http.server 8000
```

Then open the printed URL.

## Deploy (Vercel)
No build is required. When importing into Vercel, set:
- **Framework Preset:** Other
- **Build Command:** (leave empty)
- **Output Directory:** (leave empty / root)

Vercel serves `index.html` and `assets/` directly.

## Configuration
The cart, quote, contact, and phone links live in the `CONFIG` object near the
bottom of `index.html`:

```js
const CONFIG = {
  cartBaseUrl: "/cart/",
  quoteUrl:    "/contact/",
  engineerTel: "+18474199180",
  email:       "sales@transcell.net"
};
```
