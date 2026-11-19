# Hustlo website

Marketing site and early-access waitlist for [hustlo.in](https://hustlo.in).

Plain HTML and CSS: no build step, no dependencies.

## Files

| File | Purpose |
|---|---|
| `index.html` | Landing page and waitlist form |
| `privacy.html` | Privacy policy (served at `/privacy`) |
| `favicon.svg` | Browser tab icon |
| `vercel.json` | Clean URLs (`/privacy` instead of `/privacy.html`) |

## Waitlist form

The form posts JSON to the URL in `FORM_ENDPOINT`, near the bottom of `index.html`.
Create a free form at https://formspree.io, then paste its endpoint (for example `https://formspree.io/f/abcdwxyz`) into that constant.
If it's left empty, the form asks visitors to email hello@hustlo.in instead.

## Run locally

Open `index.html` in a browser, or run:

```bash
npx serve .
```

## Deploy

The site is deployed on Vercel from the `main` branch. Every push to `main` goes live automatically.
Pull requests and other branches get their own preview URL.

Domain DNS is managed in Hostinger. Only the website records (`A @`, `CNAME www`) point to Vercel.
Don't change the email records (MX, SPF, DKIM, DMARC).
