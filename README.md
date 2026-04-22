# streamy.rocks landing (static rebuild)

Static HTML/CSS rebuild of the public `streamy.rocks` marketing copy, structured for production hosting on Vercel.

## Design notes

- Uses **sRGB hex** and **rgba integer alpha** only (no `color-mix()`, no Display-P3-only colors).
- `color-scheme: dark` is set for predictable browser chrome behavior.

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
