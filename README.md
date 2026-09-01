# Presend

**Free, privacy-first browser tools — nothing is ever uploaded.**

[presend.pages.dev](https://presend.pages.dev) is a collection of **40 tools** that run entirely client-side (EXIF/metadata removal, PDF/image compression, format conversion, file integrity checks) plus a **free, no-signup, no-API-key server-side API** with 32 endpoints for developers.

## What makes it different

Most free file tools quietly upload your file to a server to process it. Presend's 38 of 40 tools do the work locally in your browser with Web APIs (Canvas, Web Crypto, FileReader) — the file never leaves your device. The 2 exceptions (IP lookup, link preview) are clearly labeled as server-side, since that's inherent to what they do.

The API layer takes the same "no friction" philosophy further: no account, no API key, and several endpoints **chain multiple operations into one call** — hash a file *and* check it against a known-malware database, decode a QR code *and* check the URL it contains for phishing, merge PDFs *and* compress the result — instead of making you call three separate free APIs and glue the results together yourself.

## Repos

- **[presend](https://github.com/presendapp/presend)** — the site + API (Cloudflare Pages Functions)
- **[presend-extension](https://github.com/presendapp/presend-extension)** — browser extension: right-click any image to strip EXIF/GPS on-device
- **[presend-api](https://github.com/presendapp/presend-api)** — zero-dependency npm client for the API ([npmjs.com/package/presend-api](https://www.npmjs.com/package/presend-api))

## Try the API

```bash
curl "https://presend.pages.dev/api/hash" -X POST --data-binary @file.pdf
```

Full docs: [presend.pages.dev/api](https://presend.pages.dev/api) · OpenAPI spec: [openapi.json](https://presend.pages.dev/openapi.json) · [Postman collection](https://presend.pages.dev/api)

## Built with

Vanilla JS, Cloudflare Pages + Pages Functions, no framework, no build step for the client-side tools. No ads, no tracking, no cookies.
