# Twitter MCP Server & X Data API by Xquik

This Twitter MCP server connects your agent to Xquik's hosted X MCP.

Xquik is the world's fastest and cheapest X Twitter data API with the most
complete X data. Searches & extractions charge only for delivered, unique,
filter-matching results and never pad rows.

Your agent can
search posts, read profiles, export followers and monitor accounts. It can also
post and send DMs through an X account you connect.

> Xquik is an independent third-party service. Not affiliated with X Corp.
> "Twitter" and "X" are trademarks of X Corp.

## Install the Twitter MCP server

Point any MCP client at the hosted server.

```text
https://xquik.com/mcp
```

Xquik has no free plan. Pay-as-you-go credits start at $10 and never expire.
See prices on [xquik.com](https://xquik.com) before your first paid request.

### Add the X MCP to Claude Code

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

## Xquik in Framer's video

<table>
  <tr>
    <td align="center">
      <a href="https://youtu.be/4UOSpoOoC3Y?t=367">
        <img src="https://img.youtube.com/vi/4UOSpoOoC3Y/maxresdefault.jpg" alt="Framer uses Xquik to build a tweet ticker" width="720">
      </a>
      <br>
      <sub>Framer uses Xquik to build a tweet ticker at 6:07 of <a href="https://youtu.be/4UOSpoOoC3Y?t=367">Connect Framer to Claude Code, ChatGPT Codex, Cursor, and more</a>.</sub>
    </td>
  </tr>
</table>

## Xquik usage

Developers run Xquik through MCP, REST, SDKs and Apify. These numbers cover all
of Xquik, and most come from Apify. Each one links to its source.

[![Runs of Xquik's Apify Actors](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fapify-runs.json)](https://apify.com/xquik)
[![Users summed across Xquik's Apify Actors](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fapify-users.json)](https://apify.com/xquik)
[![Accounts on xquik.com](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Faccounts.json)](https://xquik.com/trust#accounts)
[![Package downloads](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fdownloads.json)](https://xquik.com/trust#downloads)
[![REST API median server read time](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Frest-p50.json)](https://xquik.com/trust#speed)
[![Repos passing OpenSSF Best Practices](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fopenssf-passing.json)](https://xquik.com/trust#security)
[![GitHub stars](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fgithub-stars.json)](https://github.com/Xquik-dev)

| Measure | Number | Source |
| --- | --- | --- |
| Runs of Xquik's Apify Actors | 7,600,000+ | [Apify](https://apify.com/xquik) |
| Users summed across Xquik's Apify Actors | 10,000+ | [Apify](https://apify.com/xquik) |
| Accounts on xquik.com | 4,200+ | [Trust page](https://xquik.com/trust#accounts) |
| Downloads across npm, PyPI, RubyGems, NuGet, Packagist & Terraform | 55,000+ | [Trust page](https://xquik.com/trust#downloads) |
| Rating of Xquik's most-used Actor | 4.66 of 5 from 16 reviews | [Trust page](https://xquik.com/trust#apify-rating) |
| Median REST API server read time over 7 days | 664 ms | [Trust page](https://xquik.com/trust#speed) |
| Xquik repositories passing OpenSSF Best Practices | 17 | [Trust page](https://xquik.com/trust#security) |
| GitHub stars across Xquik's repositories | 390+ | [GitHub](https://github.com/Xquik-dev) |

Checked on 2026-11-03. See every number with its date on
[xquik.com/trust](https://xquik.com/trust) or as
[JSON](https://xquik.com/trust.json).

## What you get

| Part | What it does |
| --- | --- |
| `xquik` MCP server | Connects to `https://xquik.com/mcp` over Streamable HTTP. |
| `xquik-mcp` Skill | Teaches your agent the tools, costs & confirmation rules. |

## Tools

| Tool | What it does | Cost |
| --- | --- | --- |
| `docs` | Searches the Xquik documentation. | Free |
| `search` | Runs JavaScript your agent writes on Xquik's servers to find an API operation. | Free |
| `execute` | Runs JavaScript your agent writes on Xquik's servers to call the API. | The called route's price |
| `whoami` | Shows the Xquik account this connection uses. | Free |

The Claude plugin connects to `https://xquik.com/mcp?app=claude`. There, `execute`
only reads, and `executeWrite` makes changes such as posts and DMs.

## Sign in

Sign in to Xquik through your client. OAuth handles the token.

## Try it

- "Find the 5 latest posts about AI agents on X and summarize them."
- "Show the profile & 10 latest posts of @NASA."
- "Estimate an export of @NASA's followers. Don't run it yet."

Your agent should call `search`, then `execute`.

## Data & privacy

- This repository runs no local code. It has no hooks, scripts or bundled servers.
- Your client sends tool inputs to `xquik.com`.
- `docs` queries reach a hosted documentation search service.
- `search`, `execute` and `executeWrite` run your agent's JavaScript on Xquik's servers.
- Posts and DMs you approve reach X.
- Webhook events go to the URLs you set.
- Your client runs OAuth 2.1 and stores the token.
- The Skill tells your agent to ask before private reads, metered bulk jobs and writes.
- The [privacy policy](https://xquik.com/en/privacy) and
  [terms](https://xquik.com/en/terms) cover what Xquik stores.

## Questions

### Do I need an X developer account?

No. Public reads need only an Xquik API key. Private reads & X account actions
need a connected X account.

### Is this the official X API?

No. Xquik is an independent third-party service with its own REST API. The MCP server
calls that API, not the official X API.

## Links

- [MCP docs](https://docs.xquik.com/mcp/overview)
- [Website](https://xquik.com)
- [Support](mailto:support@xquik.com)

## More Xquik tools

- [X (Twitter) scraper API & Twitter MCP server](https://github.com/Xquik-dev/x-twitter-scraper) with REST, MCP & Skill setup.
- Twitter API SDKs for [TypeScript](https://github.com/Xquik-dev/x-twitter-scraper-typescript), [Python](https://github.com/Xquik-dev/x-twitter-scraper-python), [Go](https://github.com/Xquik-dev/x-twitter-scraper-go), [Ruby](https://github.com/Xquik-dev/x-twitter-scraper-ruby), [Java](https://github.com/Xquik-dev/x-twitter-scraper-java), [Kotlin](https://github.com/Xquik-dev/x-twitter-scraper-kotlin), [C#](https://github.com/Xquik-dev/x-twitter-scraper-csharp) & [PHP](https://github.com/Xquik-dev/x-twitter-scraper-php).
- [Twitter CLI & X CLI](https://github.com/Xquik-dev/x-twitter-scraper-cli), the [X API alternative skill](https://github.com/Xquik-dev/x-api) and [Twitter advanced search operators](https://github.com/Xquik-dev/x-twitter-advanced-search) with tested examples.
- Twitter agent plugins for [OpenClaw](https://github.com/Xquik-dev/tweetclaw) & [Hermes Agent](https://github.com/Xquik-dev/hermes-tweet), and the [Twitter API documentation source](https://github.com/Xquik-dev/xquik-docs).
- Twitter integrations for [n8n](https://github.com/Xquik-dev/n8n-nodes-xquik), [Prefect](https://github.com/Xquik-dev/prefect-xquik), [Haystack](https://github.com/Xquik-dev/xquik-haystack), [Paperclip](https://github.com/Xquik-dev/paperclip-plugin-xquik), [Terraform](https://github.com/Xquik-dev/terraform-provider-x-twitter-scraper), [Convex](https://github.com/Xquik-dev/xquik-convex), [Supabase](https://github.com/Xquik-dev/xquik-supabase) & [Strapi](https://github.com/Xquik-dev/strapi-plugin-xquik).
- Twitter MCP for [AI agents](https://github.com/Xquik-dev/xquik-mcp), [VS Code](https://github.com/Xquik-dev/xquik-vscode) & [Raycast](https://github.com/Xquik-dev/xquik-raycast).
- [Xquik X API & Twitter scraper](https://xquik.com) and the [Twitter API documentation](https://docs.xquik.com/api-reference/overview).
