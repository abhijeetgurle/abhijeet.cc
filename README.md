# Personal website

Blog and project showcase built with [Astro](https://astro.build), hosted for free on Cloudflare Pages.

## Develop

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # outputs to dist/
npm run check    # type-check
```

## Writing

- **Blog post:** add `src/content/blog/my-post.md` (or `.mdx`). The filename becomes the URL: `/blog/my-post/`.

  ```yaml
  ---
  title: My post
  description: One-line summary (used for SEO and RSS)
  date: 2026-10-10
  tags: [astro, notes]
  draft: true        # optional: hidden in production, visible in `npm run dev`
  ---
  ```

- **Project:** add `src/content/projects/my-project.md`.

  ```yaml
  ---
  title: My project
  description: What it does
  stack: [Go, Postgres]
  repo: https://github.com/you/my-project   # optional
  demo: https://my-project.example.com      # optional
  featured: true                            # show on the home page
  order: 1                                  # lower comes first
  ---
  ```

- **Site name, bio, social links:** `src/consts.ts`, `src/pages/about.md`, and the intro in `src/pages/index.astro`.

## Deploy (Cloudflare Pages, free)

1. Push this repo to GitHub.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick the repo.
3. Framework preset: **Astro**. Build command `npm run build`, output directory `dist`.
4. Set `site` in `astro.config.mjs` to the assigned `*.pages.dev` URL (or a custom domain later).

Every push to `main` deploys automatically, and pull requests get preview URLs.
