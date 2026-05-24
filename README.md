# Reyhan Issatyadi Darmawan — Personal Portfolio

Personal landing page built with [Astro](https://astro.build).

**Live:** https://reyhan-darmawan15.github.io

---

## Stack

- **Framework:** Astro 4 (static output, zero JS by default)
- **Styling:** Vanilla CSS with custom properties (no framework)
- **Fonts:** Share Tech Mono + DM Sans (Google Fonts)
- **Theme:** Oscilloscope / hardware signal aesthetic

---

## Local Development

```bash
npm install
npm run dev       # http://localhost:4321
npm run build     # outputs to ./dist
npm run preview   # preview production build
```

---

## Deployment

### GitHub Pages (recommended)

1. Push this repo to GitHub as `reyhan-darmawan15.github.io` (for root domain) or any repo name.
2. Go to **Settings → Pages → Source** → select **GitHub Actions**.
3. Push to `main` — the workflow in `.github/workflows/deploy.yml` handles the rest.

> If deploying to a subdirectory (e.g. `github.com/user/portfolio`), uncomment `base: '/portfolio'` in `astro.config.mjs`.

### Cloudflare Pages

1. Connect your GitHub repo in the Cloudflare Pages dashboard.
2. Set **Build command:** `npm run build`
3. Set **Build output directory:** `dist`
4. Deploy. Cloudflare auto-deploys on every push to `main`.

### Netlify

1. Connect repo, set build command `npm run build`, publish directory `dist`.
2. Done — Netlify handles everything automatically.

---

## Project Structure

```
reyhan-portfolio/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Nav.astro
│   │   ├── Hero.astro        ← animated ECG canvas
│   │   ├── About.astro
│   │   ├── Skills.astro
│   │   ├── Experience.astro
│   │   ├── Projects.astro
│   │   └── Contact.astro
│   ├── layouts/
│   │   └── Base.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
├── .github/workflows/
│   └── deploy.yml
├── astro.config.mjs
└── package.json
```

---

## Customization

- **Colors & theme:** Edit CSS variables at the top of `src/styles/global.css`
- **Content:** Each section is a separate component under `src/components/`
- **Site URL:** Update `site` in `astro.config.mjs` to match your domain
- **Photo:** Add `public/photo.jpg` and reference it in `About.astro`
