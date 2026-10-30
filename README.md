<!-- registry-sync: version=20.2.0; skills=2877; stars=48574; updated_at=2026-10-29T09:02:11+00:00 -->

# Agentic Awesome Skills — AI Skills & AAS Core with stars

> **Find reusable instructions for your project, inspect their complete files, and keep an exact skill set you can review and reuse.**

Agentic Awesome Skills is a library of 2,877+ installable `SKILL.md` playbooks for Claude Code, Codex, Cursor, Gemini CLI and other AI coding agents. AAS Core helps Codex or Claude search the complete local catalog, record the skills the agent chooses, and preview a plan you can inspect before changing a target. Core does not rank or recommend skills.

**Start here:** [Explore the skill catalog](https://aaskills.tech/core/) · [Codex setup](https://aaskills.tech/docs/codex-cli-skills/) · [Claude Code setup](https://aaskills.tech/docs/claude-code-skills/) · [Install skills directly](#installation)

**Current release: V20.2.0.** AAS Core supports local catalog inspection, agent-owned selection, stack validation, and plan preview. Apply and recovery remain experimental. [Read the AAS Core preview guide](https://github.com/sickn33/agentic-awesome-skills/blob/v20.2.0/docs/users/aas-core.md) for setup and exact trust boundaries.

This README tracks `main`. Features listed under [Unreleased](CHANGELOG.md#unreleased) require a later release; the versioned guide describes the published package.

This is an independent community project, not affiliated with or endorsed by Google. Google, Antigravity, Gemini, and related names describe compatibility and install targets. The GitHub repository is canonical; the [hosted catalog](https://aaskills.tech/) and browser-local Workbench are companion discovery and review surfaces.

[![GitHub stars](https://img.shields.io/badge/⭐%2049%2C000%2B%20Stars-gold?style=for-the-badge)](https://github.com/sickn33/agentic-awesome-skills/stargazers)
[![Follow @AASkills\_ on X](https://img.shields.io/badge/Follow-%40AASkills__-black?style=for-the-badge\&logo=x)](https://x.com/AASkills_)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Anthropic-purple)](https://claude.ai)
[![Cursor](https://img.shields.io/badge/Cursor-AI%20IDE-orange)](https://cursor.sh)
[![Codex CLI](https://img.shields.io/badge/Codex%20CLI-OpenAI-green)](https://github.com/openai/codex) ⭐ 131,634 | 🐛 25,609 | 🌐 Rust | 📅 2026-10-30
[![Autohand Code](https://img.shields.io/badge/Autohand%20Code-CLI-blue)](https://github.com/autohandai/code-cli) ⭐ 211 | 🐛 42 | 🌐 TypeScript | 📅 2026-10-29
[![Gemini CLI](https://img.shields.io/badge/Gemini%20CLI-Google-blue)](https://github.com/google-gemini/gemini-cli) ⭐ 108,626 | 🐛 772 | 🌐 TypeScript | 📅 2026-10-30
[![Latest Release](https://img.shields.io/github/v/release/sickn33/agentic-awesome-skills?display_name=tag\&style=for-the-badge)](https://github.com/sickn33/agentic-awesome-skills/releases/latest)
[![Direct skill distribution](https://img.shields.io/badge/Direct%20skills-npx%20agentic--awesome--skills-black?style=for-the-badge\&logo=npm)](#installation)
[![Kiro](https://img.shields.io/badge/Kiro-AWS-orange?style=for-the-badge)](https://kiro.dev)
[![Copilot](https://img.shields.io/badge/Copilot-GitHub-lightblue?style=for-the-badge)](https://github.com/features/copilot)
[![OpenCode](https://img.shields.io/badge/OpenCode-CLI-gray?style=for-the-badge)](https://github.com/opencode-ai/opencode) ⚠️ Archived
[![Antigravity](https://img.shields.io/badge/Antigravity-AI%20IDE-red?style=for-the-badge)](https://github.com/sickn33/agentic-awesome-skills)

## Table of Contents

* [Watch the Introduction](#watch-the-introduction)
* [Support the Project](#support-the-project)
* [AAS Core: Agent-First Preview](#aas-core-agent-first-preview)
* [Installation](#installation)
* [Choose Your Tool](#choose-your-tool)
* [Recommended Specialized Plugins](#recommended-specialized-plugins)
* [Bundles & Workflows](#bundles--workflows)
* [Browse 2,877+ Skills](#browse-2877-skills)
* [Troubleshooting](#troubleshooting)
* [Stable Skills Manifest v1](#stable-skills-manifest-v1)
* [Contributing](#contributing)
* [Community](#community)
* [Credits & Sources](#credits--sources)
* [Top Contributors](#top-contributors)
* [Repo Contributors](#repo-contributors)
* [Star History](#star-history)
* [License](#license)

## Watch the Introduction

A 40-second introduction to Agentic Awesome Skills. Press play to watch it here on GitHub.

<https://github.com/user-attachments/assets/02aa20ca-c3bb-4984-807e-7b06ef77e785>

If GitHub's player stalls, [watch the video on the AAS website](https://aaskills.tech/).

## Support the Project

Help keep the catalog open, maintained, and available to the builders who use it.

<a href="https://vercel.com/open-source-program"><img alt="Vercel OSS Program" src="https://vercel.com/oss/program-badge-2026.svg" /></a>

| Support AAS                                          | What it helps fund                             |
| ---------------------------------------------------- | ---------------------------------------------- |
| [♥ Sponsor AAS](https://github.com/sponsors/sickn33) | Ongoing maintenance, reviews, and release work |
| [Buy Me a Coffee](https://buymeacoffee.com/sickn33)  | Small, direct contributions from the community |

Every contribution helps us keep the skills curated, the tooling tested, and the catalog useful for the next project.

<a href="https://buymeacoffee.com/sickn33">
  <img src="assets/buy-me-a-coffee-banner.png" alt="Support Agentic Awesome Skills on Buy Me a Coffee" width="420" />
</a>

*Security tooling support: [Snyk](https://snyk.io/).*

*AI compute & model credits: [Atlas Cloud](https://atlascloud.ai/) (supporting media generation workflows via [`atlas-cloud-media`](skills/atlas-cloud-media/SKILL.md)).*

*This project is tested with BrowserStack.*

[![Powered by Atlas Cloud](https://www.atlascloud.ai/oss-program/powered-by-atlas-cloud.svg)](https://www.atlascloud.ai?ref=M9PEA3)

For a complete setup through your first skill selection and installation preview, follow [Codex setup](docs/users/codex-cli-skills.md) or [Claude Code setup](docs/users/claude-code-skills.md).

## AAS Core: Agent-First Preview

Codex or Claude inspects your project and chooses exact skills. Every current catalog skill is individually searchable, readable, and available for agent selection. The read-only `compose_stack` tool validates the chosen IDs and structure in memory; a client or the `aas` CLI can persist `aas-stack.json` and optional selection evidence. `aas stack validate` checks the manifest, while `aas stack plan` writes an immutable preview for your review. Manifests have a technical maximum of 128 skills; Core does not rank or recommend candidates or install skills in this supported preview path.

> \[!IMPORTANT]
> Structural and identity validity does not certify semantic fit, compatibility, setup correctness, operational safety, or safety to apply. Apply and recovery require experimental opt-in and remain outside the supported preview.

The [Workbench](https://aaskills.tech/workbench) reviews stack and plan artifacts in browser memory without accessing your filesystem. See the [Core guide](https://github.com/sickn33/agentic-awesome-skills/blob/v20.2.0/docs/users/aas-core.md) for tool contracts, capability coverage, and limits.

## Installation

### From selection to use

Start with AAS Core in Codex or Claude. Configure the local MCP using the [Codex](docs/users/codex-cli-skills.md) or [Claude](docs/users/claude-code-skills.md) guide. With the MCP available, ask the agent to inspect your project, compare relevant skills, and save the exact selection. Then validate its manifest and review the resulting plan before any installation. The first configuration command previews a change and returns an approval digest:

```bash
npm exec --yes --ignore-scripts --package=agentic-awesome-skills@20.2.0 -- aas mcp configure \
  --host codex \
  --scope user \
  --config /absolute/path/to/codex/config.toml \
  --cache-root /absolute/path/to/aas-cache
```

Use `--host claude` and its configuration path for Claude. The [Core setup guide](https://github.com/sickn33/agentic-awesome-skills/blob/v20.2.0/docs/users/aas-core.md#configure-the-local-mcp) explains approval, reconnection, validation, and planning. To hand the reviewed IDs to the direct installer, use `aas stack install-preview` as described in the [manifest handoff](docs/users/aas-core.md#use-the-reviewed-selection); that command only prepares a `--dry-run` preview and does not apply a Core plan.

### Install selected skills directly

If you already know the IDs, preview a focused install into your host's skill directory:

```bash
npm exec --yes --ignore-scripts --package=agentic-awesome-skills@20.2.0 -- \
  agentic-awesome-skills --release 20.2.0 --path .agents/skills \
  --skills brainstorming,systematic-debugging --dry-run
```

Review the preview, then repeat without `--dry-run` when ready. The direct installer does not consume or apply a Core plan. Antigravity's watched skill directory can overload its context, so its default target requires a selected set, a filter, or an explicit `--all` override. See the [installation guide](docs/users/getting-started.md) and [security guidance](docs/users/security-and-antivirus.md) for other targets, auditing, and failure modes.

## Choose Your Tool

Use the path for your agent. Core setup is available for Codex and Claude; the other rows show direct install targets or plugin options.

| Tool                    | Install                                                                                                                                     | First Use                                            |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| Claude Code             | [AAS Core local MCP preview](docs/users/claude-code-skills.md), direct install, or Claude plugin marketplace                                | Ask Claude to choose and compose an AAS stack        |
| Cursor                  | `npx agentic-awesome-skills --cursor`                                                                                                       | `@brainstorming help me plan a feature`              |
| Gemini CLI              | `npx agentic-awesome-skills --gemini`                                                                                                       | `Use brainstorming to plan a feature`                |
| Codex CLI               | [AAS Core local MCP preview](docs/users/codex-cli-skills.md) or `npx agentic-awesome-skills --codex`                                        | Ask Codex to choose and compose an AAS stack         |
| Autohand Code           | `npx agentic-awesome-skills --path ~/.autohand/skills` or `--path .autohand/skills`                                                         | `Use brainstorming to plan a feature`                |
| Antigravity IDE         | `npx agentic-awesome-skills --antigravity --skills <ids> --dry-run`                                                                         | Ask an MCP-enabled agent to choose exact IDs first   |
| Antigravity CLI (`agy`) | `npx agentic-awesome-skills --agy`                                                                                                          | `/brainstorming help me plan a feature`              |
| Kiro CLI                | `npx agentic-awesome-skills --kiro`                                                                                                         | `Use brainstorming to plan a feature`                |
| Kiro IDE                | `npx agentic-awesome-skills --path ~/.kiro/skills`                                                                                          | `Use @brainstorming to plan a feature`               |
| GitHub Copilot          | `gh skill install sickn33/agentic-awesome-skills skills/brainstorming/SKILL.md --agent github-copilot --scope user --pin v14.2.0` (preview) | `Ask Copilot to use brainstorming to plan a feature` |
| OpenCode                | `npx agentic-awesome-skills --path .agents/skills --category development,backend --risk safe,none`                                          | `opencode run @brainstorming help me plan a feature` |
| AdaL CLI                | `npx agentic-awesome-skills --path .adal/skills`                                                                                            | `Use brainstorming to plan a feature`                |
| Custom path             | `npx agentic-awesome-skills --path ./my-skills`                                                                                             | Depends on your tool                                 |

See the host guides, including [Claude Code](docs/users/claude-code-skills.md), [Cursor](docs/users/cursor-skills.md), [Codex](docs/users/codex-cli-skills.md), and [Gemini CLI](docs/users/gemini-cli-skills.md), for complete setup.

## Recommended Specialized Plugins

Choose a focused plugin for the domain you are working in. These packages are available for Claude Code and Codex; compatible bundles also have a standard Agent Plugins manifest. See the [plugin guide](docs/users/plugins.md) for installation and host support.

| Plugin                           | Skills | Best for                                                                      |
| -------------------------------- | -----: | ----------------------------------------------------------------------------- |
| AAS Web App Builder              |     10 | Frontend and full-stack developers shipping modern web apps.                  |
| AAS Product Design Studio        |     10 | Product UI, brand, portfolio, accessibility, and richer visual work.          |
| AAS Security Engineer            |     10 | Authorized security testing, audit, and hardening.                            |
| AAS Secure App Builder           |      9 | Developers who want security embedded while building features.                |
| AAS Documents & Presentations    |      9 | Office files, document conversion, decks, and slide workflows.                |
| AAS Data Analytics               |     10 | Product analytics, SQL, dashboards, and experiments.                          |
| AAS Agent & MCP Builder          |     10 | Agentic apps, MCP tools, RAG systems, and evaluation loops.                   |
| AAS QA & Test Automation         |     10 | Test suites, browser automation, and QA stabilization.                        |
| AAS DevOps & Cloud               |     10 | Infrastructure, deployments, and operational workflows.                       |
| AAS Accessibility & Inclusive UX |      8 | WCAG audits, automated scans, screen-reader checks, and accessible QA.        |
| AAS API Platform Builder         |     10 | API design, OpenAPI contracts, auth, security, load tests, and observability. |
| AAS SaaS Launch & Revenue        |     10 | SaaS MVPs, pricing, payments, analytics, lifecycle, referrals, and SEO.       |
| AAS AI Product & Evaluation Ops  |     10 | AI product metrics, evals, tracing, experiments, and model-quality loops.     |

Browse the [plugin roadmap](docs/users/specialized-plugin-roadmap.md), [live plugin catalog](https://aaskills.tech/plugins), or generated [`plugins/`](plugins/) tree for the full set.

## Bundles & Workflows

Bundles suggest related skills; workflows describe the order to use them. They are guidance for selecting and running skills, not additional packages to install.

* [Bundles](docs/users/bundles.md) group skills by role or goal, such as `Web Wizard`, `Security Engineer`, and `OSS Maintainer`.
* [Workflows](docs/users/workflows.md) give ordered playbooks for planning, shipping, testing, and auditing; [workflow metadata](data/workflows.json) is available for integrations.
* If too many installed skills overload Antigravity, follow the [selective activation guide](docs/users/agent-overload-recovery.md). For other hosts, preview a smaller exact install or use the installer's `--risk`, `--category`, and `--tags` filters.

## Browse 2,877+ Skills

Explore the complete library in the [hosted catalog](https://aaskills.tech/) or [`CATALOG.md`](CATALOG.md). The canonical playbooks live in [`skills/`](skills/); [`skills_index.json`](skills_index.json) provides machine-readable discovery. Use [Getting Started](docs/users/getting-started.md) and [Usage](docs/users/usage.md) for first steps, or the [Workbench](https://aaskills.tech/workbench) to inspect a saved Core stack and plan in your browser.

For narrower comparisons, see [Claude Code skills](docs/users/best-claude-code-skills-github.md), [Cursor skills](docs/users/best-cursor-skills-github.md), and the [library comparison](docs/users/agentic-awesome-skills-vs-awesome-claude-skills.md).

## Troubleshooting

* [Core setup and trust boundaries](https://github.com/sickn33/agentic-awesome-skills/blob/v20.2.0/docs/users/aas-core.md)
* [Installation and everyday use](docs/users/usage.md)
* [Windows context and truncation recovery](docs/users/windows-truncation-recovery.md)
* [Linux/macOS overload and selective activation](docs/users/agent-overload-recovery.md)
* [Plugin compatibility and installation](docs/users/plugins.md)
* [Security and antivirus alerts](docs/users/security-and-antivirus.md)

## Stable Skills Manifest v1

Host integrations that load individual `SKILL.md` files can use [`skills_index.json`](skills_index.json), the [v1 schema](schemas/skills-index.v1.schema.json), and the [compatibility mirror](data/skills_index.json). This direct-host discovery manifest is separate from `aas-stack.json` and the AAS Core catalog. Read the [discovery contract](docs/users/discovery-manifest.md) before integrating.

## Contributing

* Add new skills under `skills/<skill-name>/SKILL.md` and follow [`CONTRIBUTING.md`](CONTRIBUTING.md).
* Start from the [skill template](docs/contributors/skill-template.md) and run `npm run validate` before a PR.
* Keep source PRs free of generated registry artifacts. Skill content and risky guidance require manual logic and safety review alongside automated checks.

## Community

* [Discussions](https://github.com/sickn33/agentic-awesome-skills/discussions) for questions, ideas, and examples.
* [Issues](https://github.com/sickn33/agentic-awesome-skills/issues) for reproducible bugs and actionable improvements.
* [Follow @AASkills\_ on X](https://x.com/AASkills_) for project updates and examples, or [@sickn33](https://x.com/sickn33) for releases.
* [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) for community expectations; [`SECURITY.md`](SECURITY.md) for security reports.

## Credits & Sources

We stand on the shoulders of giants.

👉 **[View the Full Attribution Ledger](docs/sources/sources.md)**

Source credits stay here for attribution and auditability. Repository contributor credit lives separately in [Repo Contributors](#repo-contributors).

Key source families include:

* **Official AI platform and tool repositories**
* **Security, web, infrastructure, data, design, and automation communities**
* **Independent skill authors and open-source maintainers**

<details open>
<summary><strong>Official Sources</strong></summary>

### Official Sources

* **[anthropics/skills](https://github.com/anthropics/skills) ⭐ 184,878 | 🐛 1,449 | 🌐 Python | 📅 2026-10-28**: Official Anthropic skills repository - Document manipulation (DOCX, PDF, PPTX, XLSX), Brand Guidelines, Internal Communications.

* **[anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks) ⭐ 53,949 | 🐛 371 | 🌐 Jupyter Notebook | 📅 2026-10-29**: Official notebooks and recipes for building with Claude.

* **[vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) ⭐ 33,230 | 🐛 190 | 🌐 JavaScript | 📅 2026-10-28**: Vercel Labs official skills - React Best Practices, Web Design Guidelines.

* **[openai/skills](https://github.com/openai/skills) ⭐ 28,405 | 🐛 295 | 🌐 Python | 📅 2026-10-28**: OpenAI Codex skills catalog - Agent skills, Skill Creator, Concise Planning.

* **[Skyvern-AI/skyvern](https://github.com/Skyvern-AI/skyvern) ⭐ 23,309 | 🐛 289 | 🌐 Python | 📅 2026-10-30**: Official Skyvern browser automation skill — AI-powered browser control using Vision LLMs and computer vision for navigating sites, filling forms, and extracting structured data.

* **[huggingface/skills](https://github.com/huggingface/skills) ⭐ 11,237 | 🐛 69 | 🌐 Python | 📅 2026-10-29**: Official Hugging Face skills - Models, Spaces, datasets, inference, and broader Hugging Face ecosystem workflows.

* **[browser-act/skills](https://github.com/browser-act/skills) ⭐ 6,299 | 🐛 10 | 🌐 Python | 📅 2026-08-24**: Official BrowserAct skills - authenticated browser automation, JavaScript-rendered extraction, screenshots, parallel session isolation, verification handling, and human handoff (MIT).

* **[remotion-dev/skills](https://github.com/remotion-dev/skills) ⭐ 5,893 | 🐛 22 | 🌐 TypeScript | 📅 2026-10-26**: Official Remotion skills - Video creation in React with 28 modular rules.

* **[google-gemini/gemini-skills](https://github.com/google-gemini/gemini-skills) ⭐ 4,356 | 🐛 15 | 🌐 Python | 📅 2026-10-29**: Official Gemini skills - Gemini API, SDK and model interactions.

* **[nowork-studio/NotFair](https://github.com/nowork-studio/NotFair) ⭐ 4,081 | 🐛 6 | 🌐 Python | 📅 2026-10-30**: Official source for the `seo-drift` skill - dated SEO baselines and regression detection across rankings, indexation, metadata, directives, schema, and on-page elements (MIT).

* **[expo/skills](https://github.com/expo/skills) ⭐ 3,765 | 🐛 101 | 🌐 Shell | 📅 2026-10-29**: Official Expo skills - Expo project workflows and Expo Application Services guidance.

* **[browserbase/skills](https://github.com/browserbase/skills) ⭐ 3,746 | 🐛 60 | 🌐 JavaScript | 📅 2026-10-27**: Official Browserbase `competitor-analysis` skill - Browserbase Search API competitor discovery, research lanes, matrices, screenshots, and HTML reports (MIT).

* **[Forward-Future/loop-library](https://github.com/Forward-Future/loop-library) ⭐ 3,211 | 🐛 5 | 🌐 JavaScript | 📅 2026-09-11**: Official Loop Library skill - find, adapt, and design bounded AI-agent feedback loops with verification, stop rules, guardrails, and handoffs (MIT).

* **[microsoft/skills](https://github.com/microsoft/skills) ⭐ 3,157 | 🐛 79 | 🌐 TypeScript | 📅 2026-10-29**: Official Microsoft skills - Azure cloud services, Bot Framework, Cognitive Services, and enterprise development patterns across .NET, Python, TypeScript, Go, Rust, and Java.

* **[Simon-He95/markstream-vue](https://github.com/Simon-He95/markstream-vue) ⭐ 3,043 | 🐛 1 | 🌐 Vue | 📅 2026-10-27**: Official Markstream skill for installing streaming Markdown renderers across Vue, React, Svelte, Angular, Nuxt, Next.js, and Vue 2 applications (MIT).

* **[supabase/agent-skills](https://github.com/supabase/agent-skills) ⭐ 2,954 | 🐛 522 | 🌐 TypeScript | 📅 2026-10-02**: Supabase official skills - Postgres Best Practices.

* **[apify/agent-skills](https://github.com/apify/agent-skills) ⭐ 2,478 | 🐛 48 | 🌐 Python | 📅 2026-10-19**: Official Apify skills - Web scraping, data extraction and automation.

* **[MiniMax-AI/cli](https://github.com/MiniMax-AI/cli) ⭐ 2,211 | 🐛 50 | 🌐 TypeScript | 📅 2026-10-19**: Official MiniMax CLI - text, image, video, speech, music, vision, and web-search workflows for MiniMax models and APIs.

* **[vostride/agent-qa](https://github.com/vostride/agent-qa) ⭐ 910 | 🐛 6 | 🌐 TypeScript | 📅 2026-10-28**: Official Agent QA skills for authoring natural-language web and mobile tests, evidence-backed run triage, and scoped debug/fix workflows (FSL-1.1-ALv2, Apache-2.0 after two years).

* **[dair-ai/dair-academy-plugins](https://github.com/dair-ai/dair-academy-plugins) ⭐ 618 | 🐛 0 | 🌐 HTML | 📅 2026-07-21**: Official DAIR Academy plugin skills imported as standalone skills - image generation, adaptive learning, lesson artifacts, LLM council deliberation, survey papers, wiki building, and YouTube study notes (MIT).

* **[testdriverai/testdriverai](https://github.com/testdriverai/testdriverai) ⭐ 463 | 🐛 46 | 🌐 JavaScript | 📅 2026-09-21**: Official TestDriver source for the `testdriver-e2e-testing` skill - author, run, and debug end-to-end tests that drive browsers and native apps in a real desktop sandbox with AI vision and natural-language element descriptions (Apache-2.0).

* **[CosmoBlk/email-marketing-bible](https://github.com/CosmoBlk/email-marketing-bible) ⭐ 358 | 🐛 1 | 📅 2026-10-13**: Official Email Marketing Bible source for the `email-marketing-bible` skill - data-backed email marketing for agents: automation flows, deliverability triage, copy de-slopping, AI email design, compliance and 19 industry playbooks, with ESP control via MCP behind explicit send-approval gates (MIT).

* **[Orkas-AI/Orkas-VideoStudio](https://github.com/Orkas-AI/Orkas-VideoStudio) ⭐ 332 | 🐛 1 | 🌐 TypeScript | 📅 2026-10-27**: Official source for the `video-router` skill - choose and lock generation, deterministic composition, supplied-footage editing, or an automatic cross-modal production plan (MIT).

* **[Xquik-dev/x-twitter-scraper](https://github.com/Xquik-dev/x-twitter-scraper) ⭐ 225 | 🐛 2 | 🌐 TypeScript | 📅 2026-10-30**: Official Xquik skill for X data workflows - tweet search, user lookup, follower export, media downloads, MCP, webhooks, OpenAPI, and SDK setup (MIT).

* **[sandbaseai/cli](https://github.com/sandbaseai/cli) ⭐ 185 | 🐛 2 | 🌐 TypeScript | 📅 2026-10-24**: Official source for the `sandbase-mcp` skill - discover, inspect, and invoke 2,000+ AI models and APIs through a local MCP bridge with explicit schema and cost checks (Apache-2.0).

* **[pilot-protocol/pilotprotocol](https://github.com/pilot-protocol/pilotprotocol) ⭐ 147 | 🐛 10 | 🌐 Go | 📅 2026-10-14**: Official Pilot Protocol overlay network - agent addressing, encrypted P2P messaging, NAT traversal, and an installable agent app store (AGPL-3.0).

* **[hermes-labs-ai/lintlang](https://github.com/hermes-labs-ai/lintlang) ⭐ 144 | 🐛 10 | 🌐 Python | 📅 2026-10-26**: Official source for the `lintlang-audit` skill - deterministic, zero-LLM static auditing of agent instructions, tool definitions, and embedded Python prompts, reporting finding codes and locations without editing files or calling a model (Apache-2.0).

* **[NygenAnalytics/scarf](https://github.com/NygenAnalytics/scarf) ⭐ 125 | 🐛 0 | 🌐 Python | 📅 2026-10-21**: Official Scarf source for the `scarf-single-cell` skill - out-of-core single-cell RNA-seq analysis with Scarf's Zarr DataStore on local disk or object storage, immutable provenance-tracked artifacts, audited QC, clustering, markers and comparisons (BSD-3-Clause).

* **[voygr-tech/placecall](https://github.com/voygr-tech/placecall) ⭐ 109 | 🐛 6 | 🌐 Shell | 📅 2026-10-29**: Official PlaceCall source for the `placecall` skill - place real outbound phone calls to US businesses through the PlaceCall REST API (reservations, inquiries, quotes), follow the call and return the structured outcome and transcript; paid API, real calls ring real phones (MIT).

* **[neondatabase/agent-skills](https://github.com/neondatabase/agent-skills) ⭐ 108 | 🐛 33 | 🌐 JavaScript | 📅 2026-10-29**: Official Neon skills - Serverless Postgres workflows and Neon platform guidance.

* **[Krexa-xyz/skills](https://github.com/Krexa-xyz/skills/tree/main/skills/krexa) ⭐ 105 | 🐛 0 | 📅 2026-10-21**: MIT-0 official source for the `krexa` skill - turn a trading idea, post or video into fixed rules, backtest and paper-trade them, and request a user-approved live trading agent through Krexa's hosted MCP server.

* **[weaviate/agent-skills](https://github.com/weaviate/agent-skills) ⭐ 104 | 🐛 1 | 🌐 Python | 📅 2026-10-20**: Official Weaviate skills - vector database operations, semantic and hybrid search, data imports, RAG cookbooks, agentic RAG, multimodal PDF search, and async client patterns (BSD-3-Clause).

* **[arcmira/mcp](https://github.com/arcmira/mcp/tree/v0.10.6/plugins/arcmira) ⭐ 78 | 🐛 8 | 🌐 TypeScript | 📅 2026-10-23**: Apache-2.0 plugin source for `arcmira-find-quotes`, YouTube and podcast quote research with timestamped sources. The hosted service and server have separate licensing.

* **[prisma/skills](https://github.com/prisma/skills) ⭐ 77 | 🐛 4 | 📅 2026-10-29**: Official Prisma skills - Prisma Postgres setup, Prisma ORM, Prisma Compute deploys, and Client/CLI workflows.

* **[uizze/uizze](https://github.com/uizze/uizze) ⭐ 76 | 🐛 7 | 🌐 JavaScript | 📅 2026-10-24**: Official UIZZE source for the free `anti-ui-slop` skill—product-specific UI references, design contracts, required states, and a hard finish gate grounded in 800,000+ real web and iOS screens (MIT).

* **[longbridge/skills](https://github.com/longbridge/skills) ⭐ 67 | 🐛 3 | 🌐 Python | 📅 2026-10-26**: Official Longbridge Securities skills - real-time quotes, charts, fundamentals, portfolio analysis, options, and market workflows for HK, US, A-share, and SG markets.

* **[vanshyadav1408/Omentir](https://github.com/vanshyadav1408/Omentir) ⭐ 52 | 🐛 2 | 🌐 TypeScript | 📅 2026-10-30**: Official Omentir source for the [`omentir-linkedin-outreach`](skills/omentir-linkedin-outreach/SKILL.md) skill - LinkedIn prospecting and outreach through the hosted Omentir MCP server (OAuth): find and score leads, draft messages, and check campaigns, research and drafts only by default, never signs into LinkedIn (MIT).

* **[sendblue-api/sendblue-cli](https://github.com/sendblue-api/sendblue-cli) ⭐ 30 | 🐛 4 | 🌐 TypeScript | 📅 2026-09-01**: Source for `sendblue/sendblue-cli`.

* **[metalbear-co/skills](https://github.com/metalbear-co/skills) ⭐ 29 | 🐛 5 | 🌐 Python | 📅 2026-10-27**: Official mirrord skills source for the `mirrord` skill - run a local process inside a live Kubernetes pod's network, env and traffic, with confirmation before traffic-stealing or cluster-modifying steps (MIT).

* **[wassim-azi/agy-powerline](https://github.com/wassim-azi/agy-powerline) ⭐ 28 | 🐛 12 | 🌐 JavaScript | 📅 2026-10-29**: Source for `agy-powerline`.

* **[uiverify/uiverify](https://github.com/uiverify/uiverify) ⭐ 25 | 🐛 1 | 🌐 TypeScript | 📅 2026-10-28**: Source for `uiverify-triage-visual-changes`.

* **[BuyWhere/buywhere-mcp](https://github.com/BuyWhere/buywhere-mcp) ⭐ 15 | 🐛 22 | 🌐 TypeScript | 📅 2026-10-26**: Official BuyWhere MCP server — search and compare products from Singapore, SEA, and US markets via Model Context Protocol.

* **[scopeblind/scopeblind-gateway](https://github.com/scopeblind/scopeblind-gateway) ⭐ 10 | 🐛 5 | 🌐 TypeScript | 📅 2026-10-26**: Official Scopeblind MCP governance toolkit - Cedar policy authoring, shadow-to-enforce rollout, and signed-receipt verification guidance for agent tool calls.

* **[happy520ai/unified-ai-system](https://github.com/happy520ai/unified-ai-system) ⭐ 10 | 🐛 40 | 🌐 JavaScript | 📅 2026-10-29**: Official source for the `unified-ai-gateway` skill - governed Codex MCP tools for provider-free prompt enhancement, credential-free gateway health, readiness, fake-provider chat, knowledge, workflow, and workforce evidence (Apache-2.0).

* **[MohammadHijjawi97/since-cutoff](https://github.com/MohammadHijjawi97/since-cutoff) ⭐ 10 | 🐛 64 | 🌐 Python | 📅 2026-10-25**: Official source for the `since-cutoff` skill - lists which APIs of a project's pinned Python dependencies changed after the model's training cutoff, from a static diff of the two releases with no model calls, shows where the code uses them, and writes short AGENTS.md or CLAUDE.md notes (MIT).

* **[beatra-ai/photo-to-anime-skill](https://github.com/beatra-ai/photo-to-anime-skill) ⭐ 8 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ai-photo-restyler` skill - paid, hosted work installed from a digest-pinned 0.1.4 archive byte-identical to commit `87bc4c4` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-logo-maker-skill](https://github.com/beatra-ai/ai-logo-maker-skill) ⭐ 8 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ai-logo-maker` skill - paid, hosted work installed from a digest-pinned 0.1.7 archive byte-identical to commit `89bf762` with self-update disabled before first use (MIT-0).

* **[Aident-AI/aident-skill](https://github.com/Aident-AI/aident-skill/tree/main/aident-loadout/skills/aident-loadout) ⭐ 7 | 🐛 0 | 🌐 Shell | 📅 2026-10-12**: MIT official source for the `aident-loadout` skill - search actions across apps the user connected in [Aident Loadout](https://aident.ai), read live schemas, check connections and cost before running, and require approval for side effects, through the hosted Aident MCP server.

* **[uxkin/agent](https://github.com/uxkin/agent) ⭐ 7 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-29**: Official UXKIN source for the free [`uxkin-research`](skills/uxkin-research/SKILL.md) skill — research real iOS app screens, user journeys and website design systems before designing UI (MIT).

* **[beatra-ai/ai-voiceover-generator-skill](https://github.com/beatra-ai/ai-voiceover-generator-skill) ⭐ 7 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `voiceover-narration-studio` skill - paid, hosted work installed from a digest-pinned 0.1.9 archive byte-identical to commit `0c44adf` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-product-photography-skill](https://github.com/beatra-ai/ai-product-photography-skill) ⭐ 7 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `product-photo-studio` skill - paid, hosted work installed from a digest-pinned 0.2.0 archive byte-identical to commit `1490364` with self-update disabled before first use (MIT-0).

* **[HasData/hasdata-cli](https://github.com/HasData/hasdata-cli) ⭐ 7 | 🐛 0 | 🌐 Go | 📅 2026-10-26**: Official HasData CLI and API guidance for search, scraping, ecommerce, travel, jobs, local business, and structured web data workflows.

* **[beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills) ⭐ 7 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `beatra-ai-video-studio` skill - paid, hosted AI video generation, editing, and extension, installed from a digest-pinned 1.2.5 archive byte-identical to commit `95d662f` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-podcast-voiceover-skill](https://github.com/beatra-ai/ai-podcast-voiceover-skill) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ai-podcast-voiceover` skill - paid, hosted work installed from a digest-pinned 0.1.7 archive byte-identical to commit `ddca11e` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-poster-maker-skill](https://github.com/beatra-ai/ai-poster-maker-skill) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `poster-design-studio` skill - paid, hosted work installed from a digest-pinned 0.1.3 archive byte-identical to commit `7a6337f` with self-update disabled before first use (MIT-0).

* **[pixeltable/pixeltable-skill](https://github.com/pixeltable/pixeltable-skill) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-10-29**: Source for `pixeltable`.

* **[beatra-ai/viral-video-remake-skill](https://github.com/beatra-ai/viral-video-remake-skill) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `viral-video-teardown-remake` skill - paid, hosted work installed from a digest-pinned 0.3.1 archive byte-identical to commit `46f7875` with self-update disabled before first use (MIT-0).

* **[beatra-ai/multilingual-voiceover-skill](https://github.com/beatra-ai/multilingual-voiceover-skill) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ai-multilingual-dubbing` skill - paid, hosted work installed from a digest-pinned 0.1.9 archive byte-identical to commit `030ec84` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-music-generator-skill](https://github.com/beatra-ai/ai-music-generator-skill) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `music-generation-studio` skill - paid, hosted work installed from a digest-pinned 0.1.8 archive byte-identical to commit `fee8fbf` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-media-generator-skill](https://github.com/beatra-ai/ai-media-generator-skill) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `beatra` skill - paid, hosted work installed from a digest-pinned 2.8.8 archive byte-identical to commit `69afbfe` with self-update disabled before first use (MIT-0).

* **[beatra-ai/talking-avatar-video-skill](https://github.com/beatra-ai/talking-avatar-video-skill) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `talking-avatar-video` skill - paid, hosted work installed from a digest-pinned 0.2.1 archive byte-identical to commit `251c968` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-storyboard-generator-skill](https://github.com/beatra-ai/ai-storyboard-generator-skill) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `ai-storyboard-generator`.

* **[AltoRank/altorank](https://github.com/AltoRank/altorank) ⭐ 4 | 🐛 13 | 🌐 TypeScript | 📅 2026-10-29**: AGPL-3.0 official source for the `altorank` skill - SEO/AI-search readiness audits, Search Console reads, keyword research and draft creation into a person-reviewed queue through the hosted AltoRank MCP server.

* **[beatra-ai/ai-headshot-generator-skill](https://github.com/beatra-ai/ai-headshot-generator-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ai-headshot-studio` skill - paid, hosted work installed from a digest-pinned 0.1.7 archive byte-identical to commit `a8818c3` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-voice-cloning-skill](https://github.com/beatra-ai/ai-voice-cloning-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `voice-cloning-studio` skill - paid, hosted work installed from a digest-pinned 0.2.1 archive byte-identical to commit `64923d9` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ai-image-generator-skill](https://github.com/beatra-ai/ai-image-generator-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ai-image-generation-studio` skill - paid, hosted work installed from a digest-pinned 0.1.4 archive byte-identical to commit `13c7b9b` with self-update disabled before first use (MIT-0).

* **[beatra-ai/ecommerce-product-images-skill](https://github.com/beatra-ai/ecommerce-product-images-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `ecommerce-listing-image-set` skill - paid, hosted work installed from a digest-pinned 0.2.0 archive byte-identical to commit `ef9056d` with self-update disabled before first use (MIT-0).

* **[beatra-ai/lyrics-to-song-skill](https://github.com/beatra-ai/lyrics-to-song-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Beatra source for the `suno-lyrics-to-song` skill - paid, hosted work installed from a digest-pinned 0.2.0 archive byte-identical to commit `2facaac` with self-update disabled before first use (MIT-0).

* **[ASI2030/Fact-Check-X](https://github.com/ASI2030/Fact-Check-X) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-19**: Source for the `fact-check-x-complete` workflow - claim-level AI answer comparison, citation-fidelity review, and public primary-source verification without bundled browser automation (Apache-2.0).

* **[beatra-ai/ai-audiobook-generator-skill](https://github.com/beatra-ai/ai-audiobook-generator-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `ai-audiobook-narration`.

* **[beatra-ai/ai-image-realism-skill](https://github.com/beatra-ai/ai-image-realism-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `ai-image-realism`.

* **[beatra-ai/wechat-article-cover-skill](https://github.com/beatra-ai/wechat-article-cover-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `wechat-cover-maker`.

* **[beatra-ai/xiaohongshu-copywriter-skill](https://github.com/beatra-ai/xiaohongshu-copywriter-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `zhongcao-note-copywriter`.

* **[beatra-ai/xiaohongshu-cover-maker-skill](https://github.com/beatra-ai/xiaohongshu-cover-maker-skill) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `zhongcao-cover-maker`.

* **[agent-frontier/wgm](https://github.com/agent-frontier/wgm) ⭐ 3 | 🐛 2 | 🌐 Shell | 📅 2026-10-30**: Official wgm protocol skill - governed build loops with triage, alignment, planning, deterministic backpressure, holdout-scenario judging, and handoff audits (MIT).

* **[replynodes/replynodes-agent-skills](https://github.com/replynodes/replynodes-agent-skills) ⭐ 3 | 🐛 15 | 🌐 Python | 📅 2026-10-10**: Official ReplyNodes source for the `url-to-markdown` skill - fetch a public webpage as clean Markdown for reading, summarizing, quoting, or citing while preserving the source URL (MIT).

* **[target1m/traderspy-mcp](https://github.com/target1m/traderspy-mcp) ⭐ 3 | 🐛 1 | 🌐 JavaScript | 📅 2026-10-13**: Official TraderSpy source for six crypto market research skills (`traderspy-*`) - market briefings, technical analysis, screening and backtests, AI signals, top-trader positioning, and position checks through the hosted, read-only TraderSpy MCP server (MIT).

* **[qrxcodes/qrx-mcp](https://github.com/qrxcodes/qrx-mcp) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-10-13**: Official QRX skill - turn a text prompt and a link into an artistic, branded QR code through the hosted QRX MCP server, checked to scan before it is returned (MIT).

* **[a4a-network/a4a](https://github.com/a4a-network/a4a) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for `a4a`.

* **[datawebot/datawebot-mcp](https://github.com/datawebot/datawebot-mcp) ⭐ 3 | 🐛 2 | 📅 2026-10-28**: Source for `datawebot`.

* **[pangolin-spg/openclaw-skills](https://github.com/pangolin-spg/openclaw-skills) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2026-10-30**: Source for `pangolinfo-amazon-data-research`.

* **[lognorm/lognorm-mcp](https://github.com/lognorm/lognorm-mcp) ⭐ 2 | 🐛 0 | 📅 2026-10-02**: MIT official source for the `lognorm` skill — work a site's SEO and AI-visibility (GEO) backlog through the hosted LogNorm MCP server: audits, fixes, content and AI-answer tracking.

* **[gongdear/cline-pilot](https://github.com/gongdear/cline-pilot) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-10-05**: Official source for the `cline-pilot` skill - proxy-drive Cline CLI coding tasks serially, monitor long runs against git/test evidence instead of self-report, relay decision points, and learn per-project-tag preferences in git-ignored private state (MIT).

* **[busabase/skills](https://github.com/busabase/skills) ⭐ 2 | 🐛 0 | 🌐 TypeScript | 📅 2026-10-26**: MIT source for the `busabase` skill — authorized MCP workspace operations, permission-aware ChangeRequests, and canonical-versus-pending readback.

* **[jcaiagent7143-ui/linkdigest-mcp](https://github.com/jcaiagent7143-ui/linkdigest-mcp) ⭐ 2 | 🐛 1 | 🌐 Python | 📅 2026-10-29**: Official LinkDigest source for the `linkdigest-social-link-reader` skill - read one public Xiaohongshu, Douyin, TikTok, YouTube, X or WeChat article link into text (transcript, image text, key points with checked quotes, coverage receipt) through the paid hosted LinkDigest API or MCP server with the user's own key (MIT).

* **[bekservice/Famulor-Skill](https://github.com/bekservice/Famulor-Skill) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-10-29**: Official Famulor skill for tenant-safe operation of its hosted MCP server across assistants, communication history, campaigns, knowledge, automations, telephony, and workspace administration (MIT).

* **[runapi-ai/cli-skill](https://github.com/runapi-ai/cli-skill) ⭐ 2 | 🐛 0 | 📅 2026-09-28**: Official RunAPI CLI skill - generate AI images, videos, and music/audio from agent workflows, plus run other model API jobs.

* **[masakaai/jet-browser](https://github.com/masakaai/jet-browser) ⭐ 2 | 🐛 1 | 🌐 JavaScript | 📅 2026-10-12**: Official Jet Browser skill and Apache-2.0 source - isolated WPE WebKit sessions with ordered JSONL, native input, semantic DOM inspection, screenshots, and reproducible offline runtime checks.

* **[f-o-x11/deed-page-skill](https://github.com/f-o-x11/deed-page-skill) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-29**: Source for `deed-page`.

* **[webly-ai/webly-plugin](https://github.com/webly-ai/webly-plugin) ⭐ 2 | 🐛 2 | 🌐 JavaScript | 📅 2026-10-28**: Source for `webly`.

* **[tuantqse90/moltnode-mcp](https://github.com/tuantqse90/moltnode-mcp/tree/main/skills/moltnode) ⭐ 1 | 🐛 2 | 🌐 Python | 📅 2026-10-29**: MIT official source for the `moltnode-chain-reader` skill - keyless JSON-RPC reads on 31 blockchains through MoltNode by Chord, plus Chord swap quotes with an unsigned transaction and simulation. The hosted gateway and server have separate licensing.

* **[Pazificateur69/tokenleak](https://github.com/Pazificateur69/tokenleak) ⭐ 1 | 🐛 1 | 🌐 Python | 📅 2026-10-13**: Official tokenleak source for the [`tokenleak`](skills/tokenleak/SKILL.md) skill - token-lean working rules that cut the context a coding agent re-sends on every call (big reads, noisy logs, re-reads, serial calls), with a published A/B benchmark (MIT).

* **[anup-a/agent-artifacts](https://github.com/anup-a/agent-artifacts) ⭐ 1 | 🐛 0 | 🌐 HTML | 📅 2026-10-25**: Official byagent source for the `byagent` skill - publish agent-written Markdown or HTML as a shareable link with the `byagent` CLI, read readers' line comments back, edit, republish to the same link and resolve; pages are public unless `--private` and comment text is treated as untrusted data (MIT).

* **[cloudishai/skills](https://github.com/cloudishai/skills) ⭐ 1 | 🐛 0 | 📅 2026-10-28**: Official Cloudish source for the `cloudish` skill - deploy a Dockerfile, source folder, or existing image as a running container at a live URL, built server-side, with confirmation before the first deploy and before spending credits; uploads the build context and spends prepaid credits (MIT).

* **[makeev/alphai-claude-skills](https://github.com/makeev/alphai-claude-skills) ⭐ 1 | 🐛 0 | 📅 2026-10-09**: Official AlphAI skills - stock briefs, market pulse, SEC Form 4 insider scans, two-ticker read-across, and news alerts through the hosted AlphAI MCP server (relevance-scored financial news, filing-verified earnings reads) (MIT).

* **[Modellix/modellix-plugin](https://github.com/Modellix/modellix-plugin) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Official Modellix skill - authenticated, paid AI image and video generation through the Modellix CLI (MIT).

* **[fclairamb/solidping-plugin](https://github.com/fclairamb/solidping-plugin/tree/main/skills/solidping-monitoring) ⭐ 0 | 🐛 2 | 📅 2026-10-29**: MIT official source for the `solidping` skill - uptime checks across 40+ types, results, incidents, diagnosis and status pages through the hosted SolidPing MCP server, with every write confirmed by the person first. SolidPing itself is AGPL-3.0.

* **[Outreachgenie/outreachgenie-linkedin-mcp](https://github.com/Outreachgenie/outreachgenie-linkedin-mcp) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: MIT source for `outreachgenie-list-audit`, a read-only saved-list and template audit with local Python reports. Connected use requires an OutreachGenie workspace and compatible MCP host.

* **[getchordlabs/chord](https://github.com/getchordlabs/chord/tree/main/skills/chord) ⭐ 0 | 🐛 1 | 🌐 Solidity | 📅 2026-10-29**: MIT official source for the `chord-onchain-trading` skill - DEX market data, best-route swap quotes and unsigned swap transactions on eight EVM chains through the Chord API; the skill never signs or sends. The hosted API and server have separate licensing.

* **[loootai/looot-skills](https://github.com/loootai/looot-skills) ⭐ 0 | 🐛 0 | 🌐 Shell | 📅 2026-10-12**: Official looot skills - search, price and run 2,500+ data API endpoints (work emails, company search, SERP, web pages) from one prepaid balance.

* **[prateeks367/voicemoat-skills](https://github.com/prateeks367/voicemoat-skills) ⭐ 0 | 🐛 0 | 📅 2026-10-04**: Official VoiceMoat source for eight Twitter/X and LinkedIn skills (`write-in-my-voice`, `turn-this-into-a-thread`, `same-idea-both-platforms`, `repurpose-into-a-post`, `define-my-content-pillars`, `why-did-this-post-flop`, `get-seen-in-replies`, `draft-my-comments`). They draft in your own voice, write threads, cross-post, repurpose long content, pick content pillars, diagnose a post that underperformed, and write replies and comments worth reading; each works from pasted text alone, and an optional paid VoiceMoat connector adds voice scoring and preview-gated publishing (MIT).

* **[bosmdavid-gif/dropthehassle-skill](https://github.com/bosmdavid-gif/dropthehassle-skill) ⭐ 0 | 🐛 1 | 🌐 JavaScript | 📅 2026-10-20**: Official DropTheHassle source for the `dropthehassle-publish` skill - check that a folder is a finished static build, publish it to a free HTTPS link, hand the human the claim link and verify it is live; the agent never pays (MIT).

* **[Instant-Expert/skills](https://github.com/Instant-Expert/skills) ⭐ 0 | 🐛 0 | 🌐 Shell | 📅 2026-10-10**: Official Instant Expert source for the `ask-human-expert` skill - ask real executives, operators and domain experts a question for a written or voice answer or a short call, with a free test mode and the user's approval before every paid order (MIT-0).

* **[cohesivity-org/cohesivity-skill](https://github.com/cohesivity-org/cohesivity-skill) ⭐ 0 | 🐛 0 | 📅 2026-10-16**: Official Cohesivity skill - agent provisioned backend infrastructure covering Postgres, hosting, auth, realtime, storage, cron, email, and AI model APIs over one HTTP API (MIT).

* **[opencanviz/opencanviz-skills-repo](https://github.com/opencanviz/opencanviz-skills-repo) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-29**: Official openCanviz source for the `opencanviz-json` skill - write an openCanviz video project as JSON with a standard-library Python builder and validator (text entrances, 22 scene transitions, motion presets, LaTeX math, plots, tables, rings, 22 example projects), then import it at opencanviz.com/create, where a free account builds and plays it as a narrated, animated explainer and the MP4 download needs a plan or a one-time export purchase (MIT).

* **[ces107/agent-forge](https://github.com/ces107/agent-forge) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-23**: Source for `launch-check`.

* **[commentkeyword/agent-toolkit](https://github.com/commentkeyword/agent-toolkit) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-27**: Source for `comment-to-dm-cta`.

* **[cooper-email/cooper-email](https://github.com/cooper-email/cooper-email) ⭐ 0 | 🐛 8 | 🌐 TypeScript | 📅 2026-10-24**: Source for `cooper-email`.

* **[f-o-x11/perq-skill](https://github.com/f-o-x11/perq-skill) ⭐ 0 | 🐛 1 | 📅 2026-10-26**: Source for `perq`.

* **[faberlang/faber](https://github.com/faberlang/faber) ⭐ 0 | 🐛 0 | 🌐 Rust | 📅 2026-10-29**: Source for `faber-language`.

* **[kasovy/neverapply-mcp](https://github.com/kasovy/neverapply-mcp) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-25**: Source for `neverapply`.

* **[robinfaraj/postel-mcp](https://github.com/robinfaraj/postel-mcp) ⭐ 0 | 🐛 0 | 📅 2026-10-29**: Source for `postel-writing`.

* **[soundza/soundza-mcp](https://github.com/soundza/soundza-mcp) ⭐ 0 | 🐛 0 | 📅 2026-10-23**: Source for `soundza`.

* **[target1m/footval-mcp](https://github.com/target1m/footval-mcp) ⭐ 0 | 🐛 0 | 📅 2026-10-22**: Source for `footval-follow-matches-and-tables`, `footval-scout-and-rank-players`, `footval-stats-and-transfer-news`, `footval-value-and-compare-players`.

* **[SergiuPogor/curlshot-mcp](https://github.com/SergiuPogor/curlshot-mcp/tree/main/skills/curlshot)**: MIT official source for the `curlshot` skill - web page screenshots, PDFs and scrolling videos, plus HTML/Markdown rendering, through the hosted CurlShot API or MCP server. The hosted service has separate terms.

* **[Spicy-API/nsfw-ai-skill](https://github.com/Spicy-API/nsfw-ai-skill)**: Official SpicyAPI source for the [`nsfw-ai-spicyapi`](skills/nsfw-ai-spicyapi/SKILL.md) skill — adult (18+) image, image-to-video and image-edit generation through the SpicyAPI API with quote-before-spend and adults-only / consent rules (MIT).

* **[Atlas Cloud](https://atlascloud.ai/)**: Official source for the [`atlas-cloud-media`](skills/atlas-cloud-media/SKILL.md) skill — asynchronous image and video generation through the Atlas Cloud API.

* **[HEOJUNFO/ai-film-crew](https://github.com/HEOJUNFO/ai-film-crew)**: Official source for the `film-crew` skill - run a video idea past seven film-crew roles and get a shot list with one model-ready prompt per shot, plus prompt fixes and reroll diagnosis for Wan, LTX, Kling, Veo, Seedance, Hailuo, and Runway (MIT).

* **[doomsday-network/doom-pay](https://github.com/doomsday-network/doom-pay)**: Source for `doom-pay`.

* **[doomsday-network/doomsday](https://github.com/doomsday-network/doomsday)**: Source for `doomsday-escrow`.

</details>

<details>
<summary><strong>Community Contributors & Source Repositories</strong></summary>

### Community Contributors

* **[morluto/rea](https://github.com/morluto/rea) ⭐ 409,379 | 🐛 1,324 | 🌐 TypeScript | 📅 2026-10-30**: MIT source for the `reverse-engineer-anything` skill - evidence-led native, managed, JavaScript/Electron, packaged, and browser investigations with explicit provider limits.

* **[obra/superpowers](https://github.com/obra/superpowers) ⭐ 308,915 | 🐛 373 | 🌐 Shell | 📅 2026-10-29**: The original "Superpowers" by Jesse Vincent.

* **[mattpocock/skills](https://github.com/mattpocock/skills) ⭐ 306,853 | 🐛 208 | 🌐 Shell | 📅 2026-10-29**: Source for 17 Matt Pocock workflow skills - codebase design, TDD, bug diagnosis, triage, PRDs, issues, prototyping, handoff, teaching, and skill-writing guidance (MIT).

* **[affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) ⭐ 292,914 | 🐛 174 | 🌐 JavaScript | 📅 2026-10-30**: Large Claude Code configuration and workflow collection from an Anthropic hackathon winner (MIT).

* **[multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) ⭐ 226,575 | 🐛 138 | 📅 2026-04-20**: Source for the `andrej-karpathy` skill - English Karpathy-inspired LLM coding guidelines for simplicity, surgical changes, assumption surfacing, and verifiable success criteria (MIT).

* **[addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) ⭐ 111,815 | 🐛 145 | 🌐 JavaScript | 📅 2026-10-29**: Source for `constraint-driven-development`, `interview-me`, `using-agent-skills` — only names not already in the catalog (22/25 overlap with existing entries) (MIT).

* **[addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) ⭐ 111,815 | 🐛 145 | 🌐 JavaScript | 📅 2026-10-29**: Source for the `browser-testing-with-devtools` skill - Chrome DevTools MCP browser verification, profiling, network inspection, and frontend debugging guidance (MIT).

* **[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) ⭐ 105,808 | 🐛 7 | 🌐 JavaScript | 📅 2026-10-30**: Frontend design taste skill collection covering premium UI generation, redesign audits, GSAP motion, Stitch design systems, minimalist and brutalist visual modes, and full-output enforcement.

* **[unslothai/unsloth](https://github.com/unslothai/unsloth) ⭐ 78,780 | 🐛 447 | 🌐 Python | 📅 2026-10-30**: Source for the `unsloth-finetuning` skill - single-GPU VRAM sizing, LoRA/QLoRA configuration, chat-template and loss-masking correctness, GRPO/DPO post-training, and GGUF/merged export paths (Apache-2.0).

* **[career-ops-hq/career-ops](https://github.com/career-ops-hq/career-ops) ⭐ 78,761 | 🐛 537 | 🌐 JavaScript | 📅 2026-10-30**: Source for the `career-ops` skill — multi-CLI job-search command center (MIT, docs-only — Node runtime not bundled).

* **[ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) ⭐ 59,428 | 🐛 82 | 🌐 Python | 📅 2026-10-19**: Source for the `i-have-adhd` skill — ADHD-friendly output shaping (MIT).

* **[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) ⭐ 57,383 | 🐛 66 | 🌐 JavaScript | 📅 2026-10-29**: Marketing skills for CRO, copywriting, SEO, paid ads, and growth (23 skills, MIT).

* **[K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) ⭐ 55,324 | 🐛 74 | 🌐 Python | 📅 2026-10-26**: Scientific, research, engineering, finance, and writing skill suite (MIT).

* [cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill) ⭐ 53,192 | 🐛 102 | 🌐 JavaScript | 📅 2026-09-14 — Cloudflare Web Security Audit Skill (by Cloudflare)

* **[emilkowalski/skills](https://github.com/emilkowalski/skills) ⭐ 51,548 | 🐛 2 | 🌐 Markdown | 📅 2026-10-28**: Source for Emil Kowalski design engineering skills - UI polish, motion review, animation standards, component craft, and high-taste frontend guidance (MIT).

* **[kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) ⭐ 50,416 | 🐛 74 | 📅 2026-09-15**: Obsidian-focused skills for markdown, Bases, JSON Canvas, CLI workflows, and content cleanup.

* **[zhaoxuya520/reverse-skill](https://github.com/zhaoxuya520/reverse-skill) ⭐ 43,775 | 🐛 38 | 🌐 PowerShell | 📅 2026-09-22**: Source for 43 security skills covering reverse engineering, binary analysis, offensive assessment orchestration, and threat-intelligence workflows, adapted with English metadata and upstream safety gates (MIT).

* **[VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) ⭐ 36,597 | 🐛 12 | 📅 2026-10-29**: Curated collection of 1000+ official and community agent skills from leading development teams (MIT).

* **[zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides) ⭐ 31,582 | 🐛 71 | 🌐 JavaScript | 📅 2026-06-23**: Frontend slide-creation skills for web-based presentations (MIT).

* **[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) ⭐ 28,997 | 🐛 1 | 🌐 Python | 📅 2026-10-29**: Senior Engineering and PM toolkit.

* **[AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo) ⭐ 24,150 | 🐛 75 | 🌐 Python | 📅 2026-10-22**: SEO workflow collection covering technical SEO, hreflang, sitemap, geo, schema, and programmatic SEO patterns.

* **[muratcankoylan/Agent-Skills-for-Context-Engineering](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering) ⭐ 18,249 | 🐛 58 | 🌐 Python | 📅 2026-10-12**: Context-engineering, multi-agent, and production agent-system skill collection (MIT).

* **[travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) ⭐ 15,632 | 🐛 905 | 📅 2026-04-28**: Loki Mode and Playwright integration.

* **[zubair-trabzada/geo-seo-claude](https://github.com/zubair-trabzada/geo-seo-claude) ⭐ 11,369 | 🐛 24 | 🌐 Python | 📅 2026-10-30**: Source for 14 GEO/SEO skills (`geo-audit`, `geo-citability`, `geo-technical`, …) — site audits and client reporting (MIT, docs-only; `geo-update` self-installer excluded).

* **[ibelick/ui-skills](https://github.com/ibelick/ui-skills) ⭐ 10,361 | 🐛 19 | 🌐 TypeScript | 📅 2026-10-25**: UI-polish skills for improving interfaces built by agents (MIT).

* **[diet103/claude-code-infrastructure-showcase](https://github.com/diet103/claude-code-infrastructure-showcase) ⭐ 10,048 | 🐛 18 | 🌐 TypeScript | 📅 2026-07-13**: Infrastructure and Backend/Frontend Guidelines.

* **[vudovn/antigravity-kit](https://github.com/vudovn/antigravity-kit) ⭐ 8,208 | 🐛 60 | 🌐 TypeScript | 📅 2026-10-18**: AI Agent templates with Skills, Agents, and Workflows (33 skills, MIT).

* **[czlonkowski/n8n-skills](https://github.com/czlonkowski/n8n-skills) ⭐ 6,548 | 🐛 22 | 🌐 Shell | 📅 2026-10-24**: n8n workflow-building skills for Claude Code (MIT).

* **[ChrisWiles/claude-code-showcase](https://github.com/ChrisWiles/claude-code-showcase) ⭐ 6,078 | 🐛 13 | 🌐 JavaScript | 📅 2026-01-06**: React UI patterns and Design Systems.

* **[sergebulaev/linkedin-skills](https://github.com/sergebulaev/linkedin-skills) ⭐ 5,369 | 🐛 0 | 🌐 Python | 📅 2026-10-27**: Source for the `linkedin-post-writer` skill - LinkedIn post drafting from 16 tested hook formulas mapped to engagement goals, with 2026 formatting rules and an AI-tell scrub pass, from a 10-skill LinkedIn bundle for Claude Code and Codex (MIT).

* **[elementalsouls/Claude-BugHunter](https://github.com/elementalsouls/Claude-BugHunter) ⭐ 5,348 | 🐛 2 | 🌐 Python | 📅 2026-10-29**: Source for 83 bug-bounty/red-team skills (79 offensive with `AUTHORIZED USE ONLY` + confirmation gates, 4 process skills) — recon, exploitation, and validation workflows across web, API, cloud, identity, and mobile attack surfaces (MIT, docs-only — helper scripts, commands, engine, and research assets not bundled).

* **[zebbern/claude-code-guide](https://github.com/zebbern/claude-code-guide) ⭐ 4,681 | 🐛 5 | 🌐 Python | 📅 2026-10-30**: Comprehensive Security suite & Guide (Source for \~60 new skills).

* **[davidondrej/skills](https://github.com/davidondrej/skills) ⭐ 4,184 | 🐛 4 | 🌐 Shell | 📅 2026-10-29**: Source for David Ondrej agent workflow skills across orchestration, research, setup, skill authoring, and documentation workflows (MIT).

* **[Dimillian/Skills](https://github.com/Dimillian/Skills) ⭐ 4,018 | 🐛 11 | 🌐 Shell | 📅 2026-03-29**: Curated Codex skills focused on Apple platforms, GitHub workflows, refactoring, and performance (MIT).

* **[CloudAI-X/threejs-skills](https://github.com/CloudAI-X/threejs-skills) ⭐ 3,851 | 🐛 0 | 📅 2026-10-19**: Three.js-focused skill collection for agent-assisted 3D web work.

* **[AvdLee/SwiftUI-Agent-Skill](https://github.com/AvdLee/SwiftUI-Agent-Skill) ⭐ 3,792 | 🐛 11 | 🌐 Python | 📅 2026-10-06**: SwiftUI best-practices skill for agent workflows (MIT).

* **[cclank/lanshu-create-ai-presenter-video](https://github.com/cclank/lanshu-create-ai-presenter-video) ⭐ 2,846 | 🐛 3 | 🌐 HTML | 📅 2026-10-11**: Source for `lanshu-create-ai-presenter-video`.

* **[yaojingang/yao-meta-skill](https://github.com/yaojingang/yao-meta-skill) ⭐ 2,717 | 🐛 4 | 🌐 Python | 📅 2026-08-17**: Source for the `yao-meta-skill` skill - governed skill creation, refactoring, evaluation, packaging, review, and distribution workflows (MIT).

* **[amElnagdy/delegate-skills](https://github.com/amElnagdy/delegate-skills) ⭐ 2,534 | 🐛 40 | 🌐 JavaScript | 📅 2026-10-29**: Source for 18 delegation skills (`delegate-setup` + 17 implementer relays for Claude/Codex/Cursor/OpenCode and 13 more) — multi-agent delegation and fleet orchestration with Node built-ins only, relay never commits (MIT, docs-only — runtime not bundled).

* **[rmyndharis/antigravity-skills](https://github.com/rmyndharis/antigravity-skills) ⭐ 1,891 | 🐛 6 | 🌐 JavaScript | 📅 2026-10-14**: For the massive contribution of 300+ Enterprise skills and the catalog generation logic.

* **[hyhmrright/brooks-lint](https://github.com/hyhmrright/brooks-lint) ⭐ 1,550 | 🐛 0 | 🌐 HTML | 📅 2026-10-26**: AI code-review skill grounded in classic software engineering books for design-smell, coupling, and architecture review.

* [amElnagdy/guard-skills](https://github.com/amElnagdy/guard-skills) ⭐ 1,293 | 🐛 4 | 📅 2026-07-04 — Code Quality & Testing Guard Skills (by amElnagdy)

* **[gooseworks-ai/goose-skills](https://github.com/gooseworks-ai/goose-skills) ⭐ 1,273 | 🐛 74 | 🌐 JavaScript | 📅 2026-10-27**: Source for the `competitor-ad-intelligence` and `ad-campaign-analyzer` skills - evidence-labeled public ad research plus uncertainty-aware campaign diagnostics and bounded budget tests (MIT).

* **[BagelHole/DevOps-Security-Agent-Skills](https://github.com/BagelHole/DevOps-Security-Agent-Skills) ⭐ 1,184 | 🐛 5 | 🌐 Shell | 📅 2026-05-22** (compliance batch): Source for 19 governance/framework/continuity/auditing skills (MIT, docs-only).

* **[BagelHole/DevOps-Security-Agent-Skills](https://github.com/BagelHole/DevOps-Security-Agent-Skills) ⭐ 1,184 | 🐛 5 | 🌐 Shell | 📅 2026-05-22** (security batch): Source for 35 secrets, scanning, network, operations, and AI-security skills (MIT, docs-only).

* **[BagelHole/DevOps-Security-Agent-Skills](https://github.com/BagelHole/DevOps-Security-Agent-Skills) ⭐ 1,184 | 🐛 5 | 🌐 Shell | 📅 2026-05-22** (infrastructure batch): Source for 70 server, storage, database, networking, cloud, and local-AI infrastructure skills (MIT, docs-only).

* **[BagelHole/DevOps-Security-Agent-Skills](https://github.com/BagelHole/DevOps-Security-Agent-Skills) ⭐ 1,184 | 🐛 5 | 🌐 Shell | 📅 2026-05-22** (devops batch): Source for 39 CI/CD, orchestration, observability, release, and AI-ops skills (MIT, docs-only).

* **[ZeroPointRepo/youtube-skills](https://github.com/ZeroPointRepo/youtube-skills) ⭐ 1,135 | 🐛 7 | 📅 2026-10-27**: Source for the `youtube-full` skill - TranscriptAPI-backed YouTube transcripts, search, channel browsing, playlists, and cloud-safe video research workflows (MIT).

* **[bitjaru/styleseed](https://github.com/bitjaru/styleseed) ⭐ 992 | 🐛 8 | 🌐 JavaScript | 📅 2026-10-28**: StyleSeed Toss UI and UX skill collection - setup wizard, page and pattern generation, design-token management, accessibility review, UX audits, feedback states, and microcopy guidance for professional mobile-first UI.

* **[guanyang/antigravity-skills](https://github.com/guanyang/antigravity-skills) ⭐ 984 | 🐛 7 | 🌐 TypeScript | 📅 2026-10-29**: Core Antigravity extensions.

* **[huifer/WellAlly-health](https://github.com/huifer/WellAlly-health) ⭐ 963 | 🐛 7 | 🌐 Shell | 📅 2026-07-16**: Healthcare assistant project cited in release history as a source for health-focused agent capabilities (MIT).

* **[vibeforge1111/vibeship-spawner-skills](https://github.com/vibeforge1111/vibeship-spawner-skills) ⭐ 884 | 🐛 14 | 🌐 JavaScript | 📅 2026-01-02**: AI agents, integrations, maker tools, and other production-grade skill packs.

* **[Optim-Agent/optim-agent](https://github.com/Optim-Agent/optim-agent) ⭐ 798 | 🐛 1 | 🌐 Python | 📅 2026-08-14**: Source for the `optim-agent` skill - agent-guided optimization of configurable systems against measurable objectives (MIT).

* **[ZhangHanDong/makepad-skills](https://github.com/ZhangHanDong/makepad-skills) ⭐ 752 | 🐛 0 | 📅 2026-04-07**: Makepad app-development skills and references (MIT).

* **[karanb192/awesome-claude-skills](https://github.com/karanb192/awesome-claude-skills) ⭐ 576 | 🐛 238 | 📅 2026-10-29**: A massive list of verified skills for Claude Code.

* **[sanjay3290/ai-skills](https://github.com/sanjay3290/ai-skills) ⭐ 447 | 🐛 8 | 🌐 Python | 📅 2026-09-10**: Apache-licensed collection of agent skills for AI coding assistants.

* **[baskduf/FableCodex](https://github.com/baskduf/FableCodex) ⭐ 439 | 🐛 11 | 🌐 Python | 📅 2026-07-26**: Source for the `codex-fable5` skill - Codex-native Fable-inspired workflow discipline for evidence-first implementation, goal tracking, review findings, verification gates, and prompt adaptation (AGPL-3.0-or-later).

* **[LambdaTest/agent-skills](https://github.com/LambdaTest/agent-skills) ⭐ 386 | 🐛 4 | 🌐 Python | 📅 2026-10-13**: Production-grade agent skills for test automation — 46 skills covering E2E, unit, mobile, BDD, visual, and cloud testing across 15+ languages (MIT).

* **[zxkane/aws-skills](https://github.com/zxkane/aws-skills) ⭐ 373 | 🐛 0 | 🌐 Python | 📅 2026-06-15**: AWS-focused Claude agent skills (MIT).

* **[AlmogBaku/debug-skill](https://github.com/AlmogBaku/debug-skill) ⭐ 335 | 🐛 2 | 🌐 Go | 📅 2026-04-17**: Interactive debugger skill for AI agents — breakpoints, stepping, variable inspection, and stack traces via the `dap` CLI. Supports Python, Go, Node.js/TypeScript, Rust, and C/C++.

* **[ohad6k/ditto](https://github.com/ohad6k/ditto) ⭐ 302 | 🐛 16 | 🌐 HTML | 📅 2026-10-12**: Source for the `ditto` skill - mines local coding-agent sessions into private, evidence-backed work, design, and writing profiles with dated source receipts (MIT).

* **[Continuum-AI-Corp/OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) ⭐ 287 | 🐛 2 | 🌐 TypeScript | 📅 2026-10-01**: Source for the `orca-replay` skill - reading, replaying, and forking recorded coding-agent runs, so a question about what a past run did is answered from its trace rather than from memory (Apache-2.0).

* **[drogers0/gh-image](https://github.com/drogers0/gh-image) ⭐ 281 | 🐛 3 | 🌐 Go | 📅 2026-10-27**: Source for the `gh-image` skill - GitHub CLI image uploads that return canonical `user-attachments` embed URLs for PRs, issues, comments, and README screenshots (MIT).

* **[provencher/codex-skills](https://github.com/provencher/codex-skills) ⭐ 275 | 🐛 0 | 📅 2026-07-26**: Source for the `orchestrate` skill - focused Codex multi-agent delegation with non-overlapping ownership, coordinator integration, and user-held approval gates (MIT).

* **[scarletkc/vexor](https://github.com/scarletkc/vexor) ⭐ 247 | 🐛 5 | 🌐 Python | 📅 2026-10-29**: Semantic search engine for files and code, referenced in release history.

* **[taisly/agent](https://github.com/taisly/agent) ⭐ 222 | 🐛 2 | 🌐 JavaScript | 📅 2026-10-22**: Source for the Taisly Social Media Posting skill - Codex plugin, CLI, SDK, and official MCP server for publishing approved short-form videos to TikTok, Instagram Reels, YouTube Shorts, X, and Facebook (MIT).

* **[jthack/ffuf\_claude\_skill](https://github.com/jthack/ffuf_claude_skill) ⭐ 214 | 🐛 2 | 🌐 Python | 📅 2025-10-16**: FFUF skill for web fuzzing workflows in Claude.

* **[sandbaseai/sandbase-skills](https://github.com/sandbaseai/sandbase-skills) ⭐ 203 | 🐛 1 | 🌐 Python | 📅 2026-09-26**: Source for the `multi-source-search` skill - cross-validated research with explicit source diversity, confidence, conflicts, gaps, and an offline-checkable evidence ledger (Apache-2.0).

* **[gokapso/agent-skills](https://github.com/gokapso/agent-skills) ⭐ 194 | 🐛 7 | 🌐 JavaScript | 📅 2026-10-09**: Kapso/WhatsApp-oriented agent skills.

* **[Ducksss/codex-profiles](https://github.com/Ducksss/codex-profiles) ⭐ 192 | 🐛 1 | 🌐 Shell | 📅 2026-10-29**: Source for the `codex-profiles` skill - Codex CLI/Desktop profile isolation around separate `CODEX_HOME` directories, diagnostics, and account-context boundaries without copying auth tokens (MIT).

* **[socai-io/jev-social](https://github.com/socai-io/jev-social) ⭐ 190 | 🐛 14 | 🌐 JavaScript | 📅 2026-10-12**: Source for the `jev-social` skill — read-only Jev/socai social research routing (MIT).

* **[MohamedAbdallah-14/unslop](https://github.com/MohamedAbdallah-14/unslop) ⭐ 165 | 🐛 6 | 🌐 Python | 📅 2026-10-26**: Source for the `unslop` skill - deterministic and LLM-assisted cleanup for AI-generated prose across CLI and agent tool workflows.

* **[amElnagdy/review-skills](https://github.com/amElnagdy/review-skills) ⭐ 163 | 🐛 3 | 🌐 JavaScript | 📅 2026-10-09**: Source for the `debate-review` and `babysit-pr` skills - two-model debate review of PRs/MRs with inline comments and automated babysitting of review rounds for GitHub, GitLab and Azure DevOps (MIT, docs-only — runtime not bundled).

* **[supercorp-ai/supercov](https://github.com/supercorp-ai/supercov) ⭐ 159 | 🐛 3 | 🌐 Rust | 📅 2026-10-29**: MIT source for the `supercov` skill — line, branch and MC/DC coverage of a project's existing tests, used to write focused tests for the untested code.

* **[luoyuctl/agenttrace](https://github.com/luoyuctl/agenttrace) ⭐ 152 | 🐛 5 | 🌐 Rust | 📅 2026-10-26**: Source for the `agenttrace-session-audit` skill - local AI coding-agent session audits for cost spikes, tool failures, latency gaps, anomalies, health gates, and session diffs (MIT).

* **[kubestellar/console](https://github.com/kubestellar/console) ⭐ 152 | 🐛 39 | 🌐 TypeScript | 📅 2026-10-30**: KubeStellar Console multi-cluster Kubernetes dashboard with `kc-agent` MCP integration, AI-assisted operations, and built-in agent skills.

* **[wrsmith108/linear-claude-skill](https://github.com/wrsmith108/linear-claude-skill) ⭐ 139 | 🐛 1 | 🌐 TypeScript | 📅 2026-07-17**: Linear issue/project/team management skill with MCP and GraphQL workflows (MIT).

* **[Necmttn/ax](https://github.com/Necmttn/ax) ⭐ 122 | 🐛 42 | 🌐 TypeScript | 📅 2026-10-28**: Source for the `ax-extract-workflow` skill - reconstruct workflow behind past coding-agent artifacts using local ax sessions, commits, skills, and tool traces (AGPL-3.0-only).

* **[MetcalfSolutions/Satori](https://github.com/MetcalfSolutions/Satori) ⭐ 115 | 🐛 0 | 🌐 Python | 📅 2026-10-30**: Clinically informed wisdom companion blending psychology frameworks and wisdom traditions into a structured reflective partner.

* **[awss1i/assay](https://github.com/awss1i/assay) ⭐ 109 | 🐛 1 | 🌐 Python | 📅 2026-10-29**: MIT source for the `assay` skill. Deterministic local QA that opens a web page you built in a real browser, drives every control, and reports where the page contradicts itself, with no tests to write, no API key, and no network.

* **[JunsW/feature-track](https://github.com/JunsW/feature-track) ⭐ 107 | 🐛 0 | 🌐 Python | 📅 2026-07-16**: Source for the `feature-tracking` skill - lightweight repository-native feature memory for current status, source-of-truth documents, decisions, risks, and cross-session handoff (MIT).

* **[ndesv21/socialclaw](https://github.com/ndesv21/socialclaw) ⭐ 103 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-12**: Source for the SocialClaw social media publishing skill - campaign scheduling and publishing across major social platforms with a single workspace API key.

* **[monte-carlo-data/mc-agent-toolkit](https://github.com/monte-carlo-data/mc-agent-toolkit) ⭐ 93 | 🐛 7 | 🌐 Python | 📅 2026-10-28**: Monte Carlo data observability skills — table health checks, change impact assessment, monitor creation, push ingestion, and SQL validation notebooks for dbt changes.

* **[njerschow/textme](https://github.com/njerschow/textme) ⭐ 92 | 🐛 0 | 🌐 TypeScript | 📅 2026-04-09**: Source for the `textme` skill — local daemon bridging inbound iMessages (via Sendblue) to a Claude Code session on the user's machine, with voice notes, image input, code execution, and a phone-number whitelist (MIT).

* **[jonathimer/devmarketing-skills](https://github.com/jonathimer/devmarketing-skills) ⭐ 87 | 🐛 0 | 📅 2026-03-03**: Developer marketing skills — HN strategy, technical tutorials, docs-as-marketing, Reddit engagement, developer onboarding, and more (33 skills, MIT).

* **[Continuum-AI-Corp/OrcaPromptVault](https://github.com/Continuum-AI-Corp/OrcaPromptVault) ⭐ 81 | 🐛 0 | 📅 2026-10-01**: Source for the `system-prompt-lookup` skill - a dated archive of shipped AI products' system prompts and tool schemas, each labelled captured off the wire or reported by the model itself, so a claim about what an agent was instructed to do is answered from the artifact rather than from memory (AGPL-3.0).

* **[tubeagentkit/youtube-transcript-skills](https://github.com/tubeagentkit/youtube-transcript-skills) ⭐ 80 | 🐛 2 | 🌐 Shell | 📅 2026-10-30**: Source for the `youtube-transcript-skills` skill - YouTube transcript fetching, video/channel search, channel browsing, and playlist extraction via the getyoutubetranscript.com API, free tier with no card required (MIT).

* **[shitianfang/jev-use](https://github.com/shitianfang/jev-use) ⭐ 65 | 🐛 7 | 🌐 JavaScript | 📅 2026-09-22**: Source for the `jev-use` skill - routing an agent loop's no-text judgment steps to the Jev judgment model via the `jev_judge` / `jev_gate` MCP tools, batched per state, with a typed escalation contract that hands writing and low-confidence steps back to the LLM (MIT).

* **[xiehuan123/dsh-deepread](https://github.com/xiehuan123/dsh-deepread) ⭐ 63 | 🐛 0 | 🌐 JavaScript | 📅 2026-09-11**: Source for the `dsh-deepread` skill - evidence-first analysis of articles, books, PDFs, and document sets with claim tracing, knowledge maps, and Feynman checks (MIT).

* **[SHADOWPR0/beautiful\_prose](https://github.com/SHADOWPR0/beautiful_prose) ⭐ 61 | 🐛 0 | 📅 2026-10-26**: Writing-quality skill for improving prose and reducing generic output.

* **[Silverov/yandex-direct-skill](https://github.com/Silverov/yandex-direct-skill) ⭐ 60 | 🐛 1 | 🌐 Shell | 📅 2026-10-22**: Yandex Direct (API v5) advertising audit skill — 55 automated checks, A-F scoring, campaign/ad/keyword analysis for the Russian PPC market (MIT).

* **[shmlkv/dna-claude-analysis](https://github.com/shmlkv/dna-claude-analysis) ⭐ 58 | 🐛 0 | 🌐 Python | 📅 2026-03-04**: Personal genome analysis toolkit — Python scripts analyzing raw DNA data across 17 categories (health risks, ancestry, pharmacogenomics, nutrition, psychology, etc.) with terminal-style single-page HTML visualization.

* **[robzolkos/skill-rails-upgrade](https://github.com/robzolkos/skill-rails-upgrade) ⭐ 54 | 🐛 0 | 📅 2026-01-27**: Rails upgrade skill for agent-assisted migrations.

* **[rafsilva85/credit-optimizer-v5](https://github.com/rafsilva85/credit-optimizer-v5) ⭐ 52 | 🐛 0 | 🌐 Python | 📅 2026-05-25**: Manus AI credit optimizer skill — intelligent model routing, context compression, and smart testing. Saves 30-75% on credits with zero quality loss. Audited across 53 scenarios.

* **[Suraj1235/open-dynamic-workflows](https://github.com/Suraj1235/open-dynamic-workflows) ⭐ 50 | 🐛 2 | 🌐 JavaScript | 📅 2026-07-09**: Source for the `open-dynamic-workflows` skill - open-source dynamic multi-agent workflow engine that plans, orchestrates, and adversarially verifies parallel AI coding agents across OpenCode, Codex, Antigravity, and VS Code (MIT).

* **[adelaidasofia/ai-brain-starter](https://github.com/adelaidasofia/ai-brain-starter) ⭐ 50 | 🐛 52 | 🌐 Python | 📅 2026-10-29**: Source for the `ingest-youtube` skill - YouTube transcript ingestion into markdown vaults with yt-dlp metadata, VTT cleanup, and capture-seed stubs (MIT).

* **[glukicov/slideops](https://github.com/glukicov/slideops) ⭐ 50 | 🐛 0 | 🌐 HTML | 📅 2026-10-25**: Source for the `slideops` skill - cited HTML slide decks generated from a repository, with a standard-library drift check that reports the day the slides stop matching the code (MIT).

* **[romankurnovskii/etemaro](https://github.com/romankurnovskii/etemaro) ⭐ 44 | 🐛 39 | 🌐 TypeScript | 📅 2026-10-28**: Source of the `meteora-dlmm-pool-screening` skill - read-only screening and ranking of Meteora DLMM pools from public APIs (MIT).

* **[sudosubin/gh-attach](https://github.com/sudosubin/gh-attach) ⭐ 44 | 🐛 2 | 🌐 Go | 📅 2026-10-27**: Source for the `gh-attach` skill - GitHub CLI uploads and downloads of `user-attachments` (screenshots, PDFs, zips, videos), producing repo-scoped URLs for PRs, issues, and READMEs, with GitHub Enterprise Server support (MIT).

* **[umutbozdag/agent-skills-manager](https://github.com/umutbozdag/agent-skills-manager) ⭐ 43 | 🐛 2 | 🌐 TypeScript | 📅 2026-04-09**: Source for the `manage-skills` skill - cross-tool skill discovery, creation, editing, toggling, copying, moving, and deletion workflows across major agent coding tools.

* **[Hanyuyuan6/remote-gpu-trainer](https://github.com/Hanyuyuan6/remote-gpu-trainer) ⭐ 42 | 🐛 0 | 🌐 Python | 📅 2026-10-28**: Source for the `remote-gpu-trainer` skill - rented and remote GPU job orchestration, monitoring, teardown safety, spot resilience, and DL-debug workflows (MIT).

* **[frmoretto/clarity-gate](https://github.com/frmoretto/clarity-gate) ⭐ 35 | 🐛 0 | 🌐 Python | 📅 2026-03-02**: Verification protocol for marking uncertainty and reducing hallucinated certainty in LLM-facing docs.

* **[webzler/agentMemory](https://github.com/webzler/agentMemory) ⭐ 33 | 🐛 5 | 🌐 TypeScript | 📅 2026-10-21**: Source for the agent-memory-mcp skill.

* **[wrsmith108/varlock-claude-skill](https://github.com/wrsmith108/varlock-claude-skill) ⭐ 33 | 🐛 1 | 📅 2026-03-04**: Secure environment-variable management skill for Claude Code (MIT).

* **[talivia-group/agent](https://github.com/talivia-group/agent) ⭐ 32 | 🐛 3 | 🌐 JavaScript | 📅 2026-10-01**: Source for the `talivia-agent-kit` skill - revenue-first website analytics through the official MCP server, with explicit confirmation for tracking and payment attribution changes (MIT).

* **[sstklen/infinite-gratitude](https://github.com/sstklen/infinite-gratitude) ⭐ 31 | 🐛 0 | 📅 2026-03-15**: Multi-agent research skill from the AI Dojo series (MIT).

* **[yikuansun/PhotopeaAPI](https://github.com/yikuansun/PhotopeaAPI) ⭐ 30 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-04**: Source for the `photopea-embedded-editor` skill - Photopea embedding, host-page messaging, file I/O, scripting, and export workflows for web apps (MIT).

* **[iradoweck/antigravity-awesome-skills](https://github.com/iradoweck/antigravity-awesome-skills) ⭐ 30 | 🐛 0 | 🌐 Python | 📅 2026-10-21**: Source for the GeminiIgnore FinOps skill - `.geminiignore` setup patterns for context-window efficiency and token cost reduction.

* **[sendblue-api/sendblue-cli](https://github.com/sendblue-api/sendblue-cli) ⭐ 30 | 🐛 4 | 🌐 TypeScript | 📅 2026-09-01**: Source for the `sendblue-cli`, `sendblue-api`, and `sendblue-notify` skills — iMessage, SMS, and RCS messaging via Sendblue's CLI and HTTP API, plus "text me when X finishes" notification patterns for Claude Code hooks and `/loop` / `/schedule` jobs (MIT).

* **[NotMyself/claude-win11-speckit-update-skill](https://github.com/NotMyself/claude-win11-speckit-update-skill) ⚠️ Archived**: Archived Speckit update skill for Claude Code (MIT).

* **[uxuiprinciples/agent-skills](https://github.com/uxuiprinciples/agent-skills) ⭐ 27 | 🐛 0 | 📅 2026-08-31**: Research-backed UX/UI agent skills for auditing interfaces against 168 principles, detecting antipatterns, and injecting UX context into AI coding sessions.

* **[zircote/.claude](https://github.com/zircote/.claude) ⚠️ Archived**: Archived Claude Code dotfiles/config repo with a Shopify development skill reference.

* **[hyhmrright/logic-lens](https://github.com/hyhmrright/logic-lens) ⭐ 25 | 🐛 7 | 🌐 Python | 📅 2026-10-29**: AI code-review skill for formal logic inspection across bugs, race conditions, security risks, and API contract issues.

* **[TheaDust/lore](https://github.com/TheaDust/lore) ⭐ 24 | 🐛 0 | 🌐 Python | 📅 2026-08-29**: Source for the `lore` skill - Markdown-only, zero-dependency long-term project memory for AI coding agents, with monorepo scopes, two-section platform mirrors, and stdlib Python helpers (MIT).

* **[rainmanjam/poka-yoke](https://github.com/rainmanjam/poka-yoke) ⭐ 24 | 🐛 3 | 🌐 Python | 📅 2026-10-27**: Source for the `poka-yoke` skill - software mistake-proofing through control, warning, detection, and source-inspection guardrails (MIT).

* **[mbenhard/unship](https://github.com/mbenhard/unship) ⭐ 23 | 🐛 0 | 🌐 JavaScript | 📅 2026-09-16**: Source for the `unship` skill - local workflow for comparing AI-generated UI variants in a real app, then keeping one option and cleaning up temporary alternatives (MIT).

* **[TerminallyLazy/Tree-Ring-Memory](https://github.com/TerminallyLazy/Tree-Ring-Memory) ⭐ 22 | 🐛 3 | 🌐 Rust | 📅 2026-09-17**: Source for the `tree-ring-memory` skill — local-first memory lifecycle guidance for recall, evidence, audit, forgetting, consolidation, and privacy-safe agent memory operations (MIT).

* **[wede-wx/atlas](https://github.com/wede-wx/atlas) ⭐ 21 | 🐛 1 | 📅 2026-06-11**: Source for the `atlas-contract` and `atlas-ledger` goal-integrity skills - contract, phase-check, final-audit, and project-ledger guardrails for long-running agent work (MIT).

* **[uberSKILLS](https://github.com/uberskillsdev/uberSKILLS) ⭐ 21 | 🐛 1 | 🌐 TypeScript | 📅 2026-04-04**: Design, test, and deploy Claude Code Agent Skills through a visual, AI-assisted workflow.

* **[anthony-chaudhary/dos-kernel](https://github.com/anthony-chaudhary/dos-kernel) ⭐ 20 | 🐛 123 | 🌐 Python | 📅 2026-10-27**: Source for the `dos-verify-done-claims` skill — gates an agent's "done / shipped / fixed" claim on git ground truth (ancestry + the commit's own diff) via the deterministic DOS kernel's read-only `dos verify` / `dos commit-audit` verbs (MIT).

* **[cis2042/ux3-product-design-harness](https://github.com/cis2042/ux3-product-design-harness) ⭐ 19 | 🐛 2 | 🌐 Python | 📅 2026-10-23**: Source for `product-design-harness`.

* **[xi-kari/crossframe-skill](https://github.com/xi-kari/crossframe-skill) ⭐ 18 | 🐛 0 | 🌐 Python | 📅 2026-08-07**: Source for the CrossFrame Skill Suite - Chinese-canonical structural diagnosis, essay drafting, review, and companion workflows across relationships, organizations, institutions, public issues, and research notes (MIT).

* **[SeanZoR/claude-speed-reader](https://github.com/SeanZoR/claude-speed-reader) ⭐ 18 | 🐛 0 | 🌐 HTML | 📅 2026-01-15**: RSVP-style speed-reading helper for Claude responses (MIT).

* **[abhinaykrupa/cowork-to-code-bridge](https://github.com/abhinaykrupa/cowork-to-code-bridge) ⭐ 16 | 🐛 1 | 🌐 Python | 📅 2026-10-08**: Source for the `cowork-to-code-bridge` skill - consent-bound execution on the user's own machine with pinned provenance, narrow scopes, and explicit local-agent limitations (MIT).

* **[ejentum/ejentum-mcp](https://github.com/ejentum/ejentum-mcp) ⭐ 16 | 🐛 2 | 🌐 JavaScript | 📅 2026-06-11**: Source for the `ejentum-reasoning-harness` skill - MCP cognitive harness modes for reasoning, code review, anti-deception checks, and memory-drift analysis (MIT).

* **[amartelr/antigravity-workspace-manager](https://github.com/amartelr/antigravity-workspace-manager) ⭐ 16 | 🐛 1 | 🌐 Python | 📅 2026-02-28**: Workspace Manager CLI companion to dynamically auto-provision subsets of skills across local development environments.

* **[Intelligent-Internet/II-Commons-Skills](https://github.com/Intelligent-Internet/II-Commons-Skills) ⭐ 16 | 🐛 1 | 🌐 JavaScript | 📅 2026-07-08**: Source for the II-Commons research skill - deterministic retrieval across arXiv, PubMed/PMC, and supported US policy corpora.

* **[Phelan164/codex-howto](https://github.com/Phelan164/codex-howto) ⭐ 15 | 🐛 3 | 🌐 Python | 📅 2026-10-27**: Source for the `maintain-codex-wiki` skill - review-first engineering knowledge with provenance, explicit capture and promotion, and deterministic structural checks (MIT).

* **[alexyc9381/shark-skill](https://github.com/alexyc9381/shark-skill) ⭐ 14 | 🐛 1 | 🌐 Python | 📅 2026-10-04** and **[alexyc9381/court-skill](https://github.com/alexyc9381/court-skill) ⭐ 218 | 🐛 2 | 🌐 Python | 📅 2026-10-04**: MIT sources for the `shark` and `court` skills by Alex Chen (@nocodealex). Each is a panel of Claude sub-agents (investors, or a jury) that stress-tests an idea.

* **[whatiskadudoing/fp-ts-skills](https://github.com/whatiskadudoing/fp-ts-skills) ⭐ 14 | 🐛 0 | 📅 2026-01-30**: Practical fp-ts skills for TypeScript – fp-ts-pragmatic, fp-ts-react, fp-ts-errors (v4.4.0).

* **[onkarbadve/agy-auto](https://github.com/onkarbadve/agy-auto) ⭐ 13 | 🐛 1 | 🌐 Python | 📅 2026-09-21**: MIT community source for `agy-auto`, providing guarded Antigravity CLI permission automation with scoped approvals.

* **[jackjin1997/ClawForge](https://github.com/jackjin1997/ClawForge) ⭐ 13 | 🐛 1 | 🌐 Python | 📅 2026-06-16**: Resource hub of skills, MCP servers, and agent tooling for OpenClaw.

* **[timwukp/agent-skills-best-practice](https://github.com/timwukp/agent-skills-best-practice) ⭐ 12 | 🐛 0 | 🌐 Python | 📅 2026-09-16**: Source for the `fsi-compliance-checker` skill - financial-services compliance triage for PCI-DSS v4.0 and MAS TRM control mapping (MIT).

* **[fullstackcrew-alpha/privacy-mask](https://github.com/fullstackcrew-alpha/privacy-mask) ⭐ 12 | 🐛 0 | 🌐 Python | 📅 2026-03-24**: Local image privacy masking for AI coding agents. Detects and redacts PII, API keys, and secrets in screenshots via OCR + 47 regex rules. Claude Code hook integration for automatic masking. Supports Tesseract and RapidOCR. 100% offline (MIT).

* **[connerkward/screenstudio-alternative-skill](https://github.com/connerkward/screenstudio-alternative-skill) ⭐ 11 | 🐛 0 | 🌐 Python | 📅 2026-06-23**: Source for the `screenstudio-alt` skill - open-source screen recording polish with auto-zoom, idle speed-up, cursor treatment, captions, and vertical export workflows (MIT).

* **[nedcodes-ok/rule-porter](https://github.com/nedcodes-ok/rule-porter) ⭐ 11 | 🐛 4 | 🌐 JavaScript | 📅 2026-03-04**: Bidirectional rule converter between Cursor (.mdc), Claude Code (CLAUDE.md), GitHub Copilot, Windsurf, and legacy .cursorrules formats. Zero dependencies.

* **[sandbaseai/awesome-workbuddy](https://github.com/sandbaseai/awesome-workbuddy) ⭐ 10 | 🐛 5 | 🌐 Python | 📅 2026-09-11**: Source for the `skill-security-audit` skill - read-only-by-default review of Agent Skills, MCP servers, connectors, and extensions across permissions, provenance, credentials, data flow, and irreversible actions (CC0-1.0).

* **[stareezy-1/frontend-architecture-skill](https://github.com/stareezy-1/frontend-architecture-skill) ⭐ 10 | 🐛 0 | 📅 2026-06-14**: Source for the `frontend-lighthouse` skill - portable Lighthouse CI Core Web Vitals gates, performance budgets, and GitHub Actions reporting (MIT).

* **[bin1874/before-you-build-skill](https://github.com/bin1874/before-you-build-skill) ⭐ 10 | 🐛 0 | 🌐 JavaScript | 📅 2026-07-01**: Source for the `before-you-build` skill - pre-coding product risk review across demand, alternatives, switching costs, channels, and validation steps (MIT).

* **[demo112/yunqu-ai-skills](https://github.com/demo112/yunqu-ai-skills) ⭐ 10 | 🐛 1 | 🌐 HTML | 📅 2026-05-13**: Source for WeChat official account, Xiaohongshu content strategy, and MCP tool development skills for Chinese-language platform workflows (MIT).

* **[sarveshtalele/linkedin-content-skill](https://github.com/sarveshtalele/linkedin-content-skill) ⭐ 10 | 🐛 0 | 🌐 Python | 📅 2026-06-01**: Source for the `linkedin-content-generator` skill - LinkedIn post, carousel, newsletter, and content-calendar generation workflows with local feedback memory (MIT).

* **[AgentPhone-AI/skills](https://github.com/AgentPhone-AI/skills) ⭐ 10 | 🐛 0 | 📅 2026-09-04**: AgentPhone plugin for Claude Code — API-first telephony workflows for AI agents, including phone calls, SMS, phone-number management, voice-agent setup, streaming webhooks, and tool-calling patterns.

* **[connerkward/ckw-design-skill](https://github.com/connerkward/ckw-design-skill) ⭐ 9 | 🐛 0 | 🌐 JavaScript | 📅 2026-06-17**: Source for the `ckw-design` skill - frontend design direction, design-system guidance, visual philosophy, spatial checks, usability review, and production UI polish workflows (MIT).

* **[rich-elicitation](https://github.com/CyberZenithX/Rich-Elicitation-Skill) ⭐ 9 | 🐛 0 | 📅 2026-05-07**: Source for the `rich-elicitation` skill - asks clarifying questions in multiple rounds before starting ambiguous tasks.

* **[riffkit/skill](https://github.com/riffkit/skill) ⭐ 8 | 🐛 0 | 📅 2026-10-28**: Official upstream source for the `riffkit` skill - short-form video riffing and UGC ad generation in nine natively generated languages (MIT).

* **[sparklingneuronics/sparkling-skills](https://github.com/sparklingneuronics/sparkling-skills) ⭐ 8 | 🐛 0 | 🌐 Python | 📅 2026-10-29**: Source for the `dispatch` skill - multi-CLI delegation from Claude Code to Codex, Antigravity, and Gemini agents (MIT).

* **[connerkward/mcp-apple-notes](https://github.com/connerkward/mcp-apple-notes) ⭐ 8 | 🐛 1 | 🌐 HTML | 📅 2026-06-17**: Source for the `apple-notes-search` skill - semantic and keyword search, related-note discovery, bridge finding, entity threads, and cited synthesis across local Apple Notes via MCP (MIT).

* **[aomi-labs/skills](https://github.com/aomi-labs/skills) ⭐ 8 | 🐛 10 | 🌐 Shell | 📅 2026-10-22**: Source for the `aomi-transact` skill — natural-language driver for the Aomi CLI with account-abstraction-first execution and simulate-then-sign across 25+ DeFi apps (MIT).

* **[heyneuron/flowhunt-skill](https://github.com/heyneuron/flowhunt-skill) ⭐ 8 | 🐛 1 | 📅 2026-05-21**: Source for the FlowHunt automation discovery audit skill - workflow intake, tool-by-tool audit, and opportunity prioritization for productivity automation.

* **[SHADOWPR0/security-bluebook-builder](https://github.com/SHADOWPR0/security-bluebook-builder) ⭐ 8 | 🐛 0 | 📅 2026-10-26**: Security documentation/buildbook skill for agent workflows.

* **[maxbaluev/accreted-intelligence](https://github.com/maxbaluev/accreted-intelligence) ⭐ 8 | 🐛 2 | 🌐 Shell | 📅 2026-07-05**: Source for the `accint-solve` skill — routes coding-agent work through AccInt's MCP memory loop with retrieval, continuation frames, commitments, and outcome feedback (Apache 2.0).

* **[cruisekkk/time-ledger](https://github.com/cruisekkk/time-ledger) ⭐ 7 | 🐛 1 | 📅 2026-07-07**: Source for the `time-ledger` skill - natural-language time tracking parsed into the user's own Notion database with ask-instead-of-guessing reconciliation (MIT).

* **[ZeroPointRepo/zillow-skills](https://github.com/ZeroPointRepo/zillow-skills) ⭐ 7 | 🐛 0 | 🌐 Python | 📅 2026-10-27**: Source for the `us-property-data` skill - U.S. property lookup, valuation, listing, tax, school, photo, and price-history guidance through the independent Zillapi API (MIT-0).

* **[commitshow/production-audit](https://github.com/commitshow/production-audit) ⭐ 7 | 🐛 0 | 📅 2026-05-04**: Source for the `production-audit` skill - shipped-app readiness auditing across deployment health, RLS, webhooks, secrets exposure, grants, Stripe idempotency, and mobile UX.

* **[vipin-si/article-illustrations](https://github.com/vipin-si/article-illustrations) ⭐ 7 | 🐛 0 | 📅 2026-06-23**: Source for the `article-illustrations` skill - Grav-style hand-drawn article illustrations with whiteboard sketches, sparse annotations, and visual metaphor QA guidance (MIT).

* **[warmskull/idea-darwin](https://github.com/warmskull/idea-darwin) ⭐ 7 | 🐛 0 | 📅 2026-04-07**: Darwinian idea-evolution workflow for structured ideation rounds, mutation, crossbreeding, critique, and lineage tracking.

* **[flyingsquirrel0419/squirrel-skill](https://github.com/flyingsquirrel0419/squirrel-skill) ⭐ 7 | 🐛 0 | 🌐 Shell | 📅 2026-04-29**: Full-cycle software development skill — plans, builds, tests, lints, fixes bugs, and writes production-grade docs. Auto-detects project state and adapts its 8-phase pipeline. Works on 9 AI coding agent platforms (Apache 2.0).

* **[Pranav-Nexus/antigravity-skill-porter](https://github.com/Pranav-Nexus/antigravity-skill-porter) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-10-08**: MIT source for `skill-porter`, adapted for conservative local bundle previews and complete support-file copying.

* **[atdy/maoxuan-product-agent](https://github.com/atdy/maoxuan-product-agent) ⭐ 6 | 🐛 0 | 🌐 Markdown | 📅 2026-07-10**: Source for the `product-decision-agent` skill - Chinese-first product judgment across prioritization, growth, operations, data, delivery, and cross-functional collaboration, with 36 tested scenarios (MIT).

* **[AntonioCardenas/generate-nanobanana](https://github.com/AntonioCardenas/generate-nanobanana) ⭐ 6 | 🐛 0 | 📅 2026-08-04**: Source for the `generate-nanobanana` skill - image and video generation via Google's Gemini media models (Nano Banana 2 Lite/Standard/Pro, Gemini Omni Flash) with cost-approval gates before paid runs, real reference-image support, and a prompt/seed log beside every output (MIT).

* **[huyanxius/logo-to-stickers](https://github.com/huyanxius/logo-to-stickers) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-10-20**: MIT source for `logo-to-stickers` — brand marks become consistent paper-sticker characters with small visual stories, reference roles and fifteen real examples.

* **[FlowLLM-AI/AxonX](https://github.com/FlowLLM-AI/AxonX) ⭐ 5 | 🐛 1 | 🌐 Python | 📅 2026-10-29**: Apache-2.0 source for `axonx` — quantitative research plugin development, task execution, and artifact/lineage inspection through CLI and MCP.

* **[chenli-yy/entropy-box-public](https://github.com/chenli-yy/entropy-box-public) ⭐ 5 | 🐛 0 | 🌐 HTML | 📅 2026-09-03**: Source for the `entropy-box` skill - grounded embodied-AI research and workflow assembly through Consult, Search, Lookup, Evidence, and the Panorama Graph, with public-service privacy and physical-system safety boundaries (CC BY 4.0).

* **[cruisekkk/trading-ledger](https://github.com/cruisekkk/trading-ledger) ⭐ 5 | 🐛 1 | 📅 2026-07-07**: Source for the `trading-ledger` skill - decision-quality trade journaling that captures entry thesis, plan, and emotion into the user's own Notion database (MIT).

* **[qinghui316/ecl-harness-engineer](https://github.com/qinghui316/ecl-harness-engineer) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-09-02**: Source for the `ecl-harness-engineer` skill - ECL Agent Harness infrastructure for AI coding workflows, repository guidance, change tracking, lint checks, CI gates, and handoff docs (MIT).

* **[SSOJet/skills](https://github.com/ssojet/skills) ⭐ 5 | 🐛 0 | 📅 2026-02-24**: Production-ready SSOJet skills and integration guides for popular frameworks and platforms — Node.js, Next.js, React, Java, .NET Core, Go, iOS, Android, and more. Works seamlessly with SSOJet SAML, OIDC, and enterprise SSO flows. Works with Cursor, Antigravity, Claude Code, and Windsurf.

* **[yehudalevy-collab/polis-protocol](https://github.com/yehudalevy-collab/polis-protocol) ⭐ 5 | 🐛 14 | 🌐 Python | 📅 2026-10-25**: Source for the `polis-protocol` multi-agent coordination skill with capability cards, routing history, and protocol amendments (MIT).

* **[UrRhb/agentflow](https://github.com/UrRhb/agentflow) ⭐ 5 | 🐛 0 | 🌐 Shell | 📅 2026-04-01**: Kanban-driven AI development pipeline for orchestrating multi-worker Claude Code workflows with deterministic quality gates, adversarial review, cost tracking, and crash-proof execution (MIT).

* **[xiehuan123/browser-extension-launch](https://github.com/xiehuan123/browser-extension-launch) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-10-02**: Source for the `browser-extension-launch` skill - end-to-end Chrome extension product design, implementation, real-browser acceptance, packaging, and store-launch workflow (MIT).

* **[connerkward/deterministic-design-skill](https://github.com/connerkward/deterministic-design-skill) ⭐ 4 | 🐛 0 | 🌐 JavaScript | 📅 2026-06-17**: Source for the `deterministic-design` skill - rendered UI layout and usability audits using deterministic measurement plus vision-judged review loops (MIT).

* **[JularDepick/user-thoughts.SKILL](https://github.com/JularDepick/user-thoughts.SKILL) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-07-24**: Source for the `user-thoughts` skill - persistent project idea repository workflows for capturing decisions, tech stack notes, UI/UX rationale, and MDBASE-backed project memory (MIT).

* **[Antheurus/anywrite](https://github.com/Antheurus/anywrite) ⭐ 4 | 🐛 0 | 🌐 TypeScript | 📅 2026-07-31**: Source for the `anywrite` skill - low-context CLI access to Anytype's local API for objects, properties, files, search, chat, and other workspace operations (MIT).

* **[lewiswigmore/agent-skills](https://github.com/lewiswigmore/agent-skills) ⭐ 4 | 🐛 0 | 📅 2026-05-05**: Source for the `vscode-extension-guide-en` skill - VS Code extension development workflows, packaging, Marketplace publishing, TreeView, and webview patterns.

* **[Wolfe-Jam/faf-skills](https://github.com/Wolfe-Jam/faf-skills) ⭐ 4 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-29**: AI-context and project DNA skills — .faf format management, AI-readiness scoring, bi-sync, MCP server building, and championship-grade testing (7 skills, MIT).

* **[tobemagic/deepseek-harness-bluebook](https://github.com/tobemagic/deepseek-harness-bluebook) ⭐ 4 | 🐛 0 | 🌐 HTML | 📅 2026-10-26**: Source for `bluebook-writing`.

* **[yumaheymans/carejobs-mcp](https://github.com/yumaheymans/carejobs-mcp) ⭐ 3 | 🐛 0 | 📅 2026-10-18**: MIT source for the `healthcare-job-search` skill - US healthcare job and posted-pay lookup for nursing, CNA, allied health, therapy, imaging, pharmacy and physician roles through CareJobs.Now's free read-only MCP server or public CC BY 4.0 JSON endpoints.

* **[supernovae-st/nika-agents](https://github.com/supernovae-st/nika-agents) ⭐ 3 | 🐛 1 | 🌐 Python | 📅 2026-10-28**: Official upstream source for the `nika` skill and its deterministic, budget-aware AI workflow runner (MIT skill content; AGPL-3.0 engine).

* **[connerkward/macos-screen-recorder-system-audio](https://github.com/connerkward/macos-screen-recorder-system-audio) ⭐ 3 | 🐛 0 | 🌐 Swift | 📅 2026-08-17**: Source for the `macos-screen-recorder` skill - macOS ScreenCaptureKit recording with system audio, CLI workflows, permission handling, and export guidance (MIT).

* **[connerkward/web-media-getter-skill](https://github.com/connerkward/web-media-getter-skill) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2026-06-17**: Source for the `web-media-getter` skill - unified search across free image, video, and GIF APIs with license-aware media selection guidance (MIT).

* **[2slides/slides-generation-2slides-skills](https://github.com/2slides/slides-generation-2slides-skills) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2026-02-12**: Source for the `2slides-ppt-generator` skill - AI presentation generation, PDF deck creation, narration, theme search, and slide export workflows using the 2slides API (MIT).

* **[Slashworks-biz/idea-os](https://github.com/Slashworks-biz/idea-os) ⭐ 3 | 🐛 0 | 📅 2026-04-18**: Source for the `idea-os` skill - five-phase pipeline (triage -> clarify -> research -> PRD -> plan) that turns raw ideas into a build-ready PRD and execution plan.

* **[Wittlesus/cursorrules-pro](https://github.com/Wittlesus/cursorrules-pro) ⭐ 3 | 🐛 0 | 🌐 Shell | 📅 2026-02-21**: Professional .cursorrules configurations for 8 frameworks - Next.js, React, Python, Go, Rust, and more. Works with Cursor, Claude Code, and Windsurf.

* **[mishanefedov/skill-issue](https://github.com/mishanefedov/skill-issue) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-06-02**: Source for the `skill-issue` activation-audit skill for grading SKILL.md trigger metadata, prompt matching, and collision clusters (MIT).

* **[christopherlhammer11-ai/tool-use-guardian](https://github.com/christopherlhammer11-ai/tool-use-guardian) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-04-27**: Source for the Tool Use Guardian skill — tool-call reliability wrapper with retries, recovery, and failure classification.

* **[christopherlhammer11-ai/recallmax](https://github.com/christopherlhammer11-ai/recallmax) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-04-27**: Source for the RecallMax skill — long-context memory, summarization, and conversation compression for agents.

* **[CodeShuX/tokenwise](https://github.com/CodeShuX/tokenwise) ⭐ 3 | 🐛 0 | 🌐 HTML | 📅 2026-08-26**: Source for the `tokenwise` skill — measurement-driven Haiku/Sonnet/Opus router for Claude Code with per-task NDJSON logging, A/B test mode, and verified $-saved reports (MIT).

* **[eli-alvarado/us-watchlist-alerts](https://github.com/eli-alvarado/us-watchlist-alerts) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2026-10-29**: Source for `us-watchlist-alerts`.

* **[Reak-Z/mcd-secret-menu-lab](https://github.com/Reak-Z/mcd-secret-menu-lab) ⭐ 2 | 🐛 7 | 🌐 Python | 📅 2026-10-30**: MIT community recipe-planning workflow for McDonald's China using an authorized MCP connection and explicit account-action boundaries.

* **[stas4000/what-could-break](https://github.com/stas4000/what-could-break) ⭐ 2 | 🐛 0 | 📅 2026-10-06**: MIT source for the `what-could-break` skill - find what a change breaks outside its own diff and prove the one fact that makes it safe by running real code. Includes material adapted from pstack by Lauren Tan (MIT).

* **[stas4000/tastegate](https://github.com/stas4000/tastegate) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-10-02**: MIT source for the `tastegate` skill - pick a design direction, build on a craft floor, then render the page in headless Chromium at phone and desktop width and fail on overlap, sideways scroll, low contrast and AI-slop defaults. Direction rules derive from taste-skill (MIT) and the craft floor from impeccable (Apache-2.0).

* **[wwewtech/anti-slop-design](https://github.com/wwewtech/anti-slop-design) ⭐ 2 | 🐛 0 | 📅 2026-10-21**: Source for the `anti-slop-design` skill - anti-AI-slop UI/UX engineering with token archetypes and a seven-axis quality gate (MIT).

* **[wwewtech/esl-price-sync](https://github.com/wwewtech/esl-price-sync) ⭐ 2 | 🐛 0 | 📅 2026-10-21**: Source for the `esl-price-sync` skill — community guidance and examples under MIT.

* **[70v-Yoyo/md2video-audio-skill](https://github.com/70v-Yoyo/md2video-audio-skill) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-09-22**: Apache-2.0 community source for `md2video-audio`, converting Markdown into narrated MP4 video with synchronized slides and narration.

* **[Ghost011118/project-state-governor](https://github.com/Ghost011118/project-state-governor) ⭐ 2 | 🐛 2 | 📅 2026-08-25**: Source for the `project-state-governor` skill - evidence-backed canonical project state across sessions, branches, reviews, and research cycles (Apache-2.0).

* **[JanYork/using-lwc](https://github.com/JanYork/using-lwc) ⭐ 2 | 🐛 0 | 🌐 Shell | 📅 2026-08-14**: Source for the `using-lwc` skill - durable, source-grounded project memory with independently verified document and code graphs (Apache-2.0).

* **[0xsarwagya/ontoly](https://github.com/0xsarwagya/ontoly) ⭐ 2 | 🐛 2 | 🌐 TypeScript | 📅 2026-10-14**: Source for the `ontoly-software-graph` skill - deterministic TypeScript software graphs, MCP-backed architecture review, request tracing, impact analysis, and dependency analysis (MIT).

* **[chaunsin/agent-skills](https://github.com/chaunsin/agent-skills) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-10-30**: Source for the `pre-release-review` and `drizzle-migration-conflict` skills - deploy-readiness audits and Drizzle Kit migration-conflict workflows (Apache-2.0).

* **[takeaseatventure/devops-skills](https://github.com/takeaseatventure/devops-skills) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2026-07-27**: Source for the `cron-doctor` skill - cron expression diagnosis, validation, trap detection, and zero-dependency schedule analysis tooling (MIT).

* **[Genefold/arrowspace-skills](https://github.com/Genefold/arrowspace-skills) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-10-15**: Source for the `arrowspace` skill - spectral vector search using graph Laplacian eigenstructure for structurally aware retrieval (Apache-2.0).

* **[tsilverberg/webapp-uat](https://github.com/tsilverberg/webapp-uat) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2026-03-15**: Full browser UAT skill — Playwright testing with console/network error capture, WCAG 2.2 AA accessibility checks, i18n validation, responsive testing, and P0-P3 bug triage. Read-only by default, works with React, Vue, Angular, Ionic, Next.js.

* **[fruitwyatt/puzzle-activity-planner](https://github.com/fruitwyatt/puzzle-activity-planner) ⭐ 2 | 🐛 0 | 📅 2026-04-11**: Puzzle activity-planning skill for classrooms, parties, and events with generator-link workflows.

* **[Sharrmavishal/operating-kit](https://github.com/Sharrmavishal/operating-kit) ⭐ 2 | 🐛 0 | 📅 2026-07-07**: Source for the `pre-ship-gate` skill - a pre-deploy gate that walks the silent failure modes (migrations, feature flags, stale build cache, release pointer, staged rollout, missing env) and verifies the live revision instead of trusting deploy output (MIT).

* **[jiawood2006/hermes-skills](https://github.com/jiawood2006/hermes-skills) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-10-30**: MIT source for the `de-ai-writer` skill - Chinese AI-smell detection and de-AI rewriting from a 35-pattern catalog, with a deterministic AI-smell index and a deletion-first edit procedure that preserves every source fact.

* **[keviniscool-boy/onboard](https://github.com/keviniscool-boy/onboard) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-26**: Source for `onboard`.

* **[wu736139669/goal-instruction-writer](https://github.com/wu736139669/goal-instruction-writer) ⭐ 2 | 🐛 0 | 🌐 HTML | 📅 2026-10-23**: Source for `goal-instruction-writer`.

* **[openhook-dev/openhook-inbox](https://github.com/openhook-dev/openhook-inbox) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-10-29**: MIT source for the `openhook` skill: disposable callback inboxes, event inspection and cursor-based waiting for authorized integration tests.

* **[moooai/takeout-coupon](https://github.com/moooai/takeout-coupon) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-10-16**: MIT source for the `takeout-coupon` skill - Meituan, Ele.me/Taobao Shangou and JD Waimai hidden coupon feeds with verbatim taokouling codes and QR/H5 claim pages.

* **[AshenJyy/antigravity-browser-bridge](https://github.com/AshenJyy/antigravity-browser-bridge) ⭐ 1 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-28**: Source for the Browser Bridge guide for authorized Edge/Chrome automation using a separately installed local extension and daemon (Apache-2.0).

* **[alapha888/agent-skills-en](https://github.com/alapha888/agent-skills-en) ⭐ 1 | 🐛 0 | 📅 2026-10-22**: MIT source for `deep-research-framework`, `five-axis-code-review`, `git-commit-message`, `meeting-notes`, and `tech-writing-proofread` — concise English workflows for research reports, code review, commit messages, meeting minutes, and technical proofreading.

* **[Natchannnn/repository-engineering-skills](https://github.com/Natchannnn/repository-engineering-skills) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-09-30**: MIT source for `repo-foundation` and `repo-native-refactor` — repository-native implementation, contract-aware migrations, evidence-based review, and bounded cleanup.

* **[wwewtech/chatexport-need-miner](https://github.com/wwewtech/chatexport-need-miner) ⭐ 1 | 🐛 0 | 📅 2026-10-21**: Source for the `chatexport-need-miner` skill — community guidance and examples under MIT.

* **[wwewtech/dali-short-address-commissioner](https://github.com/wwewtech/dali-short-address-commissioner) ⭐ 1 | 🐛 0 | 📅 2026-10-21**: Source for the `dali-short-address-commissioner` skill — community guidance and examples under MIT.

* **[wwewtech/eol-resistor-calculator](https://github.com/wwewtech/eol-resistor-calculator) ⭐ 1 | 🐛 0 | 📅 2026-10-21**: Source for the `eol-resistor-calculator` skill — community guidance and examples under MIT.

* **[wwewtech/marlin-bed-leveling](https://github.com/wwewtech/marlin-bed-leveling) ⭐ 1 | 🐛 0 | 📅 2026-10-21**: Source for the `marlin-bed-leveling` skill — community guidance and examples under MIT.

* **[wwewtech/oneroster-csv-validator](https://github.com/wwewtech/oneroster-csv-validator) ⭐ 1 | 🐛 0 | 📅 2026-10-21**: Source for the `oneroster-csv-validator` skill — community guidance and examples under MIT.

* **[Junaid-PK/laravel-development-workflow](https://github.com/Junaid-PK/laravel-development-workflow) ⭐ 1 | 🐛 0 | 📅 2026-09-02**: Source for the `laravel-development-workflow` skill - root-cause Laravel bug fixes and repository-native feature work with regression coverage and risk-based verification (MIT).

* **[alexprivalov/boost-asio-skill](https://github.com/alexprivalov/boost-asio-skill) ⭐ 1 | 🐛 0 | 📅 2026-09-30**: Source for the `boost-asio-pro` skill - version-aware async C++ networking with Boost.Asio and standalone Asio across coroutine, callback, and classic `io_service` styles (MIT).

* **[5dive-ai/skills](https://github.com/5dive-ai/skills) ⭐ 1 | 🐛 0 | 🌐 Shell | 📅 2026-10-28**: Source for the `compile-knowledge` skill - durable, atomic, interlinked knowledge stores with explicit hygiene, provenance, expiry, and secret-handling boundaries (MIT).

* **[saudademjj/luopan](https://github.com/saudademjj/luopan) ⭐ 1 | 🐛 0 | 📅 2026-08-10**: Source for the `travel-planner` skill - Chinese-first travel itinerary planning with mandatory budget confirmation, source-traceable facts, workload-aware daily pacing, and rule self-checks (MIT).

* **[OJPalenzuela/agents-generator](https://github.com/OJPalenzuela/agents-generator) ⭐ 1 | 🐛 0 | 📅 2026-08-03**: Source for the `agents-generator` skill - project-specific `AGENTS.md` and companion rule generation with package-manager detection, monorepo handling, dry-run/update modes, backups, and validated commands (MIT).

* **[agentbody/skills](https://github.com/agentbody/skills) ⭐ 1 | 🐛 1 | 🌐 Python | 📅 2026-08-27**: Source for the `people-data` skill - LinkedIn and YouTube professional-profile and public business-contact research via the Agent Body MCP server (MIT).

* **[yylo-dev/yylo-skills](https://github.com/yylo-dev/yylo-skills) ⭐ 1 | 🐛 6 | 🌐 JavaScript | 📅 2026-10-17**: Source for 7 YYLO skills (`ledger-tasks-yylo`, `plan-ledger-tasks-yylo`, `ralph-loop-yylo`, `understand-project-yylo`, `wiki-yylo`, `workflow-yylo`, `artifact-yylo`) - repo-resident Kanban/task ledger, PDR planning, validated single-task execution loop, and wiki/workflow/artifact records with fail-closed Ledger boundaries (MIT, docs-only — `scripts/kanban.sh` runtime not bundled).

* **[maleksaadi0109/hyprfedora](https://github.com/maleksaadi0109/hyprfedora) ⭐ 1 | 🐛 0 | 🌐 Shell | 📅 2026-07-26**: Source for the `fedora-hyprland-installer` skill - GPU-aware Fedora Hyprland installation, configuration, verification, repair, and removal workflows (MIT).

* **[merc1305/findMate](https://github.com/merc1305/findMate) ⭐ 1 | 🐛 4 | 🌐 Python | 📅 2026-07-28**: Source for the `find-complementary-founders` skill - private-first own-owner assessment, approved expiring profiles, and evidence-backed human founder matching (MIT).

* **[hafiz-actyte/idea-autopsy](https://github.com/hafiz-actyte/idea-autopsy) ⭐ 1 | 🐛 0 | 📅 2026-07-10**: Source for the `idea-autopsy` skill - business-idea validation that hunts the one sentence that kills an idea before you build: kill-list check, five hard filters, free-AI one-prompt test, and live ad-market verification (MIT).

* **[takeaseatventure/sql-sentinel](https://github.com/takeaseatventure/sql-sentinel) ⭐ 1 | 🐛 1 | 🌐 JavaScript | 📅 2026-08-02**: Source for the `sql-sentinel` skill - SQL warehouse cost and performance anti-pattern audits across BigQuery, Snowflake, Redshift, and Postgres (MIT).

* **[connerkward/lookdev-auto-skill](https://github.com/connerkward/lookdev-auto-skill) ⭐ 1 | 🐛 0 | 📅 2026-06-17**: Source for the `lookdev-auto` skill - automated visual tuning loops where a vision or video model rates rendered variants and suggests improvements (MIT).

* **[connerkward/lookdev-studio-skill](https://github.com/connerkward/lookdev-studio-skill) ⭐ 1 | 🐛 0 | 📅 2026-06-17**: Source for the `lookdev` skill - human-in-the-loop visual and prose tuning through rendered variants, sliders, swatches, inline edits, and selection-driven refinement (MIT).

* **[mskadu/opencode-agent-skills](https://github.com/mskadu/opencode-agent-skills) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-06-06**: Source for opencode behavior, permission, skill-suggestion, and smart Git automation skills.

* **[mycelos-ai/bumblebee-skill](https://github.com/mycelos-ai/bumblebee-skill) ⭐ 1 | 🐛 0 | 🌐 Shell | 📅 2026-05-27**: Source for the `bumblebee` skill - multi-agent implementation workflows with repeatable planning, coding, review, and verification loops (MIT).

* **[tellmefrankie/news-engine](https://github.com/tellmefrankie/news-engine) ⭐ 1 | 🐛 6 | 🌐 TypeScript | 📅 2026-05-13**: Source for the `news-sentiment-engine` skill - news ingestion, sentiment analysis, and market/news intelligence workflows (MIT).

* **[Kench001/antigravity-awesome-skills](https://github.com/Kench001/antigravity-awesome-skills) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-05-03**: Source for the `recursive-context-pruning-token-budgeting` skill - context pruning, token budgeting, and long-session compression guidance (MIT).

* **[CodeShuX/mockhunter](https://github.com/CodeShuX/mockhunter) ⭐ 1 | 🐛 1 | 📅 2026-05-11**: Source for the `mock-hunter` skill - Playwright-based live-page audits that classify visible values as real, mock, LLM-generated, hardcoded, broken, or unknown (MIT).

* **[274326424/video-content-extractor](https://github.com/274326424/video-content-extractor) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-06-06**: Source for the `video-content-extractor` skill - FFmpeg and Tesseract OCR workflows for extracting timestamped screen text and structured Markdown reports from MP4 videos (MIT).

* **[metrox-eth/quit-sponsor](https://github.com/metrox-eth/quit-sponsor) ⭐ 1 | 🐛 0 | 📅 2026-07-14**: Source for the `quit-sponsor` skill - evidence-based quit-smoking sponsorship for agents with persistent memory: 44-source cited protocols, sponsor decision tree, three-clause contract, wave protocol, slip attribution coaching, and a timestamped logbook (MIT).

* **[ch040602/mdpr-skill](https://github.com/ch040602/mdpr-skill) ⭐ 1 | 🐛 7 | 🌐 HTML | 📅 2026-09-28**: Source for the `mdpr-skill` skill - Codex-assisted MDPR presentation review, semantic hints, visual checks, theme candidates, and deterministic renderer boundaries (MIT).

* **[MojoAuth/skills](https://github.com/MojoAuth/skills) ⭐ 1 | 🐛 0 | 📅 2026-02-25**: Production-ready MojoAuth guides and examples for popular frameworks like Node.js, Next.js, React, Java, .NET Core, Go, iOS, and Android.

* **[xwmxcz/papers-skill](https://github.com/xwmxcz/papers-skill) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-06-11**: Source for the `papers-skill` skill — academic research workflows over Semantic Scholar (200M+ papers) and arXiv, with citation lookup, arXiv PDF download, and PyMuPDF text extraction via a bundled Python CLI (MIT).

* **[kimtth/agent-pptify-kit](https://github.com/kimtth/agent-pptify-kit) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-09-10**: Source for the `pptx-deck-creation` skill - editable, production-ready PowerPoint deck creation with narrative planning, explicit layouts, asset guidance, and quality checks (MIT).

* **[mksd0398/nitrogen](https://github.com/mksd0398/nitrogen) ⭐ 1 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-25**: Source for `shopify-firebase-app`.

* **[theguysaccount/syncbook-chatgpt](https://github.com/theguysaccount/syncbook-chatgpt) ⭐ 1 | 🐛 1 | 📅 2026-10-25**: Source for `syncbook-discovery`.

* **[timini/agentic-verification](https://github.com/timini/agentic-verification) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-16**: MIT source for the `agentic-verify` and `agentic-test-audit` skills - check a Python change by running every mutant of the changed lines and writing tests until they catch them, and audit a pytest suite for gaps, flaky and slow tests, and removal candidates checked on held-out mutants.

* **[UmarSiddiqui/obsess](https://github.com/UmarSiddiqui/obsess) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-29**: MIT source for the `obsess` skill - a bounded perfectionist loop for one target that keeps the best evidence-backed attempt and stops on an attempt or time budget.

* **[moooai/trip-coupon](https://github.com/moooai/trip-coupon) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-16**: MIT source for the `trip-coupon` skill - Didi ride-hailing and hotel coupon feeds with verbatim codes and claim pages.

* **[moooai/movie-coupon](https://github.com/moooai/movie-coupon) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-16**: MIT source for the `movie-coupon` skill - movie-ticket discount feeds for Chinese cinema platforms with verbatim codes and claim links.

* **[moooai/parcel-coupon](https://github.com/moooai/parcel-coupon) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-16**: MIT source for the `parcel-coupon` skill - courier and parcel-delivery coupon feeds with verbatim codes and claim pages.

* **[moooai/obtain-coupons-all-in-one](https://github.com/moooai/obtain-coupons-all-in-one) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-16**: MIT source for the `obtain-coupons-all-in-one` skill - one aggregated coupon feed across the four categories above.

* **[Kadajett/cockney](https://github.com/Kadajett/cockney) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-12**: MIT source for the `cockney` skill - terse Cockney-voiced replies and the smallest correct change (reuse, stdlib before dependencies, no speculative abstraction), switching to plain English for security and destructive-action warnings.

* **[estevecastells/awesome-copilot](https://github.com/estevecastells/awesome-copilot) ⭐ 0 | 🐛 0 | 📅 2026-10-12**: MIT source for the `invokely-statistics` skill - find official statistical figures, series, comparisons and place rankings through the Invokely MCP server, and report each value with its period, unit and source citation. The originating contribution is open and unmerged upstream.

* **[stefanautomateed/shipvela-codex](https://github.com/stefanautomateed/shipvela-codex) ⭐ 0 | 🐛 1 | 📅 2026-10-05**: MIT source for `shipvela-publish` — owner-confirmed website publishing and exact deployment tracking through an already connected Shipvela account. The hosted service is proprietary and plan-limited.

* **[mdagnolops/1human-reels](https://github.com/mdagnolops/1human-reels) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-10**: MIT source for the `agent-reels` skill - find credited animation and video references on 1human and consult a private library shared by a human and their creative agent; registration, saves, likes, comments and publication are state-changing and require prior owner authorization.

* **[ASCIT31/darkmoon-mcp-server](https://github.com/ASCIT31/darkmoon-mcp-server) ⭐ 0 | 🐛 5 | 🌐 TypeScript | 📅 2026-10-19**: GPL-3.0 source for the `darkmoon-pentest` skill — authorized autonomous pentest runs, status polling and findings triage on a self-hosted Darkmoon Pro instance through its MCP server.

* **[alapha888/session-handoff-kit](https://github.com/alapha888/session-handoff-kit) ⭐ 0 | 🐛 0 | 📅 2026-10-22**: MIT source for the `session-handoff` skill — structured handoff artifact for the next session, for use when context approaches capacity, before /clear or /compact, when switching tasks, or when ending a coding session.

* **[tomelias10/mcp-drift-check](https://github.com/tomelias10/mcp-drift-check) ⭐ 0 | 🐛 1 | 🌐 Python | 📅 2026-10-21**: MIT source for the `mcp-dependency-drift-audit` skill — zero-execution review of mutable npm/npx package references in MCP configuration, with a manual static fallback and CI/SARIF guidance.

* **[work0r-ai/agent-kit](https://github.com/work0r-ai/agent-kit) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-07-04**: Source for the `workorai` skill — agent kit workflows (MIT).

* **[twoicewoo/awesome-copilot](https://github.com/twoicewoo/awesome-copilot/tree/886bf799bb05501bfd1afa7aae9cc5a77dedb03e/skills/break-ai-fix-loops) ⭐ 0 | 🐛 0 | 📅 2026-09-04**: Pinned MIT source for the `break-ai-fix-loops` skill - bounded AI repair loops with stable failure fingerprints, real-path proof, negative controls, and rollback verification (MIT).

* **[Sketchjar/stipple-agent-skills](https://github.com/Sketchjar/stipple-agent-skills) ⭐ 0 | 🐛 0 | 📅 2026-09-03**: Source for seven Stipple-backed document trust skills covering document forensics, identity-pack gaps, grounded extraction, citation checks, AI-text triage, adverse-media review, and AU/NZ tender matching, with explicit hosted-data and human-review boundaries (Apache-2.0).

* **[263311487-ux/falsify](https://github.com/263311487-ux/falsify) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-28**: Source for the `falsify` skill - a scientific reasoning protocol for explicit hypotheses, adversarial checks, evidence grading, and calibrated conclusions (MIT).

* **[kotobuki09/instructree](https://github.com/kotobuki09/instructree) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-26**: Source for the `instructree` skill - local instruction-scope mapping, metadata and link validation, recursive Copilot import audits, and SARIF reports (MIT).

* **[harshmaur/apify-reddit-scraper-skill](https://github.com/harshmaur/apify-reddit-scraper-skill) ⭐ 0 | 🐛 0 | 📅 2026-10-20**: Source for the `apify-reddit-scraper` skill - Reddit posts, comments, subreddits and user profiles as structured data through the `harshmaur/reddit-scraper` Apify Actor, with no Reddit API key, cost estimates before each run and date-window filters (MIT).

* **[Antheurus/sshepherd](https://github.com/Antheurus/sshepherd) ⭐ 0 | 🐛 0 | 🌐 TypeScript | 📅 2026-07-23**: Source for the `sshepherd` skill - credential-isolated SSH operations, service control, logs, configuration changes, Postgres introspection, and declarative deploys through preconfigured aliases (MIT).

* **[zenlee123/routerbase-agent-skills](https://github.com/zenlee123/routerbase-agent-skills) ⭐ 0 | 🐛 0 | 📅 2026-07-05**: Source for the `routerbase-model-gateway` skill — OpenAI-compatible RouterBase model gateway setup, model-routing plans, server-side credential handling, and fallback validation patterns (MIT-0).

* **[thecsdoctor/brendangregg-use-tsa-skill](https://github.com/thecsdoctor/brendangregg-use-tsa-skill) ⭐ 0 | 🐛 1 | 📅 2026-07-28**: Source for the `brendangregg-use-tsa` skill - methodical performance troubleshooting and root-cause analysis with Brendan Gregg's USE and TSA methods, plus evidence-backed RCA and postmortem reporting (MIT).

* **[alfredtech2026/shopify-app-review-brief](https://github.com/alfredtech2026/shopify-app-review-brief) ⭐ 0 | 🐛 0 | 📅 2026-08-05**: Source for the `shopify-review-triage` skill - public-data-only P0–P3 triage of low-star Shopify App Store reviews into a source-linked brief, with an explicit needs-human-read bucket and first-pass vs. human-checked labeling (MIT).

* **[mnemoverse/agent-memory-discipline](https://github.com/mnemoverse/agent-memory-discipline) ⭐ 0 | 🐛 0 | 📅 2026-10-21**: Source for the `agent-memory-discipline` skill, with backend-neutral rules for when an agent recalls from long-term memory before acting and when it saves decisions, corrections and failures afterwards (CC0-1.0).

* **[Search-3D/electron-drive-skill](https://github.com/Search-3D/electron-drive-skill) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-09-25**: Source for the `electron-drive-skill` skill - launching and driving Electron apps under Playwright on a scratch profile (MIT).

* **[codegiveness/kernel-prompt](https://github.com/codegiveness/kernel-prompt) ⭐ 0 | 🐛 0 | 📅 2026-10-12**: MIT source for the `kernel-prompt` skill - harness-neutral prompt design that asks one round of user-only decisions, then returns an improved prompt for another agent without performing the task.

* **[assaylabdesk-sudo/assay-lite](https://github.com/assaylabdesk-sudo/assay-lite) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-21**: Source for `calibrate-first`.

* **[clagoss/claude-code-para-disenadores](https://github.com/clagoss/claude-code-para-disenadores) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-10-29**: Source for `design-token-contrast`.

* **[harshmaur/apify-facebook-ads-library-scraper](https://github.com/harshmaur/apify-facebook-ads-library-scraper) ⭐ 0 | 🐛 0 | 📅 2026-10-20**: Source for `apify-facebook-ads-library-scraper`.

* **[harshmaur/apify-linkedin-jobs-scraper](https://github.com/harshmaur/apify-linkedin-jobs-scraper) ⭐ 0 | 🐛 0 | 📅 2026-10-20**: Source for `apify-linkedin-jobs-scraper`.

* **[harshmaur/apify-tiktok-scraper](https://github.com/harshmaur/apify-tiktok-scraper) ⭐ 0 | 🐛 0 | 📅 2026-10-21**: Source for `apify-tiktok-scraper`.

* **[harshmaur/apify-youtube-transcript-scraper](https://github.com/harshmaur/apify-youtube-transcript-scraper) ⭐ 0 | 🐛 0 | 📅 2026-10-21**: Source for `apify-youtube-transcript-scraper`.

* **[igamingsychov/second-deposit-igaming](https://github.com/igamingsychov/second-deposit-igaming) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-21**: Source for `second-deposit-igaming`.

* **[igamingsychov/watch-igaming](https://github.com/igamingsychov/watch-igaming) ⭐ 0 | 🐛 0 | 🌐 Shell | 📅 2026-10-21**: Source for `watch-igaming`.

* **[kevinmmiddleton/unpaid-intern](https://github.com/kevinmmiddleton/unpaid-intern) ⭐ 0 | 🐛 1 | 🌐 Python | 📅 2026-10-26**: Source for `unpaid-intern`.

* **[noamshorts22-prog/usage-engineer](https://github.com/noamshorts22-prog/usage-engineer) ⭐ 0 | 🐛 0 | 🌐 Python | 📅 2026-10-24**: Source for `usage-engineer`.

* **[paperandbeyond23-gif/restosignals-mcp](https://github.com/paperandbeyond23-gif/restosignals-mcp) ⭐ 0 | 🐛 0 | 📅 2026-10-17**: Source for `restosignals`.

* **[wyattau/memory-handoff-skill](https://github.com/wyattau/memory-handoff-skill) ⭐ 0 | 🐛 0 | 🌐 Shell | 📅 2026-10-25**: Source for `memory-handoff`.

* **[JDDavenport/context-kit](https://github.com/JDDavenport/context-kit)**: Source reference for the `context-kit` skill - local-first Personal Context Artifact setup, installer review, and private context hygiene for Claude Code and adjacent agent workflows.

* **[mturac/recsys-pipeline-architect](https://github.com/mturac/recsys-pipeline-architect)**: Source for the `recsys-pipeline-architect` skill - recommendation, ranking, and feed pipeline architecture using Source, Hydrator, Filter, Scorer, Selector, and SideEffect stages (MIT).

* **[openclaw/skills](https://github.com/openclaw/skills)**: Source for the `daily-gift` skill - relationship-aware creative gift generation with editorial judgment, concept selection, and multi-format rendering.

* **[pumanitro/global-chat](https://github.com/pumanitro/global-chat)**: Source for the Global Chat Agent Discovery skill - cross-protocol discovery of MCP servers and AI agents across multiple registries.

* **[milkomida77/guardian-agent-prompts](https://github.com/milkomida77/guardian-agent-prompts)**: Source for the Multi-Agent Task Orchestrator skill - production-tested delegation patterns, anti-duplication, and quality gates for coordinated agent work.

* **[Elkidogz/technical-change-skill](https://github.com/Elkidogz/technical-change-skill)**: Source for the Technical Change Tracker skill - structured JSON change records, session handoff, and accessible HTML dashboards for coding continuity.

* **[morsechimwai/lemmaly](https://github.com/morsechimwai/lemmaly)**: Source for the `lemmaly`, `mathguard`, `invariant-guard`, and `complexity-cuts` skills — algorithm-first discipline layer that forces AI coding agents to state Big-O, name the data structure, prove termination, and pick the right algorithm before writing the loop. Ships a deterministic CI scanner with 59 rules across 11 languages (Apache-2.0).

* **[whoisabhishekadhikari/lovable-cleanup](https://github.com/whoisabhishekadhikari/lovable-cleanup)**: Source for the `lovable-cleanup` skill — audits and strips Lovable scaffolding from Vite + React projects.

* **[mrprewsh/seo-aeo-engine](https://github.com/mrprewsh/seo-aeo-engine)**: SEO/AEO content-growth system covering keyword research, content clustering, landing pages, blog structure, schema, internal linking, and audit workflows.

* **[nickdesi/ZipAI](https://github.com/nickdesi/ZipAI)**: Source for the `zipai-optimizer` skill — ultra-dense prompt caching, semantic log pruning, AST-based code viewing, minified JSON payloads, and telegraphic output constraints for maximum token savings.

* **[connerlambden/helium-mcp](https://github.com/connerlambden/helium-mcp)**: Source for the `helium-mcp` skill — MCP server for news intelligence, media bias analysis, market data, options pricing, and semantic meme search.

* **[aptratcn/skill-audit](https://github.com/aptratcn/skill-audit)**: Pre-install security audit skill for detecting malicious, overprivileged, or suspicious third-party agent skills before installation (MIT).

* **[Shpigford/skills](https://github.com/Shpigford/skills)**: General-purpose agent skills for common development tasks (MIT).

* **[voidborne-d/humanize-chinese](https://github.com/voidborne-d/humanize-chinese)**: Chinese AI-text detection and humanization toolkit for scoring, rewriting, academic AIGC reduction, and style conversion workflows.

* **[voidborne-d/lambda-lang](https://github.com/voidborne-d/lambda-lang)**: Agent-to-agent coordination language with compact atoms for multi-agent messaging, orchestration, and structured coordination logs.

* **[axelfreeman/marketing-mindset](https://github.com/axelfreeman/marketing-mindset)**: Source for the `marketing-mindset` skill - a marketer's decision framework for early-stage B2B and SaaS work: exchange checks, live-competitor benchmarking, pre-declared test volume floors, and channel kill rules (MIT).

</details>

<details>
<summary><strong>Inspirations & Additional Sources</strong></summary>

### Inspirations

* **[f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) ⭐ 175,146 | 🐛 80 | 🌐 HTML | 📅 2026-10-30**: Inspiration for the Prompt Library.
* **[leonardomso/33-js-concepts](https://github.com/leonardomso/33-js-concepts) ⭐ 66,530 | 🐛 10 | 🌐 JavaScript | 📅 2026-10-21**: Inspiration for JavaScript Mastery.

### Additional Sources

* **[agent-cards/skill](https://github.com/agent-cards/skill) ⭐ 14 | 🐛 1 | 📅 2026-10-24**: Manage prepaid virtual Visa cards for AI agents. Create cards, check balances, view credentials, close cards, and get support via MCP tools.

</details>

Catalog dashboard search, filters, shortlist, and discovery were originally contributed by [@zinzied](https://github.com/zinzied) in [#1111](https://github.com/sickn33/agentic-awesome-skills/pull/1111), then repaired and integrated through [#1118](https://github.com/sickn33/agentic-awesome-skills/pull/1118) under the repository's fork-safety policy.

## Top Contributors

Thanks to everyone who has helped build this project—especially the contributors below.

<table>
<tr>
<td valign="top" width="50%">

### Most Commits

Contributors ranked by the number of commits.

|  # | Contributor                                                                                                                                                                                                                                            | Commits |
| -: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------: |
|  1 | <a href="https://github.com/WHOISABHISHEKADHIKARI"><img src="https://github.com/WHOISABHISHEKADHIKARI.png?size=48" width="32" height="32" alt="" /></a> [@WHOISABHISHEKADHIKARI](https://github.com/WHOISABHISHEKADHIKARI)                             |      51 |
|  2 | <a href="https://github.com/munir-abbasi"><img src="https://github.com/munir-abbasi.png?size=48" width="32" height="32" alt="" /></a> [@munir-abbasi](https://github.com/munir-abbasi)                                                                 |      34 |
|  3 | <a href="https://github.com/Mohammad-Faiz-Cloud-Engineer"><img src="https://github.com/Mohammad-Faiz-Cloud-Engineer.png?size=48" width="32" height="32" alt="" /></a> [@Mohammad-Faiz-Cloud-Engineer](https://github.com/Mohammad-Faiz-Cloud-Engineer) |      33 |
|  4 | <a href="https://github.com/zinzied"><img src="https://github.com/zinzied.png?size=48" width="32" height="32" alt="" /></a> [@zinzied](https://github.com/zinzied)                                                                                     |      24 |
|  5 | <a href="https://github.com/beatra-ai"><img src="https://github.com/beatra-ai.png?size=48" width="32" height="32" alt="" /></a> [@beatra-ai](https://github.com/beatra-ai)                                                                             |      19 |
|  6 | <a href="https://github.com/Prince-1652"><img src="https://github.com/Prince-1652.png?size=48" width="32" height="32" alt="" /></a> [@Prince-1652](https://github.com/Prince-1652)                                                                     |      17 |
|  7 | <a href="https://github.com/ssumanbiswas"><img src="https://github.com/ssumanbiswas.png?size=48" width="32" height="32" alt="" /></a> [@ssumanbiswas](https://github.com/ssumanbiswas)                                                                 |      15 |
|  8 | <a href="https://github.com/FrancoStino"><img src="https://github.com/FrancoStino.png?size=48" width="32" height="32" alt="" /></a> [@FrancoStino](https://github.com/FrancoStino)                                                                     |      13 |
|  9 | <a href="https://github.com/waynehamadi"><img src="https://github.com/waynehamadi.png?size=48" width="32" height="32" alt="" /></a> [@waynehamadi](https://github.com/waynehamadi)                                                                     |      12 |
| 10 | <a href="https://github.com/sx4im"><img src="https://github.com/sx4im.png?size=48" width="32" height="32" alt="" /></a> [@sx4im](https://github.com/sx4im)                                                                                             |      10 |

</td>
<td valign="top" width="50%">

### Most Skills Added

Contributors ranked by the number of skills they added.

|  # | Contributor                                                                                                                                                                                                                | Skills added |
| -: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -----------: |
|  1 | <a href="https://github.com/FrancoStino"><img src="https://github.com/FrancoStino.png?size=48" width="32" height="32" alt="" /></a> [@FrancoStino](https://github.com/FrancoStino)                                         |          336 |
|  2 | <a href="https://github.com/WHOISABHISHEKADHIKARI"><img src="https://github.com/WHOISABHISHEKADHIKARI.png?size=48" width="32" height="32" alt="" /></a> [@WHOISABHISHEKADHIKARI](https://github.com/WHOISABHISHEKADHIKARI) |          231 |
|  3 | <a href="https://github.com/Prince-1652"><img src="https://github.com/Prince-1652.png?size=48" width="32" height="32" alt="" /></a> [@Prince-1652](https://github.com/Prince-1652)                                         |           91 |
|  4 | <a href="https://github.com/sohamganatra"><img src="https://github.com/sohamganatra.png?size=48" width="32" height="32" alt="" /></a> [@sohamganatra](https://github.com/sohamganatra)                                     |           78 |
|  5 | <a href="https://github.com/ProgramadorBrasil"><img src="https://github.com/ProgramadorBrasil.png?size=48" width="32" height="32" alt="" /></a> [@ProgramadorBrasil](https://github.com/ProgramadorBrasil)                 |           52 |
|  6 | <a href="https://github.com/nikolasdehor"><img src="https://github.com/nikolasdehor.png?size=48" width="32" height="32" alt="" /></a> [@nikolasdehor](https://github.com/nikolasdehor)                                     |           35 |
|  7 | <a href="https://github.com/beatra-ai"><img src="https://github.com/beatra-ai.png?size=48" width="32" height="32" alt="" /></a> [@beatra-ai](https://github.com/beatra-ai)                                                 |           23 |
|  8 | <a href="https://github.com/Ranjeet2063"><img src="https://github.com/Ranjeet2063.png?size=48" width="32" height="32" alt="" /></a> [@Ranjeet2063](https://github.com/Ranjeet2063)                                         |           20 |
|  9 | <a href="https://github.com/MMEHDI0606"><img src="https://github.com/MMEHDI0606.png?size=48" width="32" height="32" alt="" /></a> [@MMEHDI0606](https://github.com/MMEHDI0606)                                             |           20 |
| 10 | <a href="https://github.com/ShianMike"><img src="https://github.com/ShianMike.png?size=48" width="32" height="32" alt="" /></a> [@ShianMike](https://github.com/ShianMike)                                                 |           13 |

</td>
</tr>
</table>

## Repo Contributors

<a href="https://github.com/sickn33/agentic-awesome-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=sickn33/agentic-awesome-skills&max=2000" alt="Repository contributors" />
</a>

Made with [contrib.rocks](https://contrib.rocks). *(Image may be cached; [view live contributors](https://github.com/sickn33/agentic-awesome-skills/graphs/contributors) on GitHub.)*

We officially thank the following contributors for their help in making this repository awesome!

## Star History

<a href="https://www.star-history.com/sickn33/agentic-awesome-skills">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/badge?repo=sickn33/agentic-awesome-skills&amp;type=rank&amp;theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/badge?repo=sickn33/agentic-awesome-skills&amp;type=rank" />
    <img alt="Agentic Awesome Skills global rank on Star History" src="https://api.star-history.com/badge?repo=sickn33/agentic-awesome-skills&amp;type=rank" />
  </picture>
</a>

<a href="https://www.star-history.com/?repos=sickn33%2Fagentic-awesome-skills&amp;type=date&amp;legend=top-left">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/chart?repos=sickn33/agentic-awesome-skills&amp;type=date&amp;theme=dark&amp;legend=top-left" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/chart?repos=sickn33/agentic-awesome-skills&amp;type=date&amp;legend=top-left" />
    <img alt="GitHub star growth over time for Agentic Awesome Skills" src="https://api.star-history.com/chart?repos=sickn33/agentic-awesome-skills&amp;type=date&amp;legend=top-left" />
  </picture>
</a>

[View the live Star History chart](https://www.star-history.com/?repos=sickn33%2Fagentic-awesome-skills\&type=date\&legend=top-left).

If Agentic Awesome Skills has been useful, consider ⭐ starring the repo!

<!-- GitHub Topics (for maintainers): claude-code, gemini-cli, codex-cli, antigravity, cursor, github-copilot, opencode, agentic-skills, ai-coding, llm-tools, ai-agents, autonomous-coding, mcp, ai-developer-tools, ai-pair-programming, vibe-coding, skill, skills, SKILL.md, rules.md, CLAUDE.md, GEMINI.md, CURSOR.md -->

## License

Original code and tooling are licensed under the MIT License. See [LICENSE](LICENSE).

Original documentation and other non-code written content are licensed under [CC BY 4.0](LICENSE-CONTENT), unless a more specific upstream notice says otherwise. See [docs/sources/sources.md](docs/sources/sources.md) for attributions and third-party license details.

***

### Consolidated plugin packs

The focused offer unifies overlapping historical bundles with the AAS packs. Use the [plugin migration guide](docs/users/plugin-migration.md) to find replacements. Existing installations require a manual switch after verifying the destination; activation aliases do not create duplicate marketplace plugins. Changes on main become available through the next published release.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-10-30._
