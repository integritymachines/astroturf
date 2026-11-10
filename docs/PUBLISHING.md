# Publishing guide

## File names and URLs

Use the article's lowercase shorthand as the filename: `wpic.md`, `scc.md`, `esvm.md`, or `did-d.md`. The filename is the canonical URL slug, so `wpic.md` becomes `/posts/wpic`.

The optional `shorthand` frontmatter field is for displaying or citing the abbreviation. It does not override the URL.

## Frontmatter

Every article starts with:

```yaml
---
layout: ../../layouts/MarkdownPostLayout.astro
title: A specific, descriptive title
shorthand: SHORT
description: A one- or two-sentence summary for previews and search results.
pubDate: 2026-11-10
author:
  - "@oliverbeige"
affiliation:
  - "@integritymachines"
version: "1.0"
---
```

`title`, `pubDate`, and `version` are required. `description` is strongly recommended and becomes the page metadata.

`author` and `affiliation` accept either one quoted GitHub handle or a YAML list of quoted handles. They default to `@oliverbeige` and `@integritymachines`. Handles are rendered as links to their GitHub profiles. The version links to the Git commit history for the source article and exposes an anchor such as `#v1-0`.

Use an ISO 8601 date (`YYYY-MM-DD`) and do not set a future date unless publication is intentionally scheduled.

## Assets and links

- Store assets for `wpic.md` in `public/images/wpic/`.
- Reference public assets with root-relative URLs, such as `/images/wpic/chart.png`.
- Prefer SVG for diagrams and PNG or WebP for raster images. Compress large files before committing.
- Use stable primary sources where possible and check every external link.
- Add useful alt text. If an image is purely decorative, use empty alt text.

## Review checklist

- The title, shorthand, summary, authors, affiliations, version, and date are correct.
- Claims, equations, citations, and code have received domain review.
- Headings form a sensible hierarchy and code fences specify a language.
- The article works in narrow and wide viewports.
- `npm run check` and `npm run build` pass.
- The production preview has been checked with `npm run preview`.
- The pull request includes screenshots for layout or styling changes.

## Corrections and versions

Make factual corrections directly and explain them in the pull request. Increment `version` for a material revision. For a material change to a published conclusion, add a clearly dated editor's note rather than silently rewriting the record.
