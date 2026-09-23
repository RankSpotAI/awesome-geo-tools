# Awesome GEO Tools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Generative Engine Optimization tools, compared on what they actually do. Which AI engines each one tracks, how often it refreshes, what it costs, and whether you can get the data out.

GEO, also called AEO or AI search visibility, is the practice of measuring and improving how often your brand shows up when someone asks ChatGPT, Claude, Gemini, Perplexity or Google's AI Overviews a question about your market.

There are already several lists of GEO tools. Most are link dumps. This one is a comparison table, because the only questions that matter when picking one of these are which engines it covers, how often it checks, what it costs, and whether you can pull the data into your own stack. Every figure below was read off the vendor's own pricing page in September 2026.

---

**Maintained by [RankSpot](https://www.rankspot.ai/)**, and we are a GEO tool ourselves, so read this list knowing that. RankSpot sits in the table below with the same columns as everyone else, including the columns where competitors beat us. If you find an error in a rival's row, [correct it](CONTRIBUTING.md) and we will merge it.

---

## Contents

- [How to read this list](#how-to-read-this-list)
- [Dedicated AI visibility platforms](#dedicated-ai-visibility-platforms)
- [AI visibility inside an SEO suite](#ai-visibility-inside-an-seo-suite)
- [Tools that act, not just measure](#tools-that-act-not-just-measure)
- [Open source and self-hosted](#open-source-and-self-hosted)
- [Free ways to check your AI visibility](#free-ways-to-check-your-ai-visibility)
- [AI crawler analytics](#ai-crawler-analytics)
- [Also in the category](#also-in-the-category)
- [What to look for when choosing](#what-to-look-for-when-choosing)
- [Gaps worth filling](#gaps-worth-filling)
- [Related lists](#related-lists)
- [Contributing](#contributing)

## How to read this list

| Column | Meaning |
| --- | --- |
| **Engines** | Which AI systems the tool checks. `AIO` is Google AI Overviews, `AI Mode` is Google's conversational search surface. These are separate products and a tool covering one may not cover the other. |
| **Refresh** | How often prompts are re-run. Daily is the norm. Weekly is cheaper to run and fine for slow-moving markets, but you will miss short-lived swings. |
| **From** | Cheapest paid entry point per month. A `~` means the vendor does not publish a price and the figure comes from secondary sources, so treat it as a rough guide. |
| **API** | Whether you can pull your own data out programmatically, and on which tier. |
| **MCP** | Whether an AI agent can query the tool directly. See [awesome-seo-mcp](https://github.com/RankSpotAI/awesome-seo-mcp) for how those connect. |

Two warnings about the entry price. It usually buys a small prompt allowance, and prompts are the real unit of cost, so a $99 plan with 25 prompts can work out dearer than a $189 plan with 100. And several vendors gate engines behind tiers, so the cheapest plan often watches one engine, not all of them.

**Prices change.** Everything here was checked in September 2026. Check the vendor before you buy.

## Dedicated AI visibility platforms

Built for this job and nothing else.

| Tool | Engines | Refresh | From | API | MCP |
| --- | --- | --- | --- | --- | --- |
| [Profound](https://www.tryprofound.com/) | ChatGPT only at entry, up to 9 engines on Enterprise | Daily | $99 | Enterprise only | No |
| [Peec AI](https://peec.ai/) | ChatGPT, Perplexity, Gemini and others | Not published | ~$95 | Yes | Yes |
| [Otterly.ai](https://otterly.ai/) | ChatGPT, AIO, Perplexity, Copilot. Claude, Gemini and AI Mode are paid add-ons | Daily | $29 | From $189 tier | No |
| [Rankscale](https://rankscale.ai/) | ChatGPT, Perplexity, AIO, AI Mode, Gemini, Claude, Copilot, Grok, DeepSeek, Mistral and more, 18 in total | Hourly to monthly | $20 | From $385 tier | No |
| [AthenaHQ](https://www.athenahq.ai/) | ChatGPT, Perplexity, AIO, AI Mode, Gemini, Claude, Copilot, Grok, DeepSeek, Meta AI | Continuous | Free tier, then $295 | Paid add-on | No |
| [RankSpot](https://www.rankspot.ai/) | ChatGPT, Claude, Gemini, AIO | Weekly | $99 | Via MCP | Yes |
| [Scrunch](https://scrunch.com/) | ChatGPT, Perplexity, Claude, Gemini, Copilot | Not published | Not published | Not published | No |

A note on reading that table honestly: Rankscale covers by far the most engines for the least money, Otterly has the lowest entry price, and Profound has the deepest enterprise story. RankSpot refreshes weekly where most of this table refreshes daily, which matters if you are in a fast-moving market.

## AI visibility inside an SEO suite

If you already pay for one of these, start here before buying a dedicated tool. You may already have it.

| Tool | Engines | Refresh | From | API | MCP |
| --- | --- | --- | --- | --- | --- |
| [Ahrefs Brand Radar](https://ahrefs.com/brand-radar) | AIO, Gemini, Perplexity, ChatGPT, Copilot, AI Mode | Daily | $50 custom prompts, or $199 for the AI Visibility Index. Needs a paid Ahrefs plan | Yes | Yes |
| [SE Visible](https://visible.seranking.com/) | AI Mode, AIO, Gemini, Perplexity, ChatGPT. Claude announced | Daily | $99 for 200 prompts | Yes | Yes |
| [Semrush AI Visibility](https://www.semrush.com/) | ChatGPT, AIO, AI Mode, Gemini, Perplexity, Claude | Daily | ~$99 for 25 prompts and 1 domain | Yes | Yes |

Ahrefs is the outlier worth understanding. Its AI Visibility Index is built on a corpus of hundreds of millions of real prompts people actually typed, rather than only the prompts you think to track. That is a genuinely different data asset, and it is priced accordingly.

## Tools that act, not just measure

Most of this category reports a number and stops. These go further and change something, which is a different product even though it is sold under the same label.

- **[Profound](https://www.tryprofound.com/)** has an agent action layer on its enterprise tier.
- **[Scrunch](https://scrunch.com/)** delivers AI-optimised content to crawlers through its Agent Experience Platform.
- **[AthenaHQ](https://www.athenahq.ai/)** includes a content optimisation agent.
- **[RankSpot](https://www.rankspot.ai/)** generates and publishes articles and produces a weekly prioritised action list.

Worth deciding early which kind you want, because measurement tools and action tools are priced and evaluated completely differently.

## Open source and self-hosted

Thin, and worth saying plainly: there is no open-source equivalent of Profound or Peec. Running real visibility tracking means paying for model calls at volume, which does not suit a free project. What does exist is tooling around the edges.

| Project | What it does | Licence | Stars | Updated |
| --- | --- | --- | --- | --- |
| [alexpospekhov/searchstack-aeo](https://github.com/alexpospekhov/searchstack-aeo) | Open-source AEO, GEO and SEO stack aimed at AI-native founders | none | 97 | 2026-05-04 |
| [jdillard/sphinx-llms-txt](https://github.com/jdillard/sphinx-llms-txt) | llms.txt generator for Sphinx documentation | MIT | 33 | 2026-08-03 |
| [apify/actor-llmstxt-generator](https://github.com/apify/actor-llmstxt-generator) | Crawls a site and builds an llms.txt from its content | Apache-2.0 | 32 | 2026-05-25 |
| [4hse/astro-llms-txt](https://github.com/4hse/astro-llms-txt) | llms.txt generation for Astro sites | MIT | 22 | 2026-04-21 |
| [aircodelabs/llms-txt-generator](https://github.com/aircodelabs/llms-txt-generator) | Generates llms.txt and llms-full.txt | MIT | 19 | 2025-06-18 |
| [nermalcat69/astro-llms-generate](https://github.com/nermalcat69/astro-llms-generate) | Minimal llms.txt generator for Astro | MIT | 18 | 2025-08-25 |
| [Cairrot-Inc/cloudflare-ai-crawler-tracker](https://github.com/Cairrot-Inc/cloudflare-ai-crawler-tracker) | Cloudflare Worker that detects and logs AI crawler traffic at the edge | MIT | 1 | 2026-04-01 |

There are also several open-source MCP servers that audit AI readiness, llms.txt and per-bot robots.txt rules. Those live in [awesome-seo-mcp](https://github.com/RankSpotAI/awesome-seo-mcp#ai-search-visibility-geo-and-aeo).

## Free ways to check your AI visibility

Before paying anyone, these cost nothing and answer most of the early questions.

- **Just ask the models.** Open ChatGPT, Claude, Gemini and Perplexity, ask the ten questions a customer would ask before buying from you, and write down who gets named. This is the whole category in manual form and it is free. Do it before you buy a tool, so you know what the tool should be telling you.
- **Check your server logs** for `GPTBot`, `ClaudeBot`, `PerplexityBot`, `Google-Extended`, `CCBot`, `Bytespider` and `Meta-ExternalAgent`. If none of them appear, no tool will fix that, your content is not being fetched.
- **[Cloudflare AI Crawl Control](https://www.cloudflare.com/)**, free if you are already on Cloudflare, shows which AI crawlers hit your site and lets you allow or block them per bot.
- **Free tiers.** AthenaHQ has a free tier with starting credit, and several tools listed below run free one-off checkers.
- **[AI Visibility Audit](https://ai-visibility.rowb.app/)**, free one-off checker (3 audits/day without signup, 50/month with a free key). Reads your robots.txt AI-bot rules, llms.txt, JSON-LD, meta tags and sitemap and returns a score with fixes; also callable as a remote MCP tool (`audit_website`). Built by [rowb](https://rowb.app/) — disclosure: this is a self-submission.

## AI crawler analytics

A different question from visibility: not "does AI mention me" but "does AI even read me". Underserved as a category.

- **[Cloudflare AI Crawl Control](https://www.cloudflare.com/)**, per-bot visibility and control, free on existing plans.
- **[Cairrot-Inc/cloudflare-ai-crawler-tracker](https://github.com/Cairrot-Inc/cloudflare-ai-crawler-tracker)**, self-hosted edge worker if you want the raw log.
- **[Scrunch](https://scrunch.com/)** includes crawler-level analytics alongside its monitoring.
- **Your own access logs**, which nobody sells you and which contain the answer.

## Also in the category

Tools that come up repeatedly in the space and that we have not yet verified to the standard of the tables above. Listed so the list is honest about its coverage rather than pretending the category is only ten tools.

[ZipTie](https://ziptie.dev/), [LLMrefs](https://llmrefs.com/), [Arobis](https://arobis.ai/), [LLM Pulse](https://llmpulse.ai/), [Local Falcon](https://www.localfalcon.com/) for local and map visibility, [SEOmonitor](https://www.seomonitor.com/) for AI Overview tracking inside rank tracking.

Known by name but not yet verified, and we would take a PR adding any of them properly: Goodie AI, Evertune, Trakkr, Knowatoa, Gauge, Daydream, Bluefish AI, Writesonic GEO, Waikay, Hall, Rankability, Fokal, Conductor, BrightEdge.

## What to look for when choosing

The questions that actually separate these tools, in rough order of how much they matter.

1. **Which engines, on the plan you can afford.** Nearly every vendor advertises broad coverage and then gates most of it behind higher tiers. Check the engine list on the specific plan you would buy, not the marketing page.
2. **How prompts are counted.** Prompts are the unit of cost. A prompt run daily against six engines may count as one prompt or as thirty checks depending on the vendor. This is the single biggest source of surprise bills.
3. **Whether you can get your data out.** An API or MCP server is the difference between a dashboard you log into and data you can join against your own analytics. Several tools here have no export at any price.
4. **Whether it tells you what to do.** Measurement is now commodity. The harder question is what to change, and only some of these attempt an answer.
5. **Whether it tracks the prompts you care about or the prompts people actually ask.** Most tools track prompts you write yourself, which measures what you already thought of. A corpus of real user prompts finds the demand you missed.
6. **Sentiment and citation sources, not just mention counts.** Being mentioned negatively, or being mentioned while a competitor is cited as the source, are different problems from not being mentioned.

## Gaps worth filling

- **An open-source visibility tracker.** Nothing credible exists, because model calls at volume cost money. A self-hosted tool that used your own API keys would fill a real hole.
- **Prompt-cost normalisation.** No neutral way to compare what a plan actually buys across vendors that count prompts differently.
- **Log-based attribution.** Connecting AI crawler hits to later AI citations is not solved by anyone.
- **Shared benchmarks.** Every vendor grades its own homework. There is no public dataset of who gets cited for which queries over time.
- **Small-site pricing.** The category floor is around $29 and most useful plans start near $99. Nothing serves a site that needs to track five prompts.

## Related lists

- [awesome-seo-mcp](https://github.com/RankSpotAI/awesome-seo-mcp), MCP servers for SEO including the AI visibility ones. Also maintained by us.
- [awesome-seo-agent-skills](https://github.com/RankSpotAI/awesome-seo-agent-skills), Agent Skills for SEO and GEO work. Also maintained by us.
- [josezuma/awesome-ai-visibility](https://github.com/josezuma/awesome-ai-visibility), AI visibility resources including crawler datasets.
- [DavidHuji/Awesome-GEO](https://github.com/DavidHuji/Awesome-GEO), the academic side, research papers on generative engine optimisation.

## Contributing

Corrections are especially welcome here, including corrections to entries for tools that compete with RankSpot. Prices and engine coverage in this category change monthly. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0](LICENSE). No rights reserved, copy it freely.

---

Maintained by [RankSpot](https://www.rankspot.ai/). If you want to know whether ChatGPT, Claude and Gemini recommend your brand, that is the problem we work on.
