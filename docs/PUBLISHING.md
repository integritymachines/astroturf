# Publishing guide

## Frontmatter

Every article starts with:

```yaml
---
layout: ../../layouts/MarkdownPostLayout.astro
title: A specific, descriptive title
description: A one- or two-sentence summary for previews and search results.
pubDate: 2026-10-27
author: Author Name
---
```

`title` and `pubDate` are required by the current index and layout. `description` is strongly recommended and becomes the page's metadata. `author` is optional for historical posts, but new Integrity Machines publications should include it.

Use an ISO 8601 date (`YYYY-MM-DD`) and do not set a future date unless publication is intentionally scheduled by the deployment system.

## Assets and links

- Store assets for `example-post.md` in `public/images/example-post/`.
- Reference public assets with root-relative URLs, such as `/images/example-post/chart.png`.
- Prefer SVG for diagrams and PNG or WebP for raster images. Compress large files before committing them.
- Use stable primary sources where possible and check every external link.
- Add useful alt text. If an image is purely decorative, use empty alt text.

## Review checklist

- The title, summary, author, and date are correct.
- Claims, equations, citations, and code have received domain review.
- Headings form a sensible hierarchy and code fences specify a language.
- The article works in narrow and wide viewports and in light and dark modes.
- `npm run check` and `npm run build` pass.
- The production preview has been checked with `npm run preview`.
- The pull request includes screenshots for layout or styling changes.

## Corrections

Make factual corrections directly and explain them in the pull request. For a material change to a published conclusion, add a clearly dated editor's note to the article rather than silently rewriting the record.
