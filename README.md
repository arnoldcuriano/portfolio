# Arnold Curiano portfolio

Phase 0 foundation for a static Astro portfolio. Content and visual sections are intentionally pending.

## Local development

Requires Node.js 22.12 or newer.

```sh
npm ci
npm run dev
```

## Checks

```sh
npm run format:check
npm run check
npm run build
```

Blog entries will live in `src/content/blog` as Markdown or MDX. The collection is empty until approved writing is available.

The site builds as static files for Vercel. Before launch, set the production `site` URL in `astro.config.mjs` so canonical URLs and a sitemap can be generated. No domain has been chosen yet.
