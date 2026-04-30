# streamy.rocks landing (static rebuild)

Static HTML/CSS rebuild of the public `streamy.rocks` marketing copy, structured for production hosting on Vercel.

## Design notes

- Uses **sRGB hex** and **rgba integer alpha** only (no `color-mix()`, no Display-P3-only colors).
- `color-scheme: dark` is set for predictable browser chrome behavior.

## Social / OG image

- `assets/images/og-social.jpg` is a self-hosted social preview image for Open Graph and Twitter cards.
- Meta tags use `/assets/images/og-social.jpg`. For some crawlers you may want absolute URLs (e.g. `https://streamy.rocks/assets/images/og-social.jpg`) after the production domain is fixed.

## Vercel

- `vercel.json` only sets long-cache headers for `/assets/*`. Static files (`index.html`, `styles.css`, images) are served as files — **no** catch-all rewrite to `index.html` (that would break CSS and images).

## Local preview

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy (Vercel)

From this directory:

```bash
vercel
vercel --prod
```

Attach custom domain `streamy.rocks` in the Vercel project settings after DNS is pointed at Vercel.
