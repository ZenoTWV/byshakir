# By Shakir Website

Astro 5 + Tailwind marketing site for By Shakir Luxury Interiors, featuring project pages, gallery lightbox, and a video hero.

## Quickstart
```bash
npm install
npm run dev       # http://localhost:4321
npm run build     # outputs to dist/
npm run preview   # serve the production build
```

## Key Content
- Projects: `src/content/projects/*.md` (hero + gallery images)
- Pages: `src/pages/` (home, about, contact, legal)
- Components: `src/components/`
- Assets: `src/assets/` (processed) and `public/` (static). Hero video lives at `public/videos/hero-final.mp4`.

## Deployment Notes (Cloudflare Pages)
- Cloudflare Pages has a 25 MiB per-file limit. The hero video is compressed to ~19 MB (`public/videos/hero-final.mp4`); keep any replacements under 25 MB or host externally (e.g., R2/Stream) and point the `<video>` src to the external URL.
- Build command: `npm run build`
- Output directory: `dist`

## Forms & Analytics
- Contact form posts to Web3Forms (see `src/components/contact/ContactForm.astro` for access key and fields).
- Analytics: Cloudflare Web Analytics (cookie-free) is referenced in copy; no tracking cookies are set.

## Image Guidance
- Place project images under `src/assets/images/projects/<project-slug>/`.
- Use reasonably sized originals; Astro will generate responsive, optimized WebP outputs at build time.
