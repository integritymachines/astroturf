# Contributing

Contributions should be proposed through a pull request. Keep each pull request focused and preserve the voice and claims of existing articles.

## Article changes

- Follow [`docs/PUBLISHING.md`](docs/PUBLISHING.md).
- Use kebab-case filenames and keep article assets under a matching directory in `public/images/`.
- Give fenced code blocks a language identifier.
- Prefer descriptive link text and image alt text.
- Explain substantive edits to an already-published article in the pull request.

## Code changes

- Match the surrounding Astro, TypeScript, and CSS style.
- Avoid adding runtime JavaScript when static HTML and CSS are sufficient.
- Run `npm run check` and `npm run build` before requesting review.
- Include screenshots for visible changes.
