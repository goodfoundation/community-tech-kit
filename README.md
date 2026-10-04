# Community Tech Kit

Practical technology resources for community organizations: free and
discounted software, accounting best practices, and QuickBooks automation
guides. A [Good Software Foundation](https://goodfoundation.github.io)
project.

The site is a static Jekyll build deployed to GitHub Pages.

## Local development

```sh
./serve.sh
```

Then open <http://127.0.0.1:4000/community-tech-kit/>. The script handles
bundler setup; it requires Ruby >= 2.7 (install with `brew install ruby` if
needed).

## Structure

```
_data/discounts.yml     Discounted & free software directory (cards on /discounts/)
_data/resources.yml     The three resource tracks shown on the home page
_guides/                Long-form guides (collection, rendered at /guides/:slug/)
assets/                 Styles (Sass) and JS
_includes/  _layouts/    Shared header, footer, icons, page layouts
.github/workflows/      GitHub Pages deploy on push to main
```

## Contributing

- **Add a software deal:** append an entry to `_data/discounts.yml`.
- **Add a guide:** create a markdown file in `_guides/` with `title`,
  `description`, `category`, `icon` and `date` front matter.
- Everything is plain markdown/YAML — no build tooling beyond Jekyll.