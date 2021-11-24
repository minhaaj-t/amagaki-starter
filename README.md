# amagaki-starter

[![NPM Version][npm-image]][npm-url]
[![GitHub Actions][github-image]][github-url]
[![TypeScript Style Guide][gts-image]][gts-url]

A minimal starter project that uses the [Amagaki](https://amagaki.dev) website generator.

## Features

- Reusable partial HTML templates (Nunjucks).
- Responsive image macro using a combination of `srcset` and `media`.
- Per-partial CSS splitting.
- TypeScript compilation with tree-shaking for minimal payloads.
- Opinionated autofixing and linting.

## Usage

```shell
# Install dependencies.
npm install

# Run the development server.
npm run dev

# Build the static site.
npm run build
```

`amagaki-starter` uses the
[`@amagaki/amagaki-plugin-page-builder`](https://github.com/blinkk/amagaki-plugin-page-builder).
The page builder plugin generates the core markup for each page and manages
partials. Partials are standalone, isolated modules that can be mixed and
matched to approach page building by assembling reusable modules.

### How to build pages

1. Create partials by adding files in the following locations:

```
/src/sass/partials/{partial}.sass
/src/ts/partials/{partial}.ts
/views/partials/{partial}.njk
```

2. Create pages by mixing and matching partials:

```
/content/pages/{page}.yaml
```

[github-image]: https://github.com/blinkk/amagaki-starter/workflows/Build%20site/badge.svg
[github-url]: https://github.com/blinkk/amagaki-starter/actions
[npm-image]: https://img.shields.io/npm/v/@amagaki/amagaki-starter.svg
[npm-url]: https://npmjs.org/package/@amagaki/amagaki-starter
[gts-image]: https://img.shields.io/badge/code%20style-google-blueviolet.svg
[gts-url]: https://github.com/google/gts
