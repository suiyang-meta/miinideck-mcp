# miinideck — MCP server

> Publish the HTML your AI builds to a **private, share-ready link** — without leaving the chat.

**miinideck** is a remote [Model Context Protocol](https://modelcontextprotocol.io) server. Connect it once to Claude or ChatGPT, and the AI can turn any self-contained HTML it generates — a landing page, a report, a slide deck, a one-pager — into a private, unguessable link. No deploy pipeline, no public exposure, no file or terminal to touch.

- **Homepage:** https://www.miinideck.com
- **Connect / docs:** https://www.miinideck.com/mcp
- **Connect URL:** `https://www.miinideck.com/api/mcp`
- **Transport:** Streamable HTTP (OAuth)

## What it does

| Tool | What it does |
|---|---|
| `create_page` | Publish a self-contained HTML page to a private, unguessable link. |
| `update_page` | Revise a page in place — the link you already shared shows the new version. |
| `list_pages` | List the pages you've published. |

Every page gets a 32-character unguessable URL and is `noindex` by default — no search engine finds it, and only people you send the link to can open it. Optional password and expiry.

## Connect

It's a URL you paste in — nothing to install.

**Claude** (Free, Pro, or Max) — Settings → Connectors → *Add custom connector* → paste:

```
https://www.miinideck.com/api/mcp
```

**ChatGPT** (Plus or above, developer-mode connectors) — add a connector with the same URL.

Works with Claude, ChatGPT, Cursor, Cline, or any MCP client. Then just ask your AI to publish what it built.

## Why

You build something with AI in seconds, then waste minutes figuring out how to share it without emailing a file or putting it on the open web. miinideck is the private-delivery layer: a link you control, private by default, that opens in any browser with no sign-up for the viewer.

If your app needs a real backend (a server, a database, auth), that's a job for a deploy platform like [Vercel](https://vercel.com) or [Netlify](https://netlify.com) — miinideck is for the front-end pages you share.

## Also available

- **CLI:** [`miinideck`](https://www.npmjs.com/package/miinideck) on npm — `npx miinideck` to publish from your terminal.
- **Claude Skill** — a one-file upload, see https://www.miinideck.com/mcp.

## License

MIT — see [LICENSE](./LICENSE). This repo is the public manifest + docs for the hosted miinideck MCP server; the service itself runs at miinideck.com.
