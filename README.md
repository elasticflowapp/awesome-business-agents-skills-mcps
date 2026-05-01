# Awesome Business AI Agents, Skills and MCP list

[![Skills](https://img.shields.io/badge/skills-174-blue?style=flat-square)](#contents)
[![Departments](https://img.shields.io/badge/departments-6%20live%20%2F%2010-blue?style=flat-square)](#contents)
[![Last Update](https://img.shields.io/github/last-commit/elasticflowapp/awesome-business-agents-skills-mcps?style=flat-square&label=last%20update)](#contents)
[![License](https://img.shields.io/badge/license-MIT%20%2B%20CC--BY--SA-green?style=flat-square)](LICENSE)

> Hand-curated AI agents, Claude Skills, and MCP (Model Context Protocol) servers for business teams. Organized by **Department → Role → Task → Entry** across Sales, Marketing, Legal, Product, Customer Success, and General. 174 entries hand-picked from real publishers — no AI-bulk-generated content. Compatible with Claude Code, Codex, Gemini, OpenClaw, Hermes, and ChatGPT.

## Contents

- 🎯 [Customer Success](departments-en/customer-success.md) — 8 skills _(catalog roles pending)_
- 💰 Finance _(no skills in catalog yet)_
- 🧰 [General](departments-en/general.md) — 1 role · 11 skills
- 🧑‍🤝‍🧑 HR _(no skills in catalog yet)_
- ⚖️ [Legal](departments-en/legal.md) — 3 roles · 13 skills
- 📣 [Marketing](departments-en/marketing.md) — 6 roles · 81 skills
- ⚙️ Operations _(no skills in catalog yet)_
- 🚀 [Product](departments-en/product.md) — 18 skills _(catalog roles pending)_
- 💼 [Sales](departments-en/sales.md) — 7 roles · 43 skills
- 📦 Supply Chain _(no skills in catalog yet)_

## Legend

Each entry follows this shape:

```
- [Name](catalog-url) `/command` — One-sentence description. ([Source](github-url)) _Type · Publisher · Platforms · Setup · Pricing · Trust_
```

Tokens in the metadata trailer:

- **Type**: `Skill` · `MCP` · `Agent` · `Plugin` · `Workflow`
- **Platforms**: `Claude` · `Codex` · `ChatGPT` · `Gemini` · `OpenClaw` · `Hermes`
- **Setup**: `No-code` · `API key` · `OAuth` · `IT-assisted` · `Self-hosted`
- **Pricing**: `Free` · `Freemium` · `Paid` · `Enterprise`
- **Trust** _(optional, last token)_: `✅ Verified` · `🔒 SOC2` · `🇪🇺 GDPR-compliant` · `📂 Open source`

**Role emojis** used in `## Quick path by role` blocks inside each department file. Click a role to jump to its tasks in the relevant department file:

**General**

- 👤 [Founder](departments-en/general.md#quick-path-by-role)

**Legal**

- 👔 [General Counsel](departments-en/legal.md#quick-path-by-role)
- 📄 [Contract Manager](departments-en/legal.md#quick-path-by-role)
- ⚖️ [Corporate Counsel](departments-en/legal.md#quick-path-by-role)

**Marketing**

- 📈 [Growth Marketer](departments-en/marketing.md#quick-path-by-role)
- 🎨 [Product Marketer](departments-en/marketing.md#quick-path-by-role)
- 📣 [Demand Generation Manager](departments-en/marketing.md#quick-path-by-role)
- ✍️ [Content Marketer](departments-en/marketing.md#quick-path-by-role)
- 🔍 [SEO Specialist](departments-en/marketing.md#quick-path-by-role)
- 🚀 [Marketing Lead](departments-en/marketing.md#quick-path-by-role)

**Sales**

- 👔 [VP Sales](departments-en/sales.md#quick-path-by-role)
- 🤝 [Account Executive](departments-en/sales.md#quick-path-by-role)
- 🧭 [Sales Manager](departments-en/sales.md#quick-path-by-role)
- 🎯 [SDR / BDR](departments-en/sales.md#quick-path-by-role)
- 👥 [Account Manager / CSM](departments-en/sales.md#quick-path-by-role)
- 🛠️ [RevOps](departments-en/sales.md#quick-path-by-role)
- 💼 [Sales rep](departments-en/sales.md#quick-path-by-role)

See [CONTRIBUTING.md](CONTRIBUTING.md#closed-dictionaries) for the full closed-dictionary spec.

## Mission

Most awesome-MCP and awesome-skill lists organize by technology category — databases, file systems, browser automation. That works for developers picking infrastructure. It doesn't work for a sales lead, legal counsel, or marketing manager who arrives looking for an AI tool to solve their problem today.

This list is **organized by business function**: department → role → task → entry. A Contract Manager opens [`departments-en/legal.md`](departments-en/legal.md), finds the "Contract Review" section, picks an entry, installs it. No translation from tech-speak required.

## Purpose & Audience

**Principles:**

- **Hand-picked, not bulk-generated.** Every entry is a real skill or MCP from a real publisher, used by real teams.
- **Business-first taxonomy.** Departments and roles match how companies are actually structured — not how engineers categorize code.
- **One-sentence-per-entry.** Skim, don't read. Each entry tells you what it does in a single sentence and where to install it.
- **Deep-links to install + source.** No dead ends — entry name links to the install page; parenthetical Source links to the open GitHub repo.

**Built for:**

- **Sales leaders** picking AI for follow-up, pipeline review, signal-based outbound, deal strategy.
- **In-house counsel and contract managers** for contract review, NDA triage, vendor checks, GDPR/PCI compliance, board briefings.
- **Marketing managers** evaluating SEO, ad creative, conversion optimization, competitive intelligence, content production.
- **Product managers** searching for discovery, PRD writing, roadmap prioritization, AI evals.
- **CSMs and RevOps leads** scoring account health, planning QBRs, designing renewal motions and CRM workflows.
- **Founders** wearing every hat, looking for a vetted starting point per domain — fundraising, hiring, marketing foundations.

## Glossary

The list catalogues five entry types. Each has alternative names you might encounter elsewhere — included so search and LLM queries match.

- **Skill** — a prepackaged instruction set for an AI client, invoked via slash command (e.g., `/review-contract`). _Also known as: Claude Skill, slash command, agent skill, AI command, slash skill, agent prompt._
- **MCP server** — a Model Context Protocol server that exposes tools, resources, or prompts to an AI client over a standardized interface. _Also known as: MCP, MCP service, Model Context Protocol server, MCP tool provider._
- **Agent** — an autonomous multi-step worker that uses skills and MCP servers to accomplish a task end-to-end. _Also known as: AI agent, autonomous agent, agentic AI, LLM agent._
- **Plugin** — a bundled installer combining multiple skills (and optionally MCP servers) under one publisher and persona. _Also known as: skill bundle, AI plugin, plugin pack._
- **Workflow** — a multi-step orchestration that chains skills, MCP servers, and triggers to automate a recurring business process end-to-end. _Also known as: AI workflow, agent workflow, automated playbook._

The catalog uses **Department → Role → Task → Entry** as the navigation hierarchy. A _Department_ maps to a business function (Sales, Legal, Marketing, etc.); a _Role_ to a job title (VP Sales, Account Executive, SDR / BDR); a _Task_ to a recurring outcome (Contract Review, Pipeline Forecasting); an _Entry_ to a specific Skill, MCP server, Agent, Plugin, or Workflow that addresses that task.

## Compatibility

Works across **Claude Code**, **Codex**, **Gemini**, **OpenClaw**, and **Hermes**. Each entry deep-links to its install page on [ElasticFlow Hub](https://elasticflow.app/hub) and to its open-source GitHub repo.

## Frequently Asked Questions

### What is Awesome Business AI?

A curated list of AI agents, Claude Skills, and MCP servers for business teams, organized by department, role, and task. 174 entries across 6 live departments — Sales, Marketing, Legal, Product, Customer Success, and General — hand-maintained against the [ElasticFlow Hub](https://elasticflow.app/hub) catalog.

### What's the difference between a Skill, MCP server, and Agent?

A **Skill** is a prepackaged instruction set invoked via slash command in an AI client (e.g., `/review-contract`). An **MCP server** is a Model Context Protocol service that exposes tools to an AI client over a standardized interface — for example, a Salesforce MCP server lets the AI read and write CRM data. An **Agent** is an autonomous multi-step worker that combines skills and MCP servers to complete a task end-to-end. Full definitions and synonyms in [Glossary](#glossary).

### What makes this list different?

It's organized by **business function** — Department → Role → Task → Entry — for the operator side: sales leaders, in-house counsel, marketing managers, product managers, CSMs, founders. Other awesome-AI lists typically organize by technology category (databases, file systems, browser automation) or by publisher, which is the right structure for developers picking infrastructure but the wrong one for a business reader looking to solve a specific problem. Every entry is hand-picked from a real publisher and tagged with department, role, task, type, platforms, setup complexity, pricing, and trust signals — no AI-bulk-generated content.

### How are entries vetted?

Every entry is hand-picked from a real publisher — no AI-bulk-generated content. Trust signals are surfaced per entry in the metadata trailer: `✅ Verified` for verified publishers, `🔒 SOC2`, `🇪🇺 GDPR-compliant`, `📂 Open source`.

### How do I install these tools?

Each entry's name links to its install page on [ElasticFlow Hub](https://elasticflow.app/hub), where you configure and install for your AI client (Claude Code, Codex, Gemini, OpenClaw, Hermes, ChatGPT). The parenthetical `(Source)` link goes to the open-source GitHub repository.

## Community

- 💡 **[Suggest an entry](https://github.com/elasticflowapp/awesome-business-agents-skills-mcps/discussions/categories/ideas)** — propose a new skill, MCP server, or agent without opening a PR.
- 🙏 **[Ask which tool fits your use case](https://github.com/elasticflowapp/awesome-business-agents-skills-mcps/discussions/categories/q-a)** — describe your situation, get a recommendation from the community.
- 🙌 **[Show and tell](https://github.com/elasticflowapp/awesome-business-agents-skills-mcps/discussions/categories/show-and-tell)** — share what's working in your stack.
- 🐛 **[Report a broken link or stale entry](https://github.com/elasticflowapp/awesome-business-agents-skills-mcps/issues/new)** — open an Issue.
- 📄 **[Contribute via Pull Request](CONTRIBUTING.md)** — add a new entry, task, or department.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to:
- Add a new department from the catalog
- Add an entry to an existing task
- Add a new task to an existing department

PRs welcome. Edit a markdown file, push, done.

## License

MIT for entry data. CC-BY-SA for editorial content. See [LICENSE](LICENSE).
