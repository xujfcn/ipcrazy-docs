# ipcrazy-docs

Public documentation for [ipcrazy](https://ipcrazy.com), built with [Mintlify](https://mintlify.com).

## Local preview

Requires Node.js 20 or later.

```bash
npm i -g mint
mint dev            # http://localhost:3000
```

Before pushing:

```bash
mint validate
mint broken-links
```

## Structure

```
docs.json                   Site config: theme, colors, navigation (en + cn)
index.mdx, quickstart.mdx   English pages (default language)
products/ guides/ policies/ api-reference/
cn/                         Chinese pages, same paths under cn/
api-reference/openapi.json  OpenAPI spec for the public API endpoints
logo/, favicon.svg          Brand assets
```

Every English page has a Chinese counterpart under `cn/`. When you add a page, add both files and list them in the matching `navigation.languages` entry in `docs.json`.

## Content rules

- Document only what is live in the product. No "coming soon" features.
- Prices are in US dollars only.
- Use placeholders for hosts, ports, usernames, passwords and keys. Never commit real credentials, account data or order numbers.
- Console labels must match the console (English and Chinese).

## Publishing

Pushes to `main` deploy automatically once the Mintlify GitHub app is connected to this repository.
