# Presend

**Free, privacy-first browser tools — the file tools never upload your files.**

[presend.pages.dev](https://presend.pages.dev) is 48 browser tools — the file tools (EXIF/metadata removal, PDF/image compression, format conversion, file integrity checks) run entirely client-side, while some other tools call our API or an online service plus a **free, no-signup, no-API-key server-side API** with 48 endpoints -- including Cosmos SDK transaction decoding and OFAC sanctions checks -- and an MCP server for AI agents.

## What makes it different

Most free file tools quietly upload your file to a server to process it. Presend's file tools do the work locally in your browser with Web APIs (Canvas, Web Crypto, FileReader) — the file never leaves your device.

The API's most distinctive endpoint, `maintainer-change-check`, flags an npm package whose publisher changed after a long period of dormancy — the pattern behind the `event-stream` compromise (2018). It cannot see a hijacked existing account (`ua-parser-js`) or a malicious release by the original maintainer (`colors.js`), and a handover to a publisher who already maintains other widely used packages is reported without being flagged.

## For teams

We are testing a paid offer for teams: the same dependency checks on every pull request that changes a dependency and for AI coding agents before they install a package, with false-positive rates measured and published. Nothing is for sale yet. If your team would use it, [join the waitlist](https://presend.pages.dev/teams).

## Repos

- **[presend-source](https://github.com/presendapp/presend-source)** — the site + API (Cloudflare Pages Functions)
- **[presend-examples](https://github.com/presendapp/presend-examples)** — working code for LangChain, CrewAI, LlamaIndex, OpenAI Agents SDK, Google ADK
- **[presend-mcp-config](https://github.com/presendapp/presend-mcp-config)** — copy-paste MCP setup for Claude Desktop, Cursor, Windsurf, no code required
- **[presend-check-action](https://github.com/presendapp/presend-check-action)** — GitHub Action for dependency security scanning (npm + PyPI), on the [GitHub Marketplace](https://github.com/marketplace/actions/presend-dependency-security-check)
- **[presend-extension](https://github.com/presendapp/presend-extension)** — browser extension: right-click any image to strip EXIF/GPS on-device
- **[presend-api](https://github.com/presendapp/presend-api)** — zero-dependency npm client ([npmjs.com/package/presend-api](https://www.npmjs.com/package/presend-api))

- [security-research](https://github.com/presendapp/security-research) — responsible-disclosure writeups, published post-fix only

_Edited 2026-10-01: the browser-tools claim now covers the file tools only; some other tools (for example IP geolocation, link preview, DNS lookup, speech-to-text, online text-to-speech voices) call our API or an online service; third-party services are listed in the [privacy policy](https://presend.pages.dev/privacy)._

## Try it

```bash
curl "https://presend.pages.dev/api/maintainer-change-check?ecosystem=npm&package=lodash"
```

Full docs: [presend.pages.dev/api](https://presend.pages.dev/api) · OpenAPI spec: [openapi.json](https://presend.pages.dev/openapi.json) · MCP server: [presend.pages.dev/mcp](https://presend.pages.dev/mcp) · Also on [RapidAPI](https://rapidapi.com/presendapp/api/presend-api) (split into Cybersecurity, Finance, and Email listings) · [Postman collection](https://presend.pages.dev/api)

## Contributions

Merged upstream in other open-source projects:

- [public-apis/public-apis](https://github.com/public-apis/public-apis/pull/7326) — added Presend to the Security section (481k stars)
- [public-api-lists/public-api-lists](https://github.com/public-api-lists/public-api-lists/pull/695) — added Presend to the Security section
- [anondotli/awesome-privacy-tools](https://github.com/anondotli/awesome-privacy-tools/pull/26) — added Presend's EXIF Remover + PDF Metadata Remover

## Built with

Vanilla JS, Cloudflare Pages + Pages Functions, no framework, no build step for the client-side tools. No ads. Anonymous visit counts only (Cloudflare Web Analytics).
