# Website Check-up by SEO Records

A complete check-up of a public website in one conversation: how search engines read it (SEO), whether AI assistants can read and quote it (GEO), and its security basics — turned into one prioritized action plan, with the evidence for each finding and the way to fix it by hand.

## What it contains

**Two skills**

- `website-checkup` — runs the SEO check, the AI-readiness check and the security basics on the address you give, then sorts every finding into *fix now*, *fix this month* and *improve when possible*. For a given page it can return the exact tags to add, a corrected robots.txt or a draft llms.txt.
- `audit-report-plan` — turns a purchased Audit SEO Records report (or an Effect SEO Records monthly crawl) into a step-by-step plan, and fixes the cited pages one by one.

**Four remote MCP servers**, declared in `.mcp.json`, all run by EUROPE TECHNOLOGIE:

| Server | Address | What it does |
|---|---|---|
| SEO Records | `https://api.seorecords.com/mcp` | SEO check, AI crawler access, audit report reading, product offers |
| SEO Records Corrector | `https://api.seorecords.com/mcp/corrector` | Exact SEO corrections for a page, with their source |
| GEO SEO Records | `https://api.seorecords.com/mcp/geo` | Readiness for AI assistants, corrected robots.txt, draft llms.txt |
| AI Website Security | `https://scan.aiwebsitesecurity.com/api/mcp` | HTTPS certificate, redirection, security headers, mixed content, DNS filtering |

## Access pass

The checks require an access key, and **each server has its own**: **€9.90 for 24 hours** (one-time payment) or **€29 per month** (cancel anytime), per server, bought at [seorecords.com/en/assistants#pass](https://seorecords.com/en/assistants#pass). After payment the key (`pass_…`) is shown on screen.

- Paste it in the conversation: Claude passes it to the tools of that server.
- Or set it once, before starting Claude Code — the plugin sends each one to its server as the `x-access-key` header:

| Server | Variable |
|---|---|
| SEO Records | `SEO_RECORDS_ACCESS_KEY` |
| SEO Records Corrector | `SEO_RECORDS_CORRECTOR_ACCESS_KEY` |
| GEO SEO Records | `GEO_SEO_RECORDS_ACCESS_KEY` |
| AI Website Security | `AI_WEBSITE_SECURITY_ACCESS_KEY` |

Without its key, a check answers with the two ways to buy the pass of that server. The tools that return offers, payment links or a purchased audit report work without a key. Nothing is bought without the person paying on the Stripe or storefront page themselves.

## What is sent, and where

- The website address you ask about is sent to the servers above, which read the **public** pages of that site the way a visitor does. To compare DNS filtering, AI Website Security asks the public resolvers of Cloudflare and Quad9 about the domain.
- An audit report is read only from the private link its buyer shares.
- The content of your conversation stays in Claude; the servers receive only the arguments of each tool call.
- Privacy policies: [SEO Records connectors](https://seorecords.com/en/assistants#donnees) · [AI Website Security connector](https://aiwebsitesecurity.com/en/assistants#donnees).

The plugin itself runs no code on your machine: it is two skills and the addresses of four remote servers.

## Install

Install it from the Claude directory, then ask, for example: *"Give me a full check-up of example.com: what should I fix first?"*

## Support

contact@seorecords.com · Publisher: EUROPE TECHNOLOGIE (France)

## License

MIT
