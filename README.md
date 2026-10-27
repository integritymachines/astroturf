# Integrity Machines publications

The source for Integrity Machines research notes and technical writing. The site is a small, static [Astro](https://astro.build) project with Markdown posts and MathML rendering.

## Local development

Use Node.js 22 or newer.

```sh
npm ci
npm run dev
```

Before opening a pull request, run the same checks as CI:

```sh
npm run check
npm run build
```

## Publish an article

1. Copy [`docs/post-template.md`](docs/post-template.md) to `src/pages/posts/<slug>.md`.
2. Fill in the frontmatter and write the article in Markdown.
3. Put article-specific images in `public/images/<slug>/` and reference them from `/images/<slug>/...`.
4. Run the checks above and preview the production build with `npm run preview`.
5. Open a pull request. Merging it makes the post eligible for the site's deployment process.

See [`docs/PUBLISHING.md`](docs/PUBLISHING.md) for the editorial and technical checklist.

## Project structure

```text
public/                 Static fonts, icons, images, and video
src/components/         Reusable Astro components
src/layouts/            Page and article layouts
src/pages/posts/        Published Markdown articles
src/styles/             Shared styles
```

## License

Copyright belongs to Integrity Machines and the respective article authors. No open-source or content license is granted unless a file states otherwise.
