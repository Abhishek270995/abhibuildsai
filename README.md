# Abhi Builds AI

Portfolio and publishing site for Abhishek Kumar Singh, built with Astro and deployed to Vercel. It includes static portfolio pages, a Markdown blog with RSS and sitemap output, and browser-only SQL and CSV demonstrations.

## Requirements

- Node.js 22.12 or newer
- npm

## Develop

```sh
npm ci
npm run dev
```

Astro serves the local site at `http://localhost:4321`.

## Validate and build

```sh
npm run check
npm run build
npm run preview
```

`check` runs Astro diagnostics and TypeScript checks. `build` creates the production site in `dist/`; `preview` serves that build locally.

GitHub Actions runs the check and production build on pull requests and pushes to `main`. Vercel is connected to this repository for deployments. Production uses the `main` branch; pull requests should be reviewed in their Vercel preview before merge.

## Site content

- Pages live in `src/pages/`.
- Blog posts are Markdown or MDX files in `src/content/blog/` and use the schema in `src/content.config.ts`.
- Shared components are in `src/components/`; global styling is in `src/styles/global.css`.
- Public assets live in `public/`.

## Browser tools

The SQL page is a deterministic, rule-based demonstration with sample patterns. It does not call an AI model, run SQL against a database, or measure query plans or cost savings. Review all generated examples and replace sample table and column names before use. The CSV auditor processes pasted data in the browser; the static site does not send that input to a backend.

## Deployment notes

The canonical site URL is configured in `astro.config.mjs`. Vercel project settings and verified custom domains are managed in the Vercel dashboard. Do not commit credentials or environment files.
