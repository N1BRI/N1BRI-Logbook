# N1BRI Logbook

Personal GitHub Pages deployment for N1BRI Logbook.

## What is committed

- `docs/`: generated public site and sanitized public log data
- `content/posts/`: Markdown blog source
- `data/settings.json`: public profile/site settings
- `scripts/build-posts.js`: static Markdown post builder

## What stays local

- `data/logbook.adi` is ignored by Git because ADIF exports may contain private fields such as names, email addresses, exact locations, and notes.

## GitHub Pages

Configure GitHub Pages to serve from:

```text
main /docs
```

## Rebuild posts

```sh
npm run posts
```
