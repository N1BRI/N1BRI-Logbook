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

Create an empty GitHub repository named:

```text
N1BRI-Logbook
```

Then connect this local repo:

```sh
git remote add origin git@github.com:N1BRI/N1BRI-Logbook.git
git push -u origin main
```

In GitHub, configure Pages:

```text
Settings -> Pages -> Build and deployment -> Source -> GitHub Actions
```

After that, every push to `main` deploys the static site in `docs/`.

## Rebuild posts

```sh
npm run posts
```

## Local private log

The private ADIF file stays on this machine:

```text
data/logbook.adi
```

It is intentionally ignored by Git. Publish only the generated public files under `docs/`.
