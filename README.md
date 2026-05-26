# N1BRI Logbook

This is the public, read-only logbook and radio blog for N1BRI.

Live site:

```text
https://n1bri.github.io/N1BRI-Logbook/
```

The site is generated from a local ADIF log and published through GitHub Pages. Visitors can search and filter contacts, view operating stats, browse the contact map, and read archived posts.

## Privacy

The private source log stays local:

```text
data/logbook.adi
```

That file is ignored by Git. The public site uses sanitized generated data under:

```text
docs/data/
```

## Maintenance

Rebuild blog posts:

```sh
npm run posts
```

Deploy changes:

```sh
git add docs content data/settings.json README.md
git commit -m "Update logbook site"
git push
```

GitHub Actions deploys the `docs/` folder to GitHub Pages after each push to `main`.
