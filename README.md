# Crucible Mesh — Configuration Reference Site

A static site documenting the radio and network configuration for the Crucible experimental LoRa mesh network. Built with [Eleventy](https://www.11ty.dev/) and deployed via Cloudflare Pages.

## Editing content

All content lives in `src/index.md`. It is plain Markdown — edit headings, paragraphs, tables, and code blocks as you normally would. The design is applied automatically by the template.

To change the layout or visual style, edit `src/_includes/base.njk`.

## Running locally

```bash
npm install
npm run dev
```

Opens at `http://localhost:8080` with live reload.

## Building

```bash
npm run build
```

Output goes to `_site/`.

## Deployment

The site is hosted on Cloudflare Pages. Every push to `main` triggers an automatic deploy.

**Cloudflare Pages build settings:**

| Setting | Value |
|---|---|
| Build command | `npm run build` |
| Build output directory | `_site` |
| Environment variable | `NODE_VERSION = 18` |
