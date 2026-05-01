# Contributing

Pull requests welcome. Edit a markdown file, push, that's it. No build pipeline, no YAML, no scripts.

Reference implementation: [`departments-en/legal.md`](departments-en/legal.md).

## Repository layout

```
README.md                       # Department grid, project intro
CONTRIBUTING.md                 # This file
LICENSE
departments-en/
  legal.md                      # One file per department
  marketing.md
  ...
.github/
  PULL_REQUEST_TEMPLATE.md
```

One department = one file. Tasks live as H2 sections inside it. No nested role files.

## Department file skeleton

Every department file follows this exact skeleton:

```markdown
# <Department Name>

> One-sentence tagline.

← Back to [all departments](../README.md#contents)

## Quick path by role

- <emoji> **[Role 1](catalog-role-url)** — [Task A](#task-a) · [Task B](#task-b) · also: [Task X](#task-x)
- <emoji> **[Role 2](catalog-role-url)** — [Task C](#task-c) · [Task D](#task-d)

## Contents

- [Task A](#task-a)
- [Task B](#task-b)
- [Task C](#task-c)
- [Related departments](#related-departments)

## Task A

- [Entry](catalog-url) `/command` — Description. ([Source](github-url)) _Type · Publisher · Platforms · Setup · Pricing · Trust_

## Related departments

[Department X](department-x.md) · [Department Y](department-y.md)
```

If a department has no roles defined in the catalog yet, skip the `## Quick path by role` section and add a one-line note at the top explaining the gap.

## Entry-line format

Every entry is one bullet:

```
- [Name](catalog-url) `/command` — One-sentence description. ([Source](github-url)) _Type · Publisher · Platforms · Setup · Pricing · Trust_
```

Components, in order:

| Position | Token | Required | Notes |
|----------|-------|----------|-------|
| 1 | `[Name](catalog-url)` | **Required** | Plain link, NOT bold. Link target = canonical page on `elasticflow.app/hub/...` |
| 2 | `` `/command` `` | If applicable | Slash command in monospace. Skip when entry has no command. |
| 3 | ` — ` (em-dash) + description | **Required** | One sentence. Period at end. Factual, not marketing. |
| 4 | `([Source](github-url))` | When source is open | GitHub repo or subdirectory. Use `_(closed source)_` for proprietary entries. |
| 5 | ` _Type · Publisher · Platforms · Setup · Pricing · Trust_` | **Required** | Italics. ` · `-separated. Order matters. |

### Closed dictionaries

Every value in the metadata trailer comes from these closed lists.

**Type** (always first token):
- `Skill` · `MCP` · `Agent` · `Plugin` · `Workflow`

**Setup** (complexity tier):
- `No-code` · `API key` · `OAuth` · `IT-assisted` · `Self-hosted`

**Pricing**:
- `Free` · `Freemium` · `Paid` · `Enterprise`

**Trust signals** (optional, last token, only when applicable):
- `✅ Verified` — publisher verified by ElasticFlow
- `🔒 SOC2` · `🇪🇺 GDPR-compliant` · `📂 Open source`

**Platforms** (CLI / agent surfaces a skill or MCP runs on):
- `Claude` (Anthropic — Claude Code CLI, claude.ai/code)
- `Codex` (OpenAI — Codex CLI)
- `ChatGPT` (OpenAI — chat.openai.com)
- `Gemini` (Google — Gemini CLI)
- `OpenClaw` (ElasticFlow — open-source agent runtime)
- `Hermes` (ElasticFlow — managed agent runtime)

### Examples

```markdown
- [Contract review](https://elasticflow.app/hub/anthropic/plugins/legal/skills/review-contract) `/review-contract` — GREEN / YELLOW / RED per clause with redline language. ([Source](https://github.com/anthropics/knowledge-work-plugins/tree/main/legal/skills/review-contract)) _Skill · Anthropic · Claude · No-code · Free · ✅ Verified_

- [Calendar MCP](https://elasticflow.app/hub/mcps/calendar) — Read/write calendar events. ([Source](https://github.com/modelcontextprotocol/servers/tree/main/src/calendar)) _MCP · ModelContextProtocol · OAuth · Free · 📂 Open source_

- [Sales Pipeline Agent](https://elasticflow.app/hub/agents/sales-pipeline) — Autonomous: researches prospects, drafts outreach, books meetings end-to-end. ([Source](https://github.com/elasticflow/agents/tree/main/sales-pipeline)) _Agent · ElasticFlow · Claude · OAuth · Paid_
```

## Task naming rules

Tasks are H2 headings inside a department file.

- **Outcome-named**, not tool-named. ✅ "Contract Review" / ❌ "Salesforce Tasks"
- **2-3 words**. ✅ "NDA Triage" / ❌ "Triaging incoming non-disclosure agreements"
- **Verb-able by the role**. The role _does_ the task.
- **Stable**. The H2 heading is the URL anchor — renames break inbound links.

If a task spans multiple roles, list it once under its primary task heading and mention secondary roles in `## Quick path by role` via the `also:` prefix.

## Quick path by role

A department's roles are listed at `elasticflow.app/hub/skills/roles/<dept>/`. Each role gets one bullet:

