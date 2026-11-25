# streamy.rocks

Self-hosted static build of the **Streamy.Rocks** landing page, deployed directly on **GitHub Pages** with zero third-party site builder dependencies.

## Hosting & Custom Domain (GitHub Pages)

- **Branch / Folder:** `master` / `/` (root)
- **Custom Domain (`CNAME`):** `streamy.rocks`
- **Jekyll:** Disabled via `.nojekyll`

### Required DNS Records (GoDaddy / DNS Provider)

Point the apex domain `streamy.rocks` to GitHub Pages IPv4 addresses and `www` to `commentzrus.github.io`:

| Type  | Name | Value |
| ----- | ---- | ----- |
| A     | `@`  | `185.199.108.153` |
| A     | `@`  | `185.199.109.153` |
| A     | `@`  | `185.199.110.153` |
| A     | `@`  | `185.199.111.153` |
| CNAME | `www` | `commentzrus.github.io` |

Remove any old Gamma A records (`3.136.232.26`, `3.137.108.170`) and the old `sites.gamma.app` CNAME. Once DNS propagates, GitHub Pages automatically issues an HTTPS certificate for `streamy.rocks`.

## Local Preview

Open `index.html` in a browser, or run any static file server from this directory:

```bash
npx serve .
```
