# Xquik X (Twitter) Data API MCP Server

Xquik is the world's fastest and cheapest X Twitter data API with the most
complete X data. Searches & extractions charge only for delivered, unique,
filter-matching results and never pad rows.

This repository connects your agent to Xquik's hosted MCP server. Your agent can
search posts, read profiles, export followers and monitor accounts. It can also
post and send DMs through an X account you connect.

> Xquik is an independent third-party service. Not affiliated with X Corp.
> "Twitter" and "X" are trademarks of X Corp.

## See it in action

<table>
  <tr>
    <td align="center">
      <a href="https://youtu.be/4UOSpoOoC3Y?t=367">
        <img src="https://img.youtube.com/vi/4UOSpoOoC3Y/maxresdefault.jpg" alt="Framer connects Xquik MCP to coding agents" width="720">
      </a>
      <br>
      <strong>Xquik in Framer's video</strong>
      <br>
      <sub>Framer connects the Xquik MCP server at 6:07 of <a href="https://youtu.be/4UOSpoOoC3Y?t=367">Connect Framer to Claude Code, ChatGPT Codex, Cursor, and more</a>.</sub>
    </td>
  </tr>
</table>

## Used at scale

Developers run Xquik through MCP, REST, SDKs and Apify. Each number links to its
public source.

[![Runs of Xquik's Apify Actors](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fapify-runs.json)](https://apify.com/xquik)
[![Users of Xquik's Apify Actors](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fapify-users.json)](https://apify.com/xquik)
[![Accounts on xquik.com](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Faccounts.json)](https://xquik.com/trust#accounts)
[![Package downloads](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fdownloads.json)](https://xquik.com/trust#downloads)
[![Reviews on Apify](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fapify-reviews.json)](https://xquik.com/trust#reviews)
[![REST API median server read time](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Frest-p50.json)](https://xquik.com/trust#speed)
[![Repos passing OpenSSF Best Practices](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fopenssf-passing.json)](https://xquik.com/trust#security)
[![GitHub stars](https://img.shields.io/endpoint?url=https%3A%2F%2Fxquik.com%2Fbadges%2Fgithub-stars.json)](https://github.com/Xquik-dev)

| Measure | Number | Source |
| --- | --- | --- |
| Runs of Xquik's Apify Actors | 7,600,000+ | [Apify](https://apify.com/xquik) |
| Users of Xquik's Apify Actors | 10,000+ | [Apify](https://apify.com/xquik) |
| Accounts on xquik.com | 4,200+ | [Trust page](https://xquik.com/trust#accounts) |
| Downloads across npm, PyPI, RubyGems, NuGet, Packagist & Terraform | 55,000+ | [Trust page](https://xquik.com/trust#downloads) |
| Apify reviews | 56 | [Trust page](https://xquik.com/trust#reviews) |
| Rating of Xquik's most-used Actor | 4.66 of 5 | [Trust page](https://xquik.com/trust#apify-rating) |
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
| `search` | Finds the right API operation for a task. | Free |
| `execute` | Runs JavaScript your agent writes on Xquik's servers to call the API. | The called route's price |
| `whoami` | Shows the Xquik account this connection uses. | Free |

## Set up

Xquik has no free plan. Pay-as-you-go credits start at $10 and never expire.
Read [pricing](https://xquik.com/pricing) before your first paid request.

### Claude Code

```bash
/plugin install xquik --marketplace Xquik-dev/xquik-mcp
```

### Gemini CLI

```bash
gemini extensions install https://github.com/Xquik-dev/xquik-mcp
```

### Cline

Follow [llms-install.md](llms-install.md).

### Other clients

Read the [MCP setup guide](https://docs.xquik.com/mcp/overview).

## Sign in

Sign in to Xquik when your client asks. OAuth handles the token.

## Try it

- "Find the 5 latest posts about AI agents on X and summarize them."
- "Show the profile & 10 latest posts of @NASA."
- "Estimate an export of @NASA's followers. Don't run it yet."

Your agent should call `search`, then `execute`.

## Data & privacy

- This repository runs no local code. It has no hooks, scripts or bundled servers.
- Your client sends tool inputs to `xquik.com`.
- `docs` queries reach a hosted documentation search service.
- `execute` runs on Xquik's servers and calls the Xquik API.
- Posts and DMs you approve reach X.
- Webhook events go to the URLs you set.
- Your client runs OAuth 2.1 and stores the token.
- The Skill tells your agent to ask before private reads, metered bulk jobs and writes.
- The [privacy policy](https://xquik.com/en/privacy) and
  [terms](https://xquik.com/en/terms) cover what Xquik stores.

## Links

- [MCP docs](https://docs.xquik.com/mcp/overview)
- [Pricing](https://xquik.com/pricing)
- [Support](mailto:support@xquik.com)
