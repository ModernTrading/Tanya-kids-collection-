# Tanya Kids Collection

A multilingual (English, Hindi, Gujarati, Tamil, Telugu, Kannada) storefront
landing page for **Tanya Kids Collection** — ethnic wear for boys, girls, and
parents — with WhatsApp-based ordering.

## Project structure

```
.
├── index.html          # Page markup
├── style.css           # All styles (extracted from the original inline <style>)
├── script.js           # All behavior/interactivity (language switch, category
│                        #   tabs, stories, image lightbox, WhatsApp links)
├── assets/
│   └── images/         # All product/story photos (extracted from base64)
└── README.md
```

## Running locally

No build step is required — it's a static site.

```bash
# from the project folder
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` directly in a browser (some browsers restrict
`file://` fetches, so a local server is the safer option).

## Deploying to Vercel

1. Push this folder to a GitHub repository.
2. In Vercel, click **New Project** → import the repository.
3. Framework preset: **Other** (static site) — no build command, no output
   directory override needed. Vercel will serve `index.html` as-is.
4. Deploy.

## Notes

- WhatsApp ordering number is `916281998364`, used directly in every
  `wa.me/...` link in `index.html` (the floating WhatsApp button and each
  product's "Order Now" button, each with a pre-filled message). If the
  number ever changes, it needs to be updated in each of these links.
- Language strings live in the `translations` object near the bottom of
  `script.js`.
