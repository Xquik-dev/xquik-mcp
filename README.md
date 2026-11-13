# X (Twitter) MCP Server & Data API by Xquik

[![Framer builds a tweet ticker with Xquik](https://img.youtube.com/vi/4UOSpoOoC3Y/maxresdefault.jpg)](https://youtu.be/4UOSpoOoC3Y?t=367)\
[Watch Framer build a tweet ticker with Xquik, from 6:07](https://youtu.be/4UOSpoOoC3Y?t=367).
This MCP server connects your agent to Xquik.

Use this X (Twitter) MCP server by Xquik to search X (Twitter) & export followers.
Your agent can also monitor accounts, post & send DMs from a connected account.

Xquik is the world's fastest and cheapest X (Twitter) scraper service with the most complete X (Twitter) data.
Most other Apify Actors charge before filtering or deduplication.
Xquik charges only for delivered, unique, filter-matching results and never pads rows.
Xquik is independent and not affiliated with X Corp.

<!-- trust:win:start -->

The Xquik REST API read 45 tweets per second on 2026-10-15. That cost $0.15 per 1,000. The fastest of 4 rival Actors read 12.5 per second. The cheapest cost $0.173 per 1,000. [Compare each run](https://xquik.com/benchmarks#benchmark-x-tweet-scraper). Most rival Actors charge before they filter or dedup. Xquik charges only for delivered, unique, filter-matching results.

<!-- trust:win:end -->

## Install the X (Twitter) MCP server

Point any MCP client at the hosted server.
Sign in through your client, and OAuth handles the token.

```text
https://xquik.com/mcp
```

Xquik has no free plan.
Pay-as-you-go credits start at $10 and never expire.
See prices in the [billing guide](https://docs.xquik.com/guides/billing) before your first paid request.

### Add the X (Twitter) MCP to Claude Code

Add the server with 1 command.

```bash
claude mcp add --transport http xquik https://xquik.com/mcp
```

Or install the plugin, which adds the Skill too.

```bash
/plugin install xquik --marketplace Xquik-dev/xquik-mcp
```

### Gemini CLI

```bash
gemini extensions install https://github.com/Xquik-dev/xquik-mcp
```

Then run `/mcp auth xquik` in Gemini CLI to sign in.

### Cline

Follow [llms-install.md](llms-install.md).

### Other clients

Read the [MCP setup guide](https://docs.xquik.com/mcp/overview).

## Search X (Twitter) with the X (Twitter) MCP server

Ask your agent in plain words.
It should call `search`, then `execute`.

```text
Find the 5 latest posts about AI agents on X and summarize them.
Show the profile & 10 latest posts of @NASA.
Estimate an export of @NASA's followers. Don't run it yet.
```

Next, read the [MCP tools reference](https://docs.xquik.com/mcp/tools) or the [REST API reference](https://docs.xquik.com/api-reference/overview).

<!-- trust:start -->

## Benchmarks & usage

[![X (Twitter) API p99 server read time](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Frest-p99.json)](https://xquik.com/benchmarks#speed)
[![X (Twitter) Skill installs](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fskill-installs.json)](https://xquik.com/benchmarks#skill-installs)

- 8.6 s p99 REST server read time over 7 days, failures included ([source](https://xquik.com/benchmarks#speed)) <!-- trust:rest-p99 8555 -->
- 1,600+ installs of Xquik's X (Twitter) Skills on skills.sh ([source](https://xquik.com/benchmarks#skill-installs)) <!-- trust:skill-installs 1640 -->

Checked on 2026-11-13. See each number with its date & source on [xquik.com/benchmarks](https://xquik.com/benchmarks) or as [JSON](https://xquik.com/trust.json).

<!-- trust:end -->

## Tools

| Tool | What it does | Cost |
| --- | --- | --- |
| `docs` | Searches the Xquik documentation. | Free |
| `search` | Runs JavaScript your agent writes on Xquik's servers to find an API operation. | Free |
| `execute` | Runs JavaScript your agent writes on Xquik's servers to call the API. | The called route's price |
| `whoami` | Shows the Xquik account this connection uses. | Free |

The Claude plugin connects to `https://xquik.com/mcp?app=claude`.
There, `execute` only reads, and `executeWrite` makes changes such as posts and DMs.
The plugin's `xquik-mcp` Skill teaches your agent the tools, costs & confirmation rules.

## Data & privacy

- This repository runs no local code. It has no hooks, scripts or bundled servers.
- Your client sends tool inputs to `xquik.com`.
- `docs` queries reach a hosted documentation search service.
- `search`, `execute` and `executeWrite` run your agent's JavaScript on Xquik's servers.
- Tweets, posts & DMs you approve reach X (Twitter).
- Webhook events go to the URLs you set.
- Your client runs OAuth 2.1 and stores the token.
- The Skill makes your agent ask before private reads, metered bulk jobs & writes.
- The [privacy policy](https://xquik.com/en/privacy) and [terms](https://xquik.com/en/terms) cover what Xquik stores.

## Questions

### Do I need an X (Twitter) developer account?

No. Public reads need only an Xquik API key.
Private reads & X (Twitter) account actions need a connected account.

### Is this the official X API?

No. Xquik runs its own REST API.
The MCP server calls that API, not the official X API.

## More Xquik tools

- [X (Twitter) scraper API & X (Twitter) MCP server](https://github.com/Xquik-dev/x-twitter-scraper) with REST, MCP & Skill setup.
- X (Twitter) API SDKs for [TypeScript](https://github.com/Xquik-dev/x-twitter-scraper-typescript), [Python](https://github.com/Xquik-dev/x-twitter-scraper-python), [Go](https://github.com/Xquik-dev/x-twitter-scraper-go) & [Ruby](https://github.com/Xquik-dev/x-twitter-scraper-ruby).
- X (Twitter) API SDKs for [Java](https://github.com/Xquik-dev/x-twitter-scraper-java), [Kotlin](https://github.com/Xquik-dev/x-twitter-scraper-kotlin), [C#](https://github.com/Xquik-dev/x-twitter-scraper-csharp) & [PHP](https://github.com/Xquik-dev/x-twitter-scraper-php).
- [Twitter CLI & X CLI](https://github.com/Xquik-dev/x-twitter-scraper-cli) for terminal workflows.
- [X API alternative skill](https://github.com/Xquik-dev/x-api) and [Twitter advanced search operators](https://github.com/Xquik-dev/x-twitter-advanced-search) with tested examples.
- Twitter agent plugins for [OpenClaw](https://github.com/Xquik-dev/tweetclaw) & [Hermes Agent](https://github.com/Xquik-dev/hermes-tweet).
- [X (Twitter) API documentation source](https://github.com/Xquik-dev/xquik-docs) with every public page.
- Twitter integrations for [n8n](https://github.com/Xquik-dev/n8n-nodes-xquik), [Prefect](https://github.com/Xquik-dev/prefect-xquik), [Haystack](https://github.com/Xquik-dev/xquik-haystack) & [Paperclip](https://github.com/Xquik-dev/paperclip-plugin-xquik).
- Twitter integrations for [Terraform](https://github.com/Xquik-dev/terraform-provider-x-twitter-scraper), [Convex](https://github.com/Xquik-dev/xquik-convex), [Supabase](https://github.com/Xquik-dev/xquik-supabase) & [Strapi](https://github.com/Xquik-dev/strapi-plugin-xquik).
- X (Twitter) MCP for [VS Code](https://github.com/Xquik-dev/xquik-vscode) & [Raycast](https://github.com/Xquik-dev/xquik-raycast).
- [Xquik X API & Twitter scraper](https://xquik.com) and the [X (Twitter) API documentation](https://docs.xquik.com/api-reference/overview).

## Help

- Email [support@xquik.com](mailto:support@xquik.com).
- Read the [MCP docs](https://docs.xquik.com/mcp/overview).

Xquik is an independent third-party service. Not affiliated with X Corp. "Twitter" and "X" are trademarks of X Corp.