```
- <emoji> **[Role Name](https://elasticflow.app/hub/skills/roles/<dept>/<role-slug>)** — [Task A](#task-a) · [Task B](#task-b) · also: [Task X](#task-x)
```

Rules:
- One bullet per role in the department.
- Bold the role link. Link target = catalog role page.
- List task anchors separated by ` · `.
- Use `also:` prefix when the role has secondary involvement in a task whose primary owner is a different role.
- Pick a role emoji from the standard set below or propose a new one in your PR.

Standard role emojis:
- 👔 Executive (VP Sales, General Counsel)
- 📄 Document-focused (Contract Manager)
- ⚖️ Legal-policy (Corporate Counsel)
- 🤝 Customer-facing closer (Account Executive)
- 🎯 Outbound (SDR / BDR)
- 🛠️ Operations (RevOps)
- 🧭 Coaching (Sales Manager)
- 👥 Customer Success (Account Manager / CSM)
- 💼 Generalist seller (Sales rep)
- 📈 Growth (Growth Marketer)
- 🎨 Brand / messaging (Product Marketer)
- 📣 Demand generation
- ✍️ Content
- 🔍 SEO
- 🚀 Marketing leadership
- 👤 Founder

## What NOT to include

Keep the public list simple to read and easy to maintain. The rules below are about avoiding noisy presentation, not blocking useful navigation or maintenance surfaces.

| Avoid | Use instead |
|---|---|
| 📊 Outcome stats line in the README or department hero ("47% faster X") | Put performance claims on product/catalog pages where they can be sourced and updated. |
| `## Common challenges` sections inside department files | Keep department files focused on task navigation and entries. Buyer education belongs in a separate guide or catalog page. |
| Unexplained `## Top picks` with ⭐ markers mixed into the main list | If editorial picks are needed, put them in a dated `picks.md` or website section with selection criteria. Do not mark arbitrary entries in department files. |
| `## Find by tool` / `## Find by type` / `## Find by publisher` blocks duplicated inside every department file | Use separate index files such as `INDEX.md`, `publishers.md`, or `by-tool.md` when those views are maintained. Keep each department page's TOC aligned with its body. |
| Plugin mention in hero blockquote | Plugins appear as entries or in a dedicated plugin/index file, not as promotional hero copy. |
| `**Bold name**` in entry lines | Canonical awesome-list style uses plain `[Name](url)`. |
| Multi-sentence rich descriptions | Use one factual sentence. Two sentences are acceptable only when the second removes ambiguity. |
| Per-task `> 👔 Role · When ...` blockquote header | Role mapping lives in `## Quick path by role` at the top. Keep task sections compact. |
| `Generated-on YYYY-MM-DD` footer | The list is hand-edited markdown. Use Git history or the README last-update badge for freshness. |
| `Also used by:` cross-reference sub-bullets under entries | Each entry lives under exactly one primary task. Use a maintained index file for cross-cutting discovery. |
| YAML registry or mandatory build pipeline for the GitHub list | Optional hygiene scripts and CI checks are fine; the source of truth remains hand-edited markdown. |
| Subfolders like `departments-en/legal/general-counsel.md` | One file per department. Roles surface via `## Quick path by role`. |

## Adding an entry to an existing task

1. Find the entry on [ElasticFlow Hub](https://elasticflow.app/hub/skills) — note its department, name, slug, command, source repo, primary role, platforms, and trust signals.
2. Open `departments-en/<dept>.md` and find the right task H2.
3. Add a bullet matching the [Entry-line format](#entry-line-format).
4. Sort alphabetically by entry name within the task.
5. Open a PR — the [PR template](.github/PULL_REQUEST_TEMPLATE.md) walks you through the checklist.

## Adding a new task to an existing department

1. Confirm the task name follows [Task naming rules](#task-naming-rules).
2. Add the H2 section in alphabetical order in the body.
3. Add the link to `## Contents`, also alphabetical.
4. Add the task to the relevant role(s) in `## Quick path by role`.
5. Open a PR.

If you'd like to discuss a new task name before drafting, open an Issue with the proposed name and 1-2 representative entries.

## Adding a new department

1. Confirm the department exists at `elasticflow.app/hub/skills/departments/<slug>`.
2. Create `departments-en/<slug>.md` from the [skeleton](#department-file-skeleton).
3. List the department's roles by browsing `elasticflow.app/hub/skills/roles/<slug>/` and add them to `## Quick path by role`. If no roles exist yet, skip that section and add a one-line note explaining the gap.
4. List all published skills for that department from the catalog page.
5. Cluster skills into 5–11 outcome-named tasks. Aim for 3–7 entries per task.
6. Place each entry under exactly one primary task.
7. Verify all anchors render in GitHub Preview.
8. Add the new department to `README.md#contents` (alphabetical).
9. Open a PR.

## Submitting changes

- One PR per logical change set.
- The [PR template](.github/PULL_REQUEST_TEMPLATE.md) walks you through the checklist.
- PR description should answer: which department, which task(s), which entries, and why.

## License

Entry data is MIT-licensed. Editorial content (descriptions, task framings) is CC-BY-SA. By contributing you agree that your changes carry these licenses.
