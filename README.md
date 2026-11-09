# AgingResearch.News for Claude

Every new paper on aging and longevity, read and judged as it lands by [AgingResearch.News](https://agingresearch.news), in Claude chat, Cowork and Claude Code.

AgingResearch.News reads the new papers on aging from bioRxiv, medRxiv, PubMed, arXiv and Europe PMC, judges each one for its link to aging, and writes short stories about the ones worth reading, each checked against its paper. This plugin connects Claude to its server and adds a skill that tells Claude which tool answers which question.

## What you can ask

- "What's the latest evidence that rapamycin slows aging in people?" The evidence on a drug, gene or process as structure: the species it has reached, whether independent labs found the same, findings against it, trials and those with no results posted, funders and company ties. Never a grade.
- "Which senolytic trials are recruiting now?"
- "What's new in aging research this week?"
- "Follow taurine on AgingResearch.News and tell me what's new this week." (needs an AgingResearch.News account)

## Commands

- `/agingresearch-news:whats-new senolytics`: what's new this week on a subject, or across the field with no subject.
- `/agingresearch-news:evidence rapamycin`: the evidence on a drug, supplement, gene or process, by species, independent replication, findings against, trials and funders.
- `/agingresearch-news:trials sarcopenia`: trials for a condition, drug or target, recruiting and completed.

In Claude chat, pick them from the `/` menu, or just ask: Claude applies the one that fits.

## Setup

In Claude Code:

    /plugin marketplace add paperfoot/agingresearch-news-plugin
    /plugin install agingresearch-news@agingresearch-news-plugin

In Claude chat and Cowork, add it from the directory. The first time a tool needs your account, Claude asks you to sign in with AgingResearch.News (OAuth); public lookups work before that. In Claude Code, run `/mcp`, choose agingresearch-news, then Authenticate; a free account gives 100 lookups a day. Every connected app is listed in Settings, Agents & API on agingresearch.news, where Disconnect ends its access.

The server is `https://agingresearch.news/api/mcp`. Setup for other assistants: https://agingresearch.news/connect

## What it contains

- `.mcp.json`: the AgingResearch.News MCP server.
- `skills/aging-research/SKILL.md`: when to use each tool and how to describe evidence.
- `commands/`: the three commands above.

## Privacy Policy

The tools receive only the arguments Claude sends to a tool, such as a drug's name or search words, never your conversation. AgingResearch.News does not store those arguments or send them to an AI model provider. It counts lookups for a week to apply the daily allowance, and keeps your consent and the app's tokens until you disconnect. Full policy: https://agingresearch.news/privacy#assistants. Terms: https://agingresearch.news/terms.

## Support

https://agingresearch.news/contact

## License

The plugin's files are under the MIT License. AgingResearch.News's content and data are governed by its terms.
