# Presend

**Free, privacy-first browser tools — nothing is ever uploaded.**

[presend.pages.dev](https://presend.pages.dev) is 48 tools that run entirely client-side (EXIF/metadata removal, PDF/image compression, format conversion, file integrity checks) plus a **free, no-signup, no-API-key server-side API** with 42 endpoints -- including Cosmos SDK transaction decoding and OFAC sanctions checks -- and an MCP server for AI agents.

## What makes it different

Most free file tools quietly upload your file to a server to process it. Presend's tools do the work locally in your browser with Web APIs (Canvas, Web Crypto, FileReader) — the file never leaves your device.

The API's most distinctive endpoint, `maintainer-change-check`, flags an npm package whose publisher changed after a long period of dormancy — the exact pattern behind real supply-chain attacks like `event-stream`, `ua-parser-js`, and `colors.js`. Nothing else free does this specific check.

## Repos

- **[presend](https://github.com/presendapp/presend)** — the site + API (Cloudflare Pages Functions)
- **[presend-examples](https://github.com/presendapp/presend-examples)** — working code for LangChain, CrewAI, LlamaIndex, OpenAI Agents SDK, Google ADK
- **[presend-mcp-config](https://github.com/presendapp/presend-mcp-config)** — copy-paste MCP setup for Claude Desktop, Cursor, Windsurf, no code required
- **[presend-check-action](https://github.com/presendapp/presend-check-action)** — GitHub Action for dependency security scanning (npm + PyPI), on the [GitHub Marketplace](https://github.com/marketplace/actions/presend-dependency-security-check)
- **[presend-extension](https://github.com/presendapp/presend-extension)** — browser extension: right-click any image to strip EXIF/GPS on-device
- **[presend-api](https://github.com/presendapp/presend-api)** — zero-dependency npm client ([npmjs.com/package/presend-api](https://www.npmjs.com/package/presend-api))

- [security-research](https://github.com/presendapp/security-research) — responsible-disclosure writeups, published post-fix only

## Try it

```bash
curl "https://presend.pages.dev/api/maintainer-change-check?ecosystem=npm&package=lodash"
```

Full docs: [presend.pages.dev/api](https://presend.pages.dev/api) · OpenAPI spec: [openapi.json](https://presend.pages.dev/openapi.json) · MCP server: [presend.pages.dev/mcp](https://presend.pages.dev/mcp) · [Postman collection](https://presend.pages.dev/api)

## Contributions

Merged upstream in other open-source projects:

- [public-apis/public-apis](https://github.com/public-apis/public-apis/pull/7326) — added Presend to the Security section (481k stars)
- [public-api-lists/public-api-lists](https://github.com/public-api-lists/public-api-lists/pull/695) — added Presend to the Security section
- [anondotli/awesome-privacy-tools](https://github.com/anondotli/awesome-privacy-tools/pull/26) — added Presend's EXIF Remover + PDF Metadata Remover

## Built with

Vanilla JS, Cloudflare Pages + Pages Functions, no framework, no build step for the client-side tools. No ads, no tracking, no cookies.
