<!-- registry-sync: version=16.7.0; skills=2111; stars=45955; updated_at=2026-09-04T09:06:54+00:00 -->

# AAS Core — Agentic Awesome Skills with stars

> **Find reusable instructions for your project, inspect their complete files, and keep an exact skill set you can review and reuse.**

**Current release: V16.7.0.** This release includes AAS Core for complete local catalog search, agent-owned selection, manifest validation, planning, and diagnosis. Apply and recovery remain experimental and outside the supported preview path.

Codex or Claude inspects your project and chooses exact skills from the complete local AAS catalog. AAS Core does not rank or recommend them: its read-only `compose_stack` tool validates the agent-owned selection in memory, and a client or the `aas` CLI can persist it as `aas-stack.json` and produce an immutable plan before any target change.

**[Read the AAS Core preview guide →](https://github.com/sickn33/agentic-awesome-skills/blob/v16.7.0/docs/users/aas-core.md) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05**

This README tracks `main`. Changes under [Unreleased](CHANGELOG.md#unreleased), including complete bundle inspection, Workbench evidence import and sparse installer retrieval, require a subsequent release; the linked versioned guide describes the published package.

```text
Project
  -> inspected by Codex or Claude (not by AAS)
  -> agent searches and reads the complete local catalog
  -> AAS MCP (local stdio, read-only)
  -> Codex or Claude chooses exact skill IDs
  -> compose_stack validates the selection in memory (read-only)
  -> client or AAS CLI persists aas-stack.json and optional evidence
  -> AAS CLI validate + immutable plan preview
  -> human review (optionally in Workbench)
```

The reusable `SKILL.md` playbooks, specialized plugins, bundles, workflows, and direct installers remain important. They are the content, curation, distribution, and compatibility layers around AAS Core—not competing primary products.

This is an independent community project. It is not affiliated with, sponsored by, endorsed by, or authorized by Google. Google, Antigravity, Gemini, and related product names are referenced only to describe compatibility and install targets. The GitHub repository is canonical; the hosted catalog and browser-local Workbench are companion discovery and review surfaces, not a hosted control plane.

[![GitHub stars](https://img.shields.io/badge/⭐%2046%2C000%2B%20Stars-gold?style=for-the-badge)](https://github.com/sickn33/agentic-awesome-skills/stargazers) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05
[![Follow @AASkills\_ on X](https://img.shields.io/badge/Follow-%40AASkills__-black?style=for-the-badge\&logo=x)](https://x.com/AASkills_)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Anthropic-purple)](https://claude.ai)
[![Cursor](https://img.shields.io/badge/Cursor-AI%20IDE-orange)](https://cursor.sh)
[![Codex CLI](https://img.shields.io/badge/Codex%20CLI-OpenAI-green)](https://github.com/openai/codex) ⭐ 121,605 | 🐛 15,321 | 🌐 Rust | 📅 2026-09-05
[![Autohand Code](https://img.shields.io/badge/Autohand%20Code-CLI-blue)](https://github.com/autohandai/code-cli) ⭐ 184 | 🐛 109 | 🌐 TypeScript | 📅 2026-09-02
[![Gemini CLI](https://img.shields.io/badge/Gemini%20CLI-Google-blue)](https://github.com/google-gemini/gemini-cli) ⭐ 106,819 | 🐛 845 | 🌐 TypeScript | 📅 2026-09-05
[![Latest Release](https://img.shields.io/github/v/release/sickn33/agentic-awesome-skills?display_name=tag\&style=for-the-badge)](https://github.com/sickn33/agentic-awesome-skills/releases/latest) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05
[![Direct skill distribution](https://img.shields.io/badge/Direct%20skills-npx%20agentic--awesome--skills-black?style=for-the-badge\&logo=npm)](#installation)
[![Kiro](https://img.shields.io/badge/Kiro-AWS-orange?style=for-the-badge)](https://kiro.dev)
[![Copilot](https://img.shields.io/badge/Copilot-GitHub-lightblue?style=for-the-badge)](https://github.com/features/copilot)
[![OpenCode](https://img.shields.io/badge/OpenCode-CLI-gray?style=for-the-badge)](https://github.com/opencode-ai/opencode) ⚠️ Archived
[![Antigravity](https://img.shields.io/badge/Antigravity-AI%20IDE-red?style=for-the-badge)](https://github.com/sickn33/agentic-awesome-skills) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05

## AAS Core: Agent-First Preview

> **The agent composes. You control. AAS keeps the stack reproducible.**

AAS Core gives the repository one product model:

* **Let the agent choose.** The local MCP offers `search_skills`, `get_skill`, `list_skill_files`, `read_skill_file`, `compose_stack`, `inspect_stack`, and `diff_stack`, plus read-only `export_selection_evidence` and `inspect_selection_evidence`; Core does not rank, recommend, exclude, or hide skills. Bundle files are verified and read as inert text.
* **Guide capability coverage.** MCP session instructions require the agent to evaluate the full project surface—from architecture, domain behavior, data and integrations through testing, security, UX, deployment, and maintenance—then search each applicable capability, compare multiple candidates, cover it with a non-redundant skill or report a catalog gap, and avoid stopping at a minimal shortlist. Core records and validates the resulting selection, but it does not certify semantic completeness.
* **Keep the chosen stack and evidence reviewable.** A client or the CLI can persist `aas-stack.json` and the separate `aas-selection-evidence.json` sidecar in an `artifact-dir`; the manifest preserves exact agent-selected IDs, while evidence records factual process trace and the agent-declared capability ledger.
* **Validate and preview through the CLI.** `aas stack validate` checks the proposal, while `aas stack plan` produces an immutable, per-target plan without applying it.
* **Review in Workbench.** The hosted Workbench imports and reviews stack/plan JSON in browser memory; it does not access your filesystem or install anything.
* **Retain every useful distribution path.** Direct installs, plugins, bundles, workflows, and the full catalog remain available as payload and compatibility surfaces.

> \[!IMPORTANT]
> Structural and identity validity does not certify semantic fit, compatibility, setup correctness, operational safety, or safety to apply.

| Surface                            | Current status                                                                                                                  |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Published package                  | Current npm release; AAS Core status is `agent-first-preview`                                                                   |
| Catalog search and inspection      | Supported preview; local and read-only                                                                                          |
| Agent-owned composition            | Supported preview; Core validates IDs and structure, not semantic suitability; manifests have a technical maximum of 128 skills |
| Stack validation and plan preview  | Supported preview; no target skill changes                                                                                      |
| Workbench                          | Browser-local review of stack and plan artifacts                                                                                |
| Selection evidence                 | Exported and inspected through MCP/CLI contracts; not yet reviewed in Workbench                                                 |
| Apply and recovery                 | Experimental, explicit opt-in, outside the supported safety claim                                                               |
| Semantic suitability certification | Not provided                                                                                                                    |

Read the [AAS Core guide](https://github.com/sickn33/agentic-awesome-skills/blob/v16.7.0/docs/users/aas-core.md) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05 for the exact trust boundaries, current preview status, Codex/Claude setup model, and CLI lifecycle.

## Why This Repo

* **Agent-first, locally controlled**: Codex or Claude inspects the project and chooses from the complete local catalog without uploading your repository to AAS.
* **Complete and inspectable**: every catalog skill is searchable, readable, and available for agent selection; Core does not certify suitability, compatibility, or operational safety, and metadata is informational rather than an eligibility gate.
* **Approval before writes**: the durable artifacts are an approved stack and immutable plan, not an opaque one-shot install.
* **Installable, not just inspirational**: use the compatible legacy installer or plugin distributions when direct delivery is the right path.
* **Built for major agent workflows**: Claude Code, Cursor, Codex CLI, Autohand Code, Gemini CLI, Antigravity, Kiro, OpenCode, Copilot, and more.
* **Broad coverage with real utility**: 2,111+ skills across development, testing, security, infrastructure, product, and marketing.
* **Inspect before installing**: the hosted [Skill Workbench](https://sickn33.github.io/agentic-awesome-skills/workbench) reviews agent-produced stack manifests and immutable plans without browser-side installation.
* **Focused delivery remains available**: specialized plugins package curated sets for web, security, data, docs, DevOps, QA, OSS, or agent/MCP workflows.
* **Useful whether you want breadth or curation**: install the full catalog, choose a specialized plugin, start with bundles, or compare alternatives before installing.

### Why not just search the skills directory?

Direct file search can find candidate prose, but it leaves the result in the conversation. AAS Core adds verified catalog identity, explicit target binding, durable desired state, optional selection evidence, deterministic validation, immutable planning, and dedicated review surfaces. Its value is not choosing better than the coding agent; it is turning the agent's choice into reproducible, inspectable state.

## Table of Contents

* [AAS Core: Agent-First Preview](#aas-core-agent-first-preview)
* [Why This Repo](#why-this-repo)
* [Installation](#installation)
* [Recommended Specialized Plugins](#recommended-specialized-plugins)
* [Choose Your Tool](#choose-your-tool)
* [Quick FAQ](#quick-faq)
* [Bundles & Workflows](#bundles--workflows)
* [Browse 2,111+ Skills](#browse-2111-skills)
* [Troubleshooting](#troubleshooting)
* [Stable Skills Manifest v1](#stable-skills-manifest-v1)
* [Support the Project](#support-the-project)
* [Contributing](#contributing)
* [Community](#community)
* [Credits & Sources](#credits--sources)
* [Repo Contributors](#repo-contributors)
* [Star History](#star-history)
* [License](#license)

## Installation

For Codex and Claude, start with the [AAS Core guide](https://github.com/sickn33/agentic-awesome-skills/blob/v16.7.0/docs/users/aas-core.md) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05: configure the local MCP, ask the agent to inspect the project and choose exact IDs from the full catalog, review the proposed `aas-stack.json`, then run CLI validation and planning. The MCP and validation are read-only. Planning writes only the requested plan artifact; it does not materialize skill payloads or AAS managed state in the target.

Use direct installation when your host does not yet have a native AAS Core adapter, when you already know the exact skill IDs, or when you deliberately prefer manual selection:

* **Specialized plugins** when the job has a clear domain.
* **Full library install** when you want every skill available in a local skills directory.
* **Bundles and workflows** when you want role-based recommendations or ordered execution playbooks.

### From selection to use

1. Describe the project outcome to Codex or Claude with the local AAS MCP configured.
2. Have the agent compare candidates and read the selected instructions and support files. Preserve the exact IDs in `aas-stack.json` and review their prerequisites.
3. Validate the manifest and review a CLI plan when you need an artifact-based check. Workbench can help inspect the artifacts.
4. For actual use, preview the supported direct installer with those same IDs, an exact release and the intended host directory. Review its own changes, then repeat without `--dry-run` when installation is authorized. Invoke the skill in a real task and keep the resulting check or artifact for reuse.

For example, after reviewing `brainstorming` and `systematic-debugging` for a Codex project, run from that project directory:

```bash
npm exec --yes --ignore-scripts --package=agentic-awesome-skills@16.7.0 -- \
  agentic-awesome-skills --release 16.7.0 --path .agents/skills \
  --skills brainstorming,systematic-debugging --dry-run
```

Replace the example IDs with the reviewed selection. The direct installer has its own preview and ownership format; it does not consume or apply a Core plan. Core apply/recovery remain experimental. [Worked cases](docs/users/workflows.md#recorded-worked-cases) show observed inputs and outputs without claiming guaranteed model performance.

### Direct skill install

```bash
# Antigravity: preview an exact, agent-selected set before writing.
npx agentic-awesome-skills --antigravity --skills brainstorming,systematic-debugging --dry-run

# Antigravity CLI slash commands (agy): ~/.gemini/antigravity-cli/skills/<skill>/SKILL.md
npx agentic-awesome-skills --agy
```

On `main`, the npm installer uses a shallow partial clone and checks out the canonical `skills/` tree after verifying the cloned commit against the immutable `gitHead` recorded for that exact npm package version. Git 2.25+ is required. Plugin mirrors, documentation and app assets are excluded from that temporary checkout; every canonical skill and support file remains available. See the [measured distribution comparison](docs/maintainers/distribution-efficiency.md). If the GitHub tag moved or npm identity metadata is unavailable, installation stops before copying content. Use `--tag main` only when you intentionally accept a mutable, explicitly unverified repository ref.

Antigravity watches `~/.agents/skills` and may load enough installed instructions
to exhaust its context, slow startup, trigger truncation errors, or enter a crash
loop. For that target, the installer stops before cloning or writing unless you
provide `--skills`, a metadata filter, or the explicit `--all` override. The bare
`npx agentic-awesome-skills` command uses the same protected Antigravity target.

The recommended flow is to ask Codex or Claude with the read-only AAS Core MCP
configured to inspect the project, search the complete catalog, and choose exact
skill IDs. The agent selects the IDs; AAS MCP validates them without installing; the agent
or user then previews the direct installation with the command above and repeats
it without `--dry-run` after review.

Other direct-install targets retain the legacy-compatible full-catalog behavior
when no selectors are supplied. The CLI prints the catalog's risk summary first:
a full install includes `critical` and authorized-use-only `offensive`
instructions. Installation copies files; it does not execute their commands,
but an agent may act on an installed skill later. Prefer an exact reviewed set:

```bash
npx agentic-awesome-skills audit --skills brainstorming,backend-dev-guidelines
npx agentic-awesome-skills --skills brainstorming,backend-dev-guidelines --dry-run
```

If you deliberately accept the context and crash-loop risk, the complete
Antigravity catalog remains available through explicit consent:

```bash
npx agentic-awesome-skills --antigravity --all
```

The audit reads the selected skill directories without executing them and
reports command, network, credential, filesystem, privileged, destructive,
symlink, and binary signals. It is a review aid, not a safety certificate. See
[Security, trust, and antivirus alerts](docs/users/security-and-antivirus.md).

### Focused single-skill install with GitHub CLI (preview)

GitHub CLI can preview and install one exact skill for Copilot and other supported hosts. Use an exact `SKILL.md` path in this large, mirrored repository so the selected source is unambiguous and discovery stays fast:

```bash
gh skill preview sickn33/agentic-awesome-skills skills/brainstorming/SKILL.md
gh skill install sickn33/agentic-awesome-skills skills/brainstorming/SKILL.md \
  --agent github-copilot --scope user --pin v14.2.0
```

`gh skill` support is currently a GitHub CLI preview and may change. Install a focused skill or plugin surface for the job; do not use `--all` unless you intentionally want every discovered canonical and mirrored skill.

### Verify the install

```bash
test -d ~/.agents/skills && echo "Skills installed in ~/.agents/skills"
```

### Run your first skill

```text
Use @brainstorming to plan a SaaS MVP.
```

### Prefer plugins for Claude Code, Codex, or another compatible client?

* Use a specialized plugin when you want a focused marketplace-style distribution.
* Use the full-library plugin only when you want the widest plugin-safe catalog.
* Read [Plugins for compatible agent clients](docs/users/plugins.md) for host-specific installs, portable Agent Plugins bundles, and direct skills installs.

## Recommended Specialized Plugins

Do not install everything first if you already know the work. Start with the focused plugin for your job, then add more only when the task expands.

All specialized plugins are generated as Claude Code and Codex plugin bundles. Bundles with flat, cross-host-safe skill layouts also receive a standard Agent Plugins 1.0 root manifest. For Antigravity, use the same `SKILL.md` content through the installer or supported skills paths.

| Plugin                           | Skills | Best for                                                                      |
| -------------------------------- | -----: | ----------------------------------------------------------------------------- |
| AAS Web App Builder              |     10 | Frontend and full-stack developers shipping modern web apps.                  |
| AAS Product Design Studio        |     10 | Product UI, brand, portfolio, accessibility, and richer visual work.          |
| AAS Security Engineer            |     10 | Authorized security testing, audit, and hardening.                            |
| AAS Secure App Builder           |     10 | Developers who want security embedded while building features.                |
| AAS Documents & Presentations    |      9 | Office files, document conversion, decks, and slide workflows.                |
| AAS Data Analytics               |     10 | Product analytics, SQL, dashboards, and experiments.                          |
| AAS Agent & MCP Builder          |     10 | Agentic apps, MCP tools, RAG systems, and evaluation loops.                   |
| AAS QA & Test Automation         |     10 | Test suites, browser automation, and QA stabilization.                        |
| AAS DevOps & Cloud               |     10 | Infrastructure, deployments, and operational workflows.                       |
| AAS Accessibility & Inclusive UX |      8 | WCAG audits, automated scans, screen-reader checks, and accessible QA.        |
| AAS API Platform Builder         |     10 | API design, OpenAPI contracts, auth, security, load tests, and observability. |
| AAS SaaS Launch & Revenue        |     10 | SaaS MVPs, pricing, payments, analytics, lifecycle, referrals, and SEO.       |
| AAS AI Product & Evaluation Ops  |     10 | AI product metrics, evals, tracing, experiments, and model-quality loops.     |

Next-wave plugins cover marketing/SEO/growth, automation, observability/incident response, Python APIs, mobile apps, data engineering, privacy/compliance, and localization/international growth.

* Read the [specialized plugin roadmap](docs/users/specialized-plugin-roadmap.md).
* Read the [plugin guide for compatible agent clients](docs/users/plugins.md).
* Compare the hosted [specialized plugin landing page](https://sickn33.github.io/agentic-awesome-skills/plugins).
* Browse the generated plugin folders in [`plugins/`](plugins/).

## Choose Your Tool

Use the same repository, but install or invoke it in the way your host expects.

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

Use the Codex and Claude guides for the AAS Core MCP preview path. For other hosts—or when you deliberately want manual delivery—use the table's direct install targets, specialized plugins, and host-specific path guidance.

* [Claude Code skills](docs/users/claude-code-skills.md): install paths, starter skills, prompt examples, and plugin marketplace flow.
* [Cursor skills](docs/users/cursor-skills.md): `.cursor/skills/` setup, UI-heavy work, and pair-programming flows.
* [Codex CLI skills](docs/users/codex-cli-skills.md): planning, implementation, debugging, and review skills for local coding loops.
* [Gemini CLI skills](docs/users/gemini-cli-skills.md): research, agent systems, integrations, and engineering workflows.
* [AI agent skills guide](docs/users/ai-agent-skills.md): breadth vs curation, skill-library evaluation, and starting-point selection.

## Quick FAQ

### What is Agentic Awesome Skills?

**Agentic Awesome Skills** is the repository behind AAS Core, a local agent-first control plane for recording and validating agent-chosen skill stacks. The read-only AAS MCP gives Codex and Claude complete catalog search and skill inspection; the stack CLI and Workbench make the chosen state reproducible and reviewable. Direct installers, specialized plugins, bundles, and workflows remain supported distribution and discovery surfaces.

### Is AAS Core fully certified?

The supported path covers complete local catalog search and inspection, agent-owned selection, stack composition and validation, immutable planning, and diagnosis. Transactional apply/recovery safety remains outside the supported claim; apply and recovery are explicitly experimental and disabled without additional opt-in flags.

### How do I install it?

For AAS Core, follow the [preview guide](https://github.com/sickn33/agentic-awesome-skills/blob/v16.7.0/docs/users/aas-core.md) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05 and use only a package release whose notes explicitly state that it includes Core. Release 14.6.0 predates Core; Core-capable releases begin with the 15.x line.

For direct skill distribution, use a tool-specific flag such as `--codex`,
`--cursor`, `--gemini`, or `--claude` to place skills in the directory your
assistant watches. The default target is Antigravity; it requires `--skills`, a
metadata filter, or explicit `--all` consent before cloning or writing because a
full watched catalog can exhaust context or trigger a crash loop.

For Autohand Code, use the installer with a custom path:

```bash
npx agentic-awesome-skills --path ~/.autohand/skills
npx agentic-awesome-skills --path .autohand/skills
```

### What are AAS specialized plugins?

AAS specialized plugins are focused, domain-specific distributions of the skill library. They package the most relevant skills for web apps, security, data analytics, documents, DevOps, QA, OSS maintenance, and agent or MCP work so users can start with the right surface instead of activating the entire catalog.

### Should I use the full library or a plugin?

Use the full library if you want the biggest catalog and direct filesystem control. Use a specialized plugin when you want a smaller, marketplace-style distribution for a specific workflow in Claude Code or Codex. For Antigravity, install the matching skills into the supported skills path. The complete explanation lives in [Plugins for Claude Code and Codex](docs/users/plugins.md).

### How are plugins, bundles, and workflows different?

Plugins are installable packaging surfaces, bundles are curated skill recommendations, and workflows are ordered execution playbooks. Start with a plugin when the domain is clear, use bundles to compare adjacent skills, and use workflows when the important part is sequencing planning, coding, testing, auditing, or release work.

### Where do I browse plugins, bundles, workflows, and the full catalog?

Start with [Specialized Plugins](#recommended-specialized-plugins) when you want an installable domain pack. Use [Bundles](docs/users/bundles.md) for role-based recommendations, [Workflows](docs/users/workflows.md) for ordered execution playbooks, [CATALOG.md](CATALOG.md) for the full registry, and the hosted [GitHub Pages catalog](https://sickn33.github.io/agentic-awesome-skills/) for searchable browsing.

## Bundles & Workflows

Core, plugins, bundles, and workflows answer different questions. Codex or Claude selects skills; AAS Core records and validates that selection; plugins package a focused delivery surface; bundles are curated starting points; workflows are ordered playbooks for getting a result.

| Surface            | Answers                                                                 | Use it for                                                                                |
| ------------------ | ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| AAS Core           | How do I search the full catalog and preserve the agent's chosen stack? | Agent-owned selection, a pinned `aas-stack.json`, validation, and immutable plan preview. |
| Specialized plugin | What should I install or activate for this domain?                      | Focused Claude Code/Codex plugin packaging and Antigravity-compatible skill selection.    |
| Bundle             | Which skills naturally belong together?                                 | Role-based discovery after a full-library install or when building a custom subset.       |
| Workflow           | What order should the agent run skills in?                              | Planning, shipping, auditing, testing, or incident-style execution.                       |

Use a specialized plugin first when your domain is clear. Use bundles to explore adjacent skills or assemble a custom install. Use workflows when the hard part is sequencing the work.

### Start with bundles

Bundles are curated groups of recommended skills for a role or goal such as `Web Wizard`, `Security Engineer`, or `OSS Maintainer`.

* Bundles are recommendations, not separate installs.
* Install the closest specialized plugin when one matches your work, or install the repository once and use [docs/users/bundles.md](docs/users/bundles.md) to pick a starting set.
* Good starter combinations:
  * SaaS MVP: `Essentials` + `Full-Stack Developer` + `QA & Testing`
  * Production hardening: `Security Developer` + `DevOps & Cloud` + `Observability & Monitoring`
  * OSS shipping: `Essentials` + `OSS Maintainer`

### Use workflows for outcome-driven execution

* Read [docs/users/workflows.md](docs/users/workflows.md) for human-readable playbooks.
* Use [data/workflows.json](data/workflows.json) for machine-readable workflow metadata.
* Initial workflows include shipping a SaaS MVP, security audits, AI agent systems, QA/browser automation, and DDD-oriented design work.

### Need fewer active skills at runtime?

If Antigravity starts hitting context limits with too many active skills, the activation guidance in [docs/users/agent-overload-recovery.md](docs/users/agent-overload-recovery.md) can materialize only the bundles or skill ids you want in the live Antigravity directory.

If you use OpenCode or another `.agents/skills` host, prefer a reduced install up front instead of copying the full library into a context-sensitive runtime. The installer now supports `--risk`, `--category`, and `--tags` so you can keep the installed set narrow.

For a reproducible exact set, pin the package and catalog release and preview the full per-target plan before writing:

```bash
npx agentic-awesome-skills@14.3.0 --codex --release 14.3.0 --skills frontend-design,game-development/2d-games --dry-run
```

Remove `--dry-run` only after reviewing the install, update, and removal plan. Unknown or ambiguous skill identifiers fail closed, and metadata filters combine with `--skills` using AND.

The hosted [Skill Workbench](https://sickn33.github.io/agentic-awesome-skills/workbench) imports and reviews AAS Core stack manifests and immutable plans in browser memory. It does not access the filesystem, generate an approved plan, or install skills.

## Browse 2,111+ Skills

Use the root repo as a landing page, then jump into the deeper surface that matches your intent.

### What you get in this repository

* **Skills library** in [`skills/`](skills/)
* **AAS Core** in [`tools/lib/aas-v1`](tools/lib/aas-v1), exposed through the `aas` CLI and local `aas-mcp` server
* **Versioned stack and result schemas** in [`schemas/aas-v1`](schemas/aas-v1)
* **Compatible legacy installer CLI** powered by the npm package in [`package.json`](package.json)
* **Generated catalog and metadata** in [`CATALOG.md`](CATALOG.md), `skills_index.json`, and [`data/`](data/)
* **Hosted and local web app** in [`apps/web-app`](apps/web-app) and on [GitHub Pages](https://sickn33.github.io/agentic-awesome-skills/)
* **Role-based bundles** in [docs/users/bundles.md](docs/users/bundles.md)
* **Specialized plugin surfaces** in [docs/users/specialized-plugin-roadmap.md](docs/users/specialized-plugin-roadmap.md), [docs/users/plugins.md](docs/users/plugins.md), and [`plugins/`](plugins/)
* **Execution workflows** in [docs/users/workflows.md](docs/users/workflows.md)
* **User, contributor, and maintainer docs** under [`docs/`](docs/)
* **Project visuals** in [`assets/`](assets/), including the [hero](assets/aas-readme-hero.jpeg), [social card](assets/aas-social-card.jpeg), [logo](assets/aas-logo.jpeg), and [support banner](assets/buy-me-a-coffee-banner.png)

### Best ways to explore

* Read the full catalog in [`CATALOG.md`](CATALOG.md).
* Browse the hosted catalog at <https://sickn33.github.io/agentic-awesome-skills/>.
* Start with [Getting Started](docs/users/getting-started.md) and [Usage](docs/users/usage.md) if you are new after installation.
* Use [Bundles](docs/users/bundles.md) for role-based discovery and [Workflows](docs/users/workflows.md) for step-by-step execution.
* Use [Plugins for Claude Code and Codex](docs/users/plugins.md) when you care about marketplace-safe distribution, and the [Specialized Plugin Roadmap](docs/users/specialized-plugin-roadmap.md) when you want the best plugin candidates.

### Compare alternatives

* **[Vexilo · A field guide to Claude Code](https://vexilo.app/?lang=en)** — different scope: a visual, searchable index of every Claude Code primitive (31 agents / 99 commands / 123 skills / 13 rules), organized around the 5-step workflow. Useful as a navigation layer *over* any skill library, not as a skill library itself. ([companion repo](https://github.com/lilhawk7077/claude-code-resources) ⭐ 1 | 🐛 0 | 📅 2026-07-01)
* **[Agentic Awesome Skills vs Awesome Claude Skills](docs/users/agentic-awesome-skills-vs-awesome-claude-skills.md)** for breadth vs curated-list tradeoffs.
* **[Best Claude Code skills on GitHub](docs/users/best-claude-code-skills-github.md)** for a high-intent shortlist.
* **[Best Cursor skills on GitHub](docs/users/best-cursor-skills-github.md)** for Cursor-compatible options and selection criteria.

## Troubleshooting

Keep the root README short; use the dedicated docs for recovery and platform-specific guidance.

* For Core setup, trust boundaries, stack manifests, and preview status, use the [AAS Core guide](https://github.com/sickn33/agentic-awesome-skills/blob/v16.7.0/docs/users/aas-core.md) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05.
* If you are confused after installation, start with the [Usage Guide](docs/users/usage.md).
* On native Windows, `AAS_ADAPTER_WINDOWS_ACL_FAILED` refers to the configuration path checked with PowerShell `Get-Acl`, not the cache and not `icacls`; do not approve until preview returns an approval digest.
* If you integrate agentic-awesome-skills into a host, read the discovery contract first: [Stable Skills Manifest v1](docs/users/discovery-manifest.md).
* For Windows truncation or context crash loops, use [docs/users/windows-truncation-recovery.md](docs/users/windows-truncation-recovery.md).
* For Linux/macOS overload or selective activation, use [docs/users/agent-overload-recovery.md](docs/users/agent-overload-recovery.md).
* For OpenCode or other `.agents/skills` installs, prefer a reduced install such as `npx agentic-awesome-skills --path .agents/skills --category development,backend --risk safe,none`.
* For plugin install details, host compatibility, and marketplace-safe distribution, use [docs/users/plugins.md](docs/users/plugins.md).
* For contributor expectations and guardrails, use [CONTRIBUTING.md](CONTRIBUTING.md), [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md), and [`SECURITY.md`](SECURITY.md).

## Stable Skills Manifest v1

This is the stable **direct-host discovery manifest** for integrations that load individual `SKILL.md` files. It is not `aas-stack.json`, the verified AAS Core catalog, or the Core composition contract. Core users should start with the [AAS Core guide](https://github.com/sickn33/agentic-awesome-skills/blob/v16.7.0/docs/users/aas-core.md) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05; custom host integrations can continue using the manifest below.

Host integrations should use:

* [`skills_index.json`](./skills_index.json) as the **canonical array-format manifest**.
* [`schemas/skills-index.v1.schema.json`](./schemas/skills-index.v1.schema.json) for the JSON shape.
* [`data/skills_index.json`](./data/skills_index.json) as the compatibility mirror.

This keeps discovery stable (`id`, `path`, metadata) while ensuring hosts only load `SKILL.md` for requested `@skill-id` values.

## Support the Project

Support is optional. The project stays free and open-source for everyone.

[![Buy me a coffee](assets/buy-me-a-coffee-banner.png)](https://buymeacoffee.com/sickn33)

* [Buy me a book on Buy Me a Coffee](https://buymeacoffee.com/sickn33)
* Security tooling support: [Snyk](https://snyk.io/)
* Star the repository
* Open reproducible issues
* Contribute docs, fixes, and skills

***

## Contributing

* Add new skills under `skills/<skill-name>/SKILL.md`.
* Follow the contributor guide in [`CONTRIBUTING.md`](CONTRIBUTING.md).
* Use the template in [`docs/contributors/skill-template.md`](docs/contributors/skill-template.md).
* Validate with `npm run validate` before opening a PR.
* Keep community PRs source-only: do not commit generated registry artifacts like `CATALOG.md`, `skills_index.json`, or `data/*.json`.
* If your PR changes `SKILL.md`, expect the automated `skill-review` check on GitHub in addition to the usual validation and security scans.
* If your PR changes skills or risky guidance, manual logic review is still required even when the automated checks are green.

## Community

* [Discussions](https://github.com/sickn33/agentic-awesome-skills/discussions) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05 for questions, ideas, showcase posts, and community feedback.
* [Issues](https://github.com/sickn33/agentic-awesome-skills/issues) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05 for reproducible bugs and concrete, actionable improvement requests.
* [Follow @AASkills\_ on X](https://x.com/AASkills_) for daily skills, practical workflows, and example prompts from the repo.
* [Follow @sickn33 on X](https://x.com/sickn33) for project updates and releases.
* [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) for community expectations and moderation standards.
* [`SECURITY.md`](SECURITY.md) for security reporting.

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

* **[anthropics/skills](https://github.com/anthropics/skills) ⭐ 174,238 | 🐛 1,208 | 🌐 Python | 📅 2026-09-03**: Official Anthropic skills repository - Document manipulation (DOCX, PDF, PPTX, XLSX), Brand Guidelines, Internal Communications.
* **[anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks) ⭐ 52,439 | 🐛 320 | 🌐 Jupyter Notebook | 📅 2026-09-03**: Official notebooks and recipes for building with Claude.
* **[vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) ⭐ 30,851 | 🐛 174 | 🌐 JavaScript | 📅 2026-08-28**: Vercel Labs official skills - React Best Practices, Web Design Guidelines.
* **[openai/skills](https://github.com/openai/skills) ⭐ 25,414 | 🐛 291 | 🌐 Python | 📅 2026-07-14**: OpenAI Codex skills catalog - Agent skills, Skill Creator, Concise Planning.
* **[Skyvern-AI/skyvern](https://github.com/Skyvern-AI/skyvern) ⭐ 22,931 | 🐛 216 | 🌐 Python | 📅 2026-09-05**: Official Skyvern browser automation skill — AI-powered browser control using Vision LLMs and computer vision for navigating sites, filling forms, and extracting structured data.
* **[huggingface/skills](https://github.com/huggingface/skills) ⭐ 11,019 | 🐛 48 | 🌐 Python | 📅 2026-09-03**: Official Hugging Face skills - Models, Spaces, datasets, inference, and broader Hugging Face ecosystem workflows.
* **[browser-act/skills](https://github.com/browser-act/skills) ⭐ 5,580 | 🐛 7 | 🌐 Python | 📅 2026-08-24**: Official BrowserAct skills - authenticated browser automation, JavaScript-rendered extraction, screenshots, parallel session isolation, verification handling, and human handoff (MIT).
* **[remotion-dev/skills](https://github.com/remotion-dev/skills) ⭐ 4,487 | 🐛 21 | 🌐 TypeScript | 📅 2026-09-01**: Official Remotion skills - Video creation in React with 28 modular rules.
* **[google-gemini/gemini-skills](https://github.com/google-gemini/gemini-skills) ⭐ 3,985 | 🐛 10 | 🌐 Python | 📅 2026-09-02**: Official Gemini skills - Gemini API, SDK and model interactions.
* **[browserbase/skills](https://github.com/browserbase/skills) ⭐ 3,710 | 🐛 54 | 🌐 JavaScript | 📅 2026-09-02**: Official Browserbase `competitor-analysis` skill - Browserbase Search API competitor discovery, research lanes, matrices, screenshots, and HTML reports (MIT).
* **[nowork-studio/NotFair](https://github.com/nowork-studio/NotFair) ⭐ 3,452 | 🐛 13 | 🌐 TypeScript | 📅 2026-08-29**: Official source for the `seo-drift` skill - dated SEO baselines and regression detection across rankings, indexation, metadata, directives, schema, and on-page elements (MIT).
* **[Forward-Future/loop-library](https://github.com/Forward-Future/loop-library) ⭐ 3,105 | 🐛 5 | 🌐 JavaScript | 📅 2026-07-26**: Official Loop Library skill - find, adapt, and design bounded AI-agent feedback loops with verification, stop rules, guardrails, and handoffs (MIT).
* **[microsoft/skills](https://github.com/microsoft/skills) ⭐ 2,992 | 🐛 69 | 🌐 TypeScript | 📅 2026-09-04**: Official Microsoft skills - Azure cloud services, Bot Framework, Cognitive Services, and enterprise development patterns across .NET, Python, TypeScript, Go, Rust, and Java.
* **[Simon-He95/markstream-vue](https://github.com/Simon-He95/markstream-vue) ⭐ 2,986 | 🐛 5 | 🌐 Vue | 📅 2026-09-04**: Official Markstream skill for installing streaming Markdown renderers across Vue, React, Svelte, Angular, Nuxt, Next.js, and Vue 2 applications (MIT).
* **[supabase/agent-skills](https://github.com/supabase/agent-skills) ⭐ 2,574 | 🐛 417 | 🌐 TypeScript | 📅 2026-08-12**: Supabase official skills - Postgres Best Practices.
* **[expo/skills](https://github.com/expo/skills) ⭐ 2,501 | 🐛 61 | 🌐 Shell | 📅 2026-09-03**: Official Expo skills - Expo project workflows and Expo Application Services guidance.
* **[apify/agent-skills](https://github.com/apify/agent-skills) ⭐ 2,367 | 🐛 37 | 🌐 Python | 📅 2026-08-27**: Official Apify skills - Web scraping, data extraction and automation.
* **[MiniMax-AI/cli](https://github.com/MiniMax-AI/cli) ⭐ 2,081 | 🐛 22 | 🌐 TypeScript | 📅 2026-09-03**: Official MiniMax CLI - text, image, video, speech, music, vision, and web-search workflows for MiniMax models and APIs.
* **[vostride/agent-qa](https://github.com/vostride/agent-qa) ⭐ 901 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-03**: Official Agent QA skills for authoring natural-language web and mobile tests, evidence-backed run triage, and scoped debug/fix workflows (FSL-1.1-ALv2, Apache-2.0 after two years).
* **[dair-ai/dair-academy-plugins](https://github.com/dair-ai/dair-academy-plugins) ⭐ 611 | 🐛 0 | 🌐 HTML | 📅 2026-07-21**: Official DAIR Academy plugin skills imported as standalone skills - image generation, adaptive learning, lesson artifacts, LLM council deliberation, survey papers, wiki building, and YouTube study notes (MIT).
* **[Orkas-AI/Orkas-VideoStudio](https://github.com/Orkas-AI/Orkas-VideoStudio) ⭐ 491 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-04**: Official source for the `video-router` skill - choose and lock generation, deterministic composition, supplied-footage editing, or an automatic cross-modal production plan (MIT).
* **[Xquik-dev/x-twitter-scraper](https://github.com/Xquik-dev/x-twitter-scraper) ⭐ 193 | 🐛 2 | 🌐 JavaScript | 📅 2026-09-04**: Official Xquik skill for X data workflows - tweet search, user lookup, follower export, media downloads, MCP, webhooks, OpenAPI, and SDK setup (MIT).
* **[pilot-protocol/pilotprotocol](https://github.com/pilot-protocol/pilotprotocol) ⭐ 135 | 🐛 3 | 🌐 Go | 📅 2026-09-03**: Official Pilot Protocol overlay network - agent addressing, encrypted P2P messaging, NAT traversal, and an installable agent app store (AGPL-3.0).
* **[sandbaseai/cli](https://github.com/sandbaseai/cli) ⭐ 110 | 🐛 2 | 🌐 TypeScript | 📅 2026-08-28**: Official source for the `sandbase-mcp` skill - discover, inspect, and invoke 2,000+ AI models and APIs through a local MCP bridge with explicit schema and cost checks (Apache-2.0).
* **[weaviate/agent-skills](https://github.com/weaviate/agent-skills) ⭐ 104 | 🐛 2 | 🌐 Python | 📅 2026-06-11**: Official Weaviate skills - vector database operations, semantic and hybrid search, data imports, RAG cookbooks, agentic RAG, multimodal PDF search, and async client patterns (BSD-3-Clause).
* **[neondatabase/agent-skills](https://github.com/neondatabase/agent-skills) ⭐ 85 | 🐛 13 | 🌐 JavaScript | 📅 2026-09-04**: Official Neon skills - Serverless Postgres workflows and Neon platform guidance.
* **[longbridge/skills](https://github.com/longbridge/skills) ⭐ 52 | 🐛 3 | 🌐 Python | 📅 2026-08-27**: Official Longbridge Securities skills - real-time quotes, charts, fundamentals, portfolio analysis, options, and market workflows for HK, US, A-share, and SG markets.
* **[uizze/uizze](https://github.com/uizze/uizze) ⭐ 17 | 🐛 5 | 🌐 JavaScript | 📅 2026-09-01**: Official UIZZE source for the free `anti-ui-slop` skill—product-specific UI references, design contracts, required states, and a hard finish gate grounded in 800,000+ real web and iOS screens (MIT).
* **[BuyWhere/buywhere-mcp](https://github.com/BuyWhere/buywhere-mcp) ⭐ 10 | 🐛 14 | 🌐 TypeScript | 📅 2026-09-04**: Official BuyWhere MCP server — search and compare products from Singapore, SEA, and US markets via Model Context Protocol.
* **[scopeblind/scopeblind-gateway](https://github.com/scopeblind/scopeblind-gateway) ⭐ 9 | 🐛 4 | 🌐 TypeScript | 📅 2026-07-09**: Official Scopeblind MCP governance toolkit - Cedar policy authoring, shadow-to-enforce rollout, and signed-receipt verification guidance for agent tool calls.
* **[HasData/hasdata-cli](https://github.com/HasData/hasdata-cli) ⭐ 7 | 🐛 1 | 🌐 Go | 📅 2026-09-04**: Official HasData CLI and API guidance for search, scraping, ecommerce, travel, jobs, local business, and structured web data workflows.
* **[happy520ai/unified-ai-system](https://github.com/happy520ai/unified-ai-system) ⭐ 6 | 🐛 13 | 🌐 JavaScript | 📅 2026-09-05**: Official source for the `unified-ai-gateway` skill - nine governed Codex MCP tools for provider-free prompt enhancement, credential-free gateway health, readiness, fake-provider chat, knowledge, workflow, and workforce evidence (Apache-2.0).
* **[agent-frontier/wgm](https://github.com/agent-frontier/wgm) ⭐ 3 | 🐛 4 | 🌐 Shell | 📅 2026-08-29**: Official wgm protocol skill - governed build loops with triage, alignment, planning, deterministic backpressure, holdout-scenario judging, and handoff audits (MIT).
* **[bekservice/Famulor-Skill](https://github.com/bekservice/Famulor-Skill) ⭐ 2 | 🐛 0 | 📅 2026-08-23**: Official Famulor skill for tenant-safe operation of its hosted MCP server across assistants, communication history, campaigns, knowledge, automations, telephony, and workspace administration (MIT).
* **[runapi-ai/cli-skill](https://github.com/runapi-ai/cli-skill) ⭐ 2 | 🐛 0 | 📅 2026-08-17**: Official RunAPI CLI skill - generate AI images, videos, and music/audio from agent workflows, plus run other model API jobs.
* **[Modellix/modellix-plugin](https://github.com/Modellix/modellix-plugin) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-09-04**: Official Modellix skill - authenticated, paid AI image and video generation through the Modellix CLI (MIT).
* **[ASI2030/Fact-Check-X](https://github.com/ASI2030/Fact-Check-X) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-08-31**: Source for the `fact-check-x-complete` workflow - claim-level AI answer comparison, citation-fidelity review, and public primary-source verification without bundled browser automation (Apache-2.0).
* **[cohesivity-org/cohesivity-skill](https://github.com/cohesivity-org/cohesivity-skill) ⭐ 0 | 🐛 0 | 📅 2026-08-27**: Official Cohesivity skill - agent provisioned backend infrastructure covering Postgres, hosting, auth, realtime, storage, cron, email, and AI model APIs over one HTTP API (MIT).

</details>

<details>
<summary><strong>Community Contributors & Source Repositories</strong></summary>

### Community Contributors

* **[obra/superpowers](https://github.com/obra/superpowers) ⭐ 281,865 | 🐛 333 | 🌐 Shell | 📅 2026-09-04**: The original "Superpowers" by Jesse Vincent.

* **[mattpocock/skills](https://github.com/mattpocock/skills) ⭐ 250,838 | 🐛 466 | 🌐 Shell | 📅 2026-09-04**: Source for 17 Matt Pocock workflow skills - codebase design, TDD, bug diagnosis, triage, PRDs, issues, prototyping, handoff, teaching, and skill-writing guidance (MIT).

* **[affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) ⭐ 248,755 | 🐛 144 | 🌐 JavaScript | 📅 2026-09-04**: Large Claude Code configuration and workflow collection from an Anthropic hackathon winner (MIT).

* **[multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) ⭐ 210,215 | 🐛 129 | 📅 2026-04-20**: Source for the `andrej-karpathy` skill - English Karpathy-inspired LLM coding guidelines for simplicity, surgical changes, assumption surfacing, and verifiable success criteria (MIT).

* **[addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) ⭐ 92,310 | 🐛 137 | 🌐 JavaScript | 📅 2026-09-05**: Source for the `browser-testing-with-devtools` skill - Chrome DevTools MCP browser verification, profiling, network inspection, and frontend debugging guidance (MIT).

* **[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) ⭐ 84,422 | 🐛 60 | 🌐 JavaScript | 📅 2026-08-24**: Frontend design taste skill collection covering premium UI generation, redesign audits, GSAP motion, Stitch design systems, minimalist and brutalist visual modes, and full-output enforcement.

* **[unslothai/unsloth](https://github.com/unslothai/unsloth) ⭐ 75,638 | 🐛 1,422 | 🌐 Python | 📅 2026-09-05**: Source for the `unsloth-finetuning` skill - single-GPU VRAM sizing, LoRA/QLoRA configuration, chat-template and loss-masking correctness, GRPO/DPO post-training, and GGUF/merged export paths (Apache-2.0).

* **[kepano/obsidian-skills](https://github.com/kepano/obsidian-skills) ⭐ 47,876 | 🐛 68 | 📅 2026-06-08**: Obsidian-focused skills for markdown, Bases, JSON Canvas, CLI workflows, and content cleanup.

* **[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) ⭐ 46,922 | 🐛 106 | 🌐 JavaScript | 📅 2026-09-05**: Marketing skills for CRO, copywriting, SEO, paid ads, and growth (23 skills, MIT).

* **[K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) ⭐ 42,710 | 🐛 31 | 🌐 Python | 📅 2026-09-02**: Scientific, research, engineering, finance, and writing skill suite (MIT).

* **[emilkowalski/skills](https://github.com/emilkowalski/skills) ⭐ 35,503 | 🐛 1 | 🌐 Markdown | 📅 2026-08-21**: Source for Emil Kowalski design engineering skills - UI polish, motion review, animation standards, component craft, and high-taste frontend guidance (MIT).

* **[zhaoxuya520/reverse-skill](https://github.com/zhaoxuya520/reverse-skill) ⭐ 34,613 | 🐛 2 | 🌐 PowerShell | 📅 2026-09-03**: Source for 43 security skills covering reverse engineering, binary analysis, offensive assessment orchestration, and threat-intelligence workflows, adapted with English metadata and upstream safety gates (MIT).

* **[VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) ⭐ 33,770 | 🐛 55 | 📅 2026-09-04**: Curated collection of 1000+ official and community agent skills from leading development teams (MIT).

* **[zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides) ⭐ 28,749 | 🐛 69 | 🌐 JavaScript | 📅 2026-06-23**: Frontend slide-creation skills for web-based presentations (MIT).

* **[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) ⭐ 25,546 | 🐛 12 | 🌐 Python | 📅 2026-08-30**: Senior Engineering and PM toolkit.

* **[muratcankoylan/Agent-Skills-for-Context-Engineering](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering) ⭐ 17,920 | 🐛 52 | 🌐 Python | 📅 2026-08-19**: Context-engineering, multi-agent, and production agent-system skill collection (MIT).

* **[AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo) ⭐ 16,324 | 🐛 52 | 🌐 Python | 📅 2026-08-26**: SEO workflow collection covering technical SEO, hreflang, sitemap, geo, schema, and programmatic SEO patterns.

* **[travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) ⭐ 14,970 | 🐛 795 | 📅 2026-04-28**: Loki Mode and Playwright integration.

* **[diet103/claude-code-infrastructure-showcase](https://github.com/diet103/claude-code-infrastructure-showcase) ⭐ 10,017 | 🐛 18 | 🌐 TypeScript | 📅 2026-07-13**: Infrastructure and Backend/Frontend Guidelines.

* **[vudovn/antigravity-kit](https://github.com/vudovn/antigravity-kit) ⭐ 8,170 | 🐛 57 | 🌐 TypeScript | 📅 2026-08-31**: AI Agent templates with Skills, Agents, and Workflows (33 skills, MIT).

* **[ibelick/ui-skills](https://github.com/ibelick/ui-skills) ⭐ 8,107 | 🐛 13 | 🌐 TypeScript | 📅 2026-09-03**: UI-polish skills for improving interfaces built by agents (MIT).

* **[czlonkowski/n8n-skills](https://github.com/czlonkowski/n8n-skills) ⭐ 6,193 | 🐛 9 | 🌐 Shell | 📅 2026-09-03**: n8n workflow-building skills for Claude Code (MIT).

* **[ChrisWiles/claude-code-showcase](https://github.com/ChrisWiles/claude-code-showcase) ⭐ 6,059 | 🐛 12 | 🌐 JavaScript | 📅 2026-01-06**: React UI patterns and Design Systems.

* **[zebbern/claude-code-guide](https://github.com/zebbern/claude-code-guide) ⭐ 4,600 | 🐛 1 | 🌐 Python | 📅 2026-09-05**: Comprehensive Security suite & Guide (Source for \~60 new skills).

* **[Dimillian/Skills](https://github.com/Dimillian/Skills) ⭐ 3,941 | 🐛 11 | 🌐 Shell | 📅 2026-03-29**: Curated Codex skills focused on Apple platforms, GitHub workflows, refactoring, and performance (MIT).

* **[davidondrej/skills](https://github.com/davidondrej/skills) ⭐ 3,935 | 🐛 2 | 🌐 Python | 📅 2026-09-05**: Source for David Ondrej agent workflow skills across orchestration, research, setup, skill authoring, and documentation workflows (MIT).

* **[AvdLee/SwiftUI-Agent-Skill](https://github.com/AvdLee/SwiftUI-Agent-Skill) ⭐ 3,491 | 🐛 3 | 🌐 Python | 📅 2026-08-12**: SwiftUI best-practices skill for agent workflows (MIT).

* **[CloudAI-X/threejs-skills](https://github.com/CloudAI-X/threejs-skills) ⭐ 3,239 | 🐛 9 | 📅 2026-07-09**: Three.js-focused skill collection for agent-assisted 3D web work.

* [cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill) ⭐ 3,224 | 🐛 6 | 🌐 JavaScript | 📅 2026-07-06 — Cloudflare Web Security Audit Skill (by Cloudflare)

* **[yaojingang/yao-meta-skill](https://github.com/yaojingang/yao-meta-skill) ⭐ 2,596 | 🐛 1 | 🌐 Python | 📅 2026-08-17**: Source for the `yao-meta-skill` skill - governed skill creation, refactoring, evaluation, packaging, review, and distribution workflows (MIT).

* **[amElnagdy/delegate-skills](https://github.com/amElnagdy/delegate-skills) ⭐ 1,673 | 🐛 23 | 🌐 JavaScript | 📅 2026-08-31**: Source for 18 delegation skills (`delegate-setup` + 17 implementer relays for Claude/Codex/Cursor/OpenCode and 13 more) — multi-agent delegation and fleet orchestration with Node built-ins only, relay never commits (MIT, docs-only — runtime not bundled).

* **[rmyndharis/antigravity-skills](https://github.com/rmyndharis/antigravity-skills) ⭐ 1,482 | 🐛 2 | 🌐 JavaScript | 📅 2026-08-02**: For the massive contribution of 300+ Enterprise skills and the catalog generation logic.

* **[hyhmrright/brooks-lint](https://github.com/hyhmrright/brooks-lint) ⭐ 1,448 | 🐛 1 | 🌐 JavaScript | 📅 2026-09-01**: AI code-review skill grounded in classic software engineering books for design-smell, coupling, and architecture review.

* [amElnagdy/guard-skills](https://github.com/amElnagdy/guard-skills) ⭐ 1,227 | 🐛 4 | 📅 2026-07-04 — Code Quality & Testing Guard Skills (by amElnagdy)

* **[gooseworks-ai/goose-skills](https://github.com/gooseworks-ai/goose-skills) ⭐ 1,195 | 🐛 56 | 🌐 Python | 📅 2026-09-01**: Source for the `competitor-ad-intelligence` and `ad-campaign-analyzer` skills - evidence-labeled public ad research plus uncertainty-aware campaign diagnostics and bounded budget tests (MIT).

* **[guanyang/antigravity-skills](https://github.com/guanyang/antigravity-skills) ⭐ 960 | 🐛 5 | 🌐 TypeScript | 📅 2026-09-04**: Core Antigravity extensions.

* **[bitjaru/styleseed](https://github.com/bitjaru/styleseed) ⭐ 943 | 🐛 16 | 🌐 TypeScript | 📅 2026-09-03**: StyleSeed Toss UI and UX skill collection - setup wizard, page and pattern generation, design-token management, accessibility review, UX audits, feedback states, and microcopy guidance for professional mobile-first UI.

* **[huifer/WellAlly-health](https://github.com/huifer/WellAlly-health) ⭐ 938 | 🐛 7 | 🌐 Shell | 📅 2026-07-16**: Healthcare assistant project cited in release history as a source for health-focused agent capabilities (MIT).

* **[Optim-Agent/optim-agent](https://github.com/Optim-Agent/optim-agent) ⭐ 936 | 🐛 0 | 🌐 Python | 📅 2026-08-14**: Source for the `optim-agent` skill - agent-guided optimization of configurable systems against measurable objectives (MIT).

* **[vibeforge1111/vibeship-spawner-skills](https://github.com/vibeforge1111/vibeship-spawner-skills) ⭐ 879 | 🐛 14 | 🌐 JavaScript | 📅 2026-01-02**: AI agents, integrations, maker tools, and other production-grade skill packs.

* **[sergebulaev/linkedin-skills](https://github.com/sergebulaev/linkedin-skills) ⭐ 873 | 🐛 3 | 🌐 Python | 📅 2026-09-05**: Source for the `linkedin-post-writer` skill - LinkedIn post drafting from 16 tested hook formulas mapped to engagement goals, with 2026 formatting rules and an AI-tell scrub pass, from a 10-skill LinkedIn bundle for Claude Code and Codex (MIT).

* **[ZeroPointRepo/youtube-skills](https://github.com/ZeroPointRepo/youtube-skills) ⭐ 753 | 🐛 3 | 📅 2026-09-01**: Source for the `youtube-full` skill - TranscriptAPI-backed YouTube transcripts, search, channel browsing, playlists, and cloud-safe video research workflows (MIT).

* **[ZhangHanDong/makepad-skills](https://github.com/ZhangHanDong/makepad-skills) ⭐ 747 | 🐛 0 | 📅 2026-04-07**: Makepad app-development skills and references (MIT).

* **[karanb192/awesome-claude-skills](https://github.com/karanb192/awesome-claude-skills) ⭐ 505 | 🐛 211 | 📅 2026-09-01**: A massive list of verified skills for Claude Code.

* **[baskduf/FableCodex](https://github.com/baskduf/FableCodex) ⭐ 437 | 🐛 9 | 🌐 Python | 📅 2026-07-26**: Source for the `codex-fable5` skill - Codex-native Fable-inspired workflow discipline for evidence-first implementation, goal tracking, review findings, verification gates, and prompt adaptation (AGPL-3.0-or-later).

* **[sanjay3290/ai-skills](https://github.com/sanjay3290/ai-skills) ⭐ 417 | 🐛 4 | 🌐 Python | 📅 2026-07-09**: Apache-licensed collection of agent skills for AI coding assistants.

* **[LambdaTest/agent-skills](https://github.com/LambdaTest/agent-skills) ⭐ 366 | 🐛 4 | 🌐 Python | 📅 2026-07-24**: Production-grade agent skills for test automation — 46 skills covering E2E, unit, mobile, BDD, visual, and cloud testing across 15+ languages (MIT).

* **[zxkane/aws-skills](https://github.com/zxkane/aws-skills) ⭐ 360 | 🐛 0 | 🌐 Python | 📅 2026-06-15**: AWS-focused Claude agent skills (MIT).

* **[AlmogBaku/debug-skill](https://github.com/AlmogBaku/debug-skill) ⭐ 317 | 🐛 2 | 🌐 Go | 📅 2026-04-17**: Interactive debugger skill for AI agents — breakpoints, stepping, variable inspection, and stack traces via the `dap` CLI. Supports Python, Go, Node.js/TypeScript, Rust, and C/C++.

* **[ohad6k/ditto](https://github.com/ohad6k/ditto) ⭐ 288 | 🐛 21 | 🌐 Python | 📅 2026-08-24**: Source for the `ditto` skill - mines local coding-agent sessions into private, evidence-backed work, design, and writing profiles with dated source receipts (MIT).

* **[drogers0/gh-image](https://github.com/drogers0/gh-image) ⭐ 266 | 🐛 8 | 🌐 Go | 📅 2026-09-02**: Source for the `gh-image` skill - GitHub CLI image uploads that return canonical `user-attachments` embed URLs for PRs, issues, comments, and README screenshots (MIT).

* **[provencher/codex-skills](https://github.com/provencher/codex-skills) ⭐ 241 | 🐛 0 | 📅 2026-07-26**: Source for the `orchestrate` skill - focused Codex multi-agent delegation with non-overlapping ownership, coordinator integration, and user-held approval gates (MIT).

* **[scarletkc/vexor](https://github.com/scarletkc/vexor) ⭐ 239 | 🐛 3 | 🌐 Python | 📅 2026-08-29**: Semantic search engine for files and code, referenced in release history.

* **[taisly/agent](https://github.com/taisly/agent) ⭐ 219 | 🐛 2 | 🌐 JavaScript | 📅 2026-07-06**: Source for the Taisly Social Media Posting skill - Codex plugin, CLI, SDK, and official MCP server for publishing approved short-form videos to TikTok, Instagram Reels, YouTube Shorts, X, and Facebook (MIT).

* **[jthack/ffuf\_claude\_skill](https://github.com/jthack/ffuf_claude_skill) ⭐ 210 | 🐛 1 | 🌐 Python | 📅 2025-10-16**: FFUF skill for web fuzzing workflows in Claude.

* **[gokapso/agent-skills](https://github.com/gokapso/agent-skills) ⭐ 153 | 🐛 6 | 🌐 JavaScript | 📅 2026-08-26**: Kapso/WhatsApp-oriented agent skills.

* **[kubestellar/console](https://github.com/kubestellar/console) ⭐ 132 | 🐛 100 | 🌐 TypeScript | 📅 2026-09-05**: KubeStellar Console multi-cluster Kubernetes dashboard with `kc-agent` MCP integration, AI-assisted operations, and built-in agent skills.

* **[luoyuctl/agenttrace](https://github.com/luoyuctl/agenttrace) ⭐ 129 | 🐛 7 | 🌐 Rust | 📅 2026-08-24**: Source for the `agenttrace-session-audit` skill - local AI coding-agent session audits for cost spikes, tool failures, latency gaps, anomalies, health gates, and session diffs (MIT).

* **[MohamedAbdallah-14/unslop](https://github.com/MohamedAbdallah-14/unslop) ⭐ 127 | 🐛 1 | 🌐 Python | 📅 2026-08-31**: Source for the `unslop` skill - deterministic and LLM-assisted cleanup for AI-generated prose across CLI and agent tool workflows.

* **[sandbaseai/sandbase-skills](https://github.com/sandbaseai/sandbase-skills) ⭐ 126 | 🐛 0 | 🌐 Python | 📅 2026-09-03**: Source for the `multi-source-search` skill - cross-validated research with explicit source diversity, confidence, conflicts, gaps, and an offline-checkable evidence ledger (Apache-2.0).

* **[wrsmith108/linear-claude-skill](https://github.com/wrsmith108/linear-claude-skill) ⭐ 121 | 🐛 0 | 🌐 TypeScript | 📅 2026-07-17**: Linear issue/project/team management skill with MCP and GraphQL workflows (MIT).

* **[Ducksss/codex-profiles](https://github.com/Ducksss/codex-profiles) ⭐ 117 | 🐛 0 | 🌐 Shell | 📅 2026-09-04**: Source for the `codex-profiles` skill - Codex CLI/Desktop profile isolation around separate `CODEX_HOME` directories, diagnostics, and account-context boundaries without copying auth tokens (MIT).

* **[JunsW/feature-track](https://github.com/JunsW/feature-track) ⭐ 107 | 🐛 0 | 🌐 Python | 📅 2026-07-16**: Source for the `feature-tracking` skill - lightweight repository-native feature memory for current status, source-of-truth documents, decisions, risks, and cross-session handoff (MIT).

* **[Necmttn/ax](https://github.com/Necmttn/ax) ⭐ 104 | 🐛 36 | 🌐 TypeScript | 📅 2026-08-26**: Source for the `ax-extract-workflow` skill - reconstruct workflow behind past coding-agent artifacts using local ax sessions, commits, skills, and tool traces (AGPL-3.0-only).

* **[Continuum-AI-Corp/OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) ⭐ 101 | 🐛 2 | 🌐 TypeScript | 📅 2026-09-04**: Source for the `orca-replay` skill - reading, replaying, and forking recorded coding-agent runs, so a question about what a past run did is answered from its trace rather than from memory (Apache-2.0).

* **[amElnagdy/review-skills](https://github.com/amElnagdy/review-skills) ⭐ 93 | 🐛 2 | 🌐 JavaScript | 📅 2026-08-26**: Source for the `debate-review` and `babysit-pr` skills - two-model debate review of PRs/MRs with inline comments and automated babysitting of review rounds for GitHub, GitLab and Azure DevOps (MIT, docs-only — runtime not bundled).

* **[njerschow/textme](https://github.com/njerschow/textme) ⭐ 93 | 🐛 0 | 🌐 TypeScript | 📅 2026-04-09**: Source for the `textme` skill — local daemon bridging inbound iMessages (via Sendblue) to a Claude Code session on the user's machine, with voice notes, image input, code execution, and a phone-number whitelist (MIT).

* **[monte-carlo-data/mc-agent-toolkit](https://github.com/monte-carlo-data/mc-agent-toolkit) ⭐ 91 | 🐛 6 | 🌐 Python | 📅 2026-08-24**: Monte Carlo data observability skills — table health checks, change impact assessment, monitor creation, push ingestion, and SQL validation notebooks for dbt changes.

* **[jonathimer/devmarketing-skills](https://github.com/jonathimer/devmarketing-skills) ⭐ 86 | 🐛 1 | 📅 2026-03-03**: Developer marketing skills — HN strategy, technical tutorials, docs-as-marketing, Reddit engagement, developer onboarding, and more (33 skills, MIT).

* **[ndesv21/socialclaw](https://github.com/ndesv21/socialclaw) ⭐ 86 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-24**: Source for the SocialClaw social media publishing skill - campaign scheduling and publishing across major social platforms with a single workspace API key.

* **[MetcalfSolutions/Satori](https://github.com/MetcalfSolutions/Satori) ⭐ 68 | 🐛 1 | 🌐 Shell | 📅 2026-04-13**: Clinically informed wisdom companion blending psychology frameworks and wisdom traditions into a structured reflective partner.

* **[Hanyuyuan6/remote-gpu-trainer](https://github.com/Hanyuyuan6/remote-gpu-trainer) ⭐ 63 | 🐛 0 | 🌐 Python | 📅 2026-08-10**: Source for the `remote-gpu-trainer` skill - rented and remote GPU job orchestration, monitoring, teardown safety, spot resilience, and DL-debug workflows (MIT).

* **[shmlkv/dna-claude-analysis](https://github.com/shmlkv/dna-claude-analysis) ⭐ 57 | 🐛 0 | 🌐 Python | 📅 2026-03-04**: Personal genome analysis toolkit — Python scripts analyzing raw DNA data across 17 categories (health risks, ancestry, pharmacogenomics, nutrition, psychology, etc.) with terminal-style single-page HTML visualization.

* **[SHADOWPR0/beautiful\_prose](https://github.com/SHADOWPR0/beautiful_prose) ⭐ 55 | 🐛 0 | 📅 2025-12-30**: Writing-quality skill for improving prose and reducing generic output.

* **[robzolkos/skill-rails-upgrade](https://github.com/robzolkos/skill-rails-upgrade) ⭐ 54 | 🐛 0 | 📅 2026-01-27**: Rails upgrade skill for agent-assisted migrations.

* **[rafsilva85/credit-optimizer-v5](https://github.com/rafsilva85/credit-optimizer-v5) ⭐ 50 | 🐛 0 | 🌐 Python | 📅 2026-05-25**: Manus AI credit optimizer skill — intelligent model routing, context compression, and smart testing. Saves 30-75% on credits with zero quality loss. Audited across 53 scenarios.

* **[Silverov/yandex-direct-skill](https://github.com/Silverov/yandex-direct-skill) ⭐ 48 | 🐛 1 | 🌐 Shell | 📅 2026-02-17**: Yandex Direct (API v5) advertising audit skill — 55 automated checks, A-F scoring, campaign/ad/keyword analysis for the Russian PPC market (MIT).

* **[xiehuan123/dsh-deepread](https://github.com/xiehuan123/dsh-deepread) ⭐ 47 | 🐛 0 | 🌐 JavaScript | 📅 2026-09-03**: Source for the `dsh-deepread` skill - evidence-first analysis of articles, books, PDFs, and document sets with claim tracing, knowledge maps, and Feynman checks (MIT).

* **[sudosubin/gh-attach](https://github.com/sudosubin/gh-attach) ⭐ 38 | 🐛 0 | 🌐 Go | 📅 2026-08-15**: Source for the `gh-attach` skill - GitHub CLI uploads and downloads of `user-attachments` (screenshots, PDFs, zips, videos), producing repo-scoped URLs for PRs, issues, and READMEs, with GitHub Enterprise Server support (MIT).

* **[Suraj1235/open-dynamic-workflows](https://github.com/Suraj1235/open-dynamic-workflows) ⭐ 36 | 🐛 0 | 🌐 JavaScript | 📅 2026-07-09**: Source for the `open-dynamic-workflows` skill - open-source dynamic multi-agent workflow engine that plans, orchestrates, and adversarially verifies parallel AI coding agents across OpenCode, Codex, Antigravity, and VS Code (MIT).

* **[adelaidasofia/ai-brain-starter](https://github.com/adelaidasofia/ai-brain-starter) ⭐ 36 | 🐛 44 | 🌐 Python | 📅 2026-09-02**: Source for the `ingest-youtube` skill - YouTube transcript ingestion into markdown vaults with yt-dlp metadata, VTT cleanup, and capture-seed stubs (MIT).

* **[glukicov/slideops](https://github.com/glukicov/slideops) ⭐ 36 | 🐛 0 | 🌐 HTML | 📅 2026-09-03**: Source for the `slideops` skill - cited HTML slide decks generated from a repository, with a standard-library drift check that reports the day the slides stop matching the code (MIT).

* **[talivia-group/agent](https://github.com/talivia-group/agent) ⭐ 35 | 🐛 3 | 🌐 JavaScript | 📅 2026-09-01**: Source for the `talivia-agent-kit` skill - revenue-first website analytics through the official MCP server, with explicit confirmation for tracking and payment attribution changes (MIT).

* **[umutbozdag/agent-skills-manager](https://github.com/umutbozdag/agent-skills-manager) ⭐ 34 | 🐛 2 | 🌐 TypeScript | 📅 2026-04-09**: Source for the `manage-skills` skill - cross-tool skill discovery, creation, editing, toggling, copying, moving, and deletion workflows across major agent coding tools.

* **[webzler/agentMemory](https://github.com/webzler/agentMemory) ⭐ 33 | 🐛 4 | 🌐 TypeScript | 📅 2026-01-21**: Source for the agent-memory-mcp skill.

* **[frmoretto/clarity-gate](https://github.com/frmoretto/clarity-gate) ⭐ 33 | 🐛 0 | 🌐 Python | 📅 2026-03-02**: Verification protocol for marking uncertainty and reducing hallucinated certainty in LLM-facing docs.

* **[wrsmith108/varlock-claude-skill](https://github.com/wrsmith108/varlock-claude-skill) ⭐ 33 | 🐛 0 | 📅 2026-03-04**: Secure environment-variable management skill for Claude Code (MIT).

* **[sstklen/infinite-gratitude](https://github.com/sstklen/infinite-gratitude) ⭐ 31 | 🐛 0 | 📅 2026-03-15**: Multi-agent research skill from the AI Dojo series (MIT).

* **[iradoweck/antigravity-awesome-skills](https://github.com/iradoweck/antigravity-awesome-skills) ⭐ 30 | 🐛 0 | 🌐 Python | 📅 2026-08-31**: Source for the GeminiIgnore FinOps skill - `.geminiignore` setup patterns for context-window efficiency and token cost reduction.

* **[NotMyself/claude-win11-speckit-update-skill](https://github.com/NotMyself/claude-win11-speckit-update-skill) ⚠️ Archived**: Archived Speckit update skill for Claude Code (MIT).

* **[yikuansun/PhotopeaAPI](https://github.com/yikuansun/PhotopeaAPI) ⭐ 29 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-04**: Source for the `photopea-embedded-editor` skill - Photopea embedding, host-page messaging, file I/O, scripting, and export workflows for web apps (MIT).

* **[sendblue-api/sendblue-cli](https://github.com/sendblue-api/sendblue-cli) ⭐ 29 | 🐛 3 | 🌐 TypeScript | 📅 2026-09-01**: Source for the `sendblue-cli`, `sendblue-api`, and `sendblue-notify` skills — iMessage, SMS, and RCS messaging via Sendblue's CLI and HTTP API, plus "text me when X finishes" notification patterns for Claude Code hooks and `/loop` / `/schedule` jobs (MIT).

* **[zircote/.claude](https://github.com/zircote/.claude) ⚠️ Archived**: Archived Claude Code dotfiles/config repo with a Shopify development skill reference.

* **[TheaDust/lore](https://github.com/TheaDust/lore) ⭐ 23 | 🐛 0 | 🌐 Python | 📅 2026-08-29**: Source for the `lore` skill - Markdown-only, zero-dependency long-term project memory for AI coding agents, with monorepo scopes, two-section platform mirrors, and stdlib Python helpers (MIT).

* **[rainmanjam/poka-yoke](https://github.com/rainmanjam/poka-yoke) ⭐ 22 | 🐛 0 | 🌐 Python | 📅 2026-09-01**: Source for the `poka-yoke` skill - software mistake-proofing through control, warning, detection, and source-inspection guardrails (MIT).

* **[hyhmrright/logic-lens](https://github.com/hyhmrright/logic-lens) ⭐ 22 | 🐛 5 | 🌐 Python | 📅 2026-08-29**: AI code-review skill for formal logic inspection across bugs, race conditions, security risks, and API contract issues.

* **[wede-wx/atlas](https://github.com/wede-wx/atlas) ⭐ 20 | 🐛 1 | 📅 2026-06-11**: Source for the `atlas-contract` and `atlas-ledger` goal-integrity skills - contract, phase-check, final-audit, and project-ledger guardrails for long-running agent work (MIT).

* **[mbenhard/unship](https://github.com/mbenhard/unship) ⭐ 19 | 🐛 0 | 🌐 JavaScript | 📅 2026-06-07**: Source for the `unship` skill - local workflow for comparing AI-generated UI variants in a real app, then keeping one option and cleaning up temporary alternatives (MIT).

* **[uberSKILLS](https://github.com/uberskillsdev/uberSKILLS) ⭐ 19 | 🐛 1 | 🌐 TypeScript | 📅 2026-04-04**: Design, test, and deploy Claude Code Agent Skills through a visual, AI-assisted workflow.

* **[anthony-chaudhary/dos-kernel](https://github.com/anthony-chaudhary/dos-kernel) ⭐ 19 | 🐛 103 | 🌐 Python | 📅 2026-08-24**: Source for the `dos-verify-done-claims` skill — gates an agent's "done / shipped / fixed" claim on git ground truth (ancestry + the commit's own diff) via the deterministic DOS kernel's read-only `dos verify` / `dos commit-audit` verbs (MIT).

* **[xi-kari/crossframe-skill](https://github.com/xi-kari/crossframe-skill) ⭐ 18 | 🐛 0 | 🌐 Python | 📅 2026-08-07**: Source for the CrossFrame Skill Suite - Chinese-canonical structural diagnosis, essay drafting, review, and companion workflows across relationships, organizations, institutions, public issues, and research notes (MIT).

* **[ejentum/ejentum-mcp](https://github.com/ejentum/ejentum-mcp) ⭐ 16 | 🐛 1 | 🌐 JavaScript | 📅 2026-06-11**: Source for the `ejentum-reasoning-harness` skill - MCP cognitive harness modes for reasoning, code review, anti-deception checks, and memory-drift analysis (MIT).

* **[SeanZoR/claude-speed-reader](https://github.com/SeanZoR/claude-speed-reader) ⭐ 16 | 🐛 0 | 🌐 HTML | 📅 2026-01-15**: RSVP-style speed-reading helper for Claude responses (MIT).

* **[TerminallyLazy/Tree-Ring-Memory](https://github.com/TerminallyLazy/Tree-Ring-Memory) ⭐ 16 | 🐛 3 | 🌐 Rust | 📅 2026-08-29**: Source for the `tree-ring-memory` skill — local-first memory lifecycle guidance for recall, evidence, audit, forgetting, consolidation, and privacy-safe agent memory operations (MIT).

* **[amartelr/antigravity-workspace-manager](https://github.com/amartelr/antigravity-workspace-manager) ⭐ 15 | 🐛 1 | 🌐 Python | 📅 2026-02-28**: Workspace Manager CLI companion to dynamically auto-provision subsets of skills across local development environments.

* **[Intelligent-Internet/II-Commons-Skills](https://github.com/Intelligent-Internet/II-Commons-Skills) ⭐ 15 | 🐛 1 | 🌐 JavaScript | 📅 2026-07-08**: Source for the II-Commons research skill - deterministic retrieval across arXiv, PubMed/PMC, and supported US policy corpora.

* **[uxuiprinciples/agent-skills](https://github.com/uxuiprinciples/agent-skills) ⭐ 15 | 🐛 0 | 📅 2026-08-31**: Research-backed UX/UI agent skills for auditing interfaces against 168 principles, detecting antipatterns, and injecting UX context into AI coding sessions.

* **[abhinaykrupa/cowork-to-code-bridge](https://github.com/abhinaykrupa/cowork-to-code-bridge) ⭐ 12 | 🐛 13 | 🌐 Python | 📅 2026-08-07**: Source for the `cowork-to-code-bridge` skill - consent-bound execution on the user's own machine with pinned provenance, narrow scopes, and explicit local-agent limitations (MIT).

* **[nedcodes-ok/rule-porter](https://github.com/nedcodes-ok/rule-porter) ⭐ 12 | 🐛 4 | 🌐 JavaScript | 📅 2026-03-04**: Bidirectional rule converter between Cursor (.mdc), Claude Code (CLAUDE.md), GitHub Copilot, Windsurf, and legacy .cursorrules formats. Zero dependencies.

* **[jackjin1997/ClawForge](https://github.com/jackjin1997/ClawForge) ⭐ 12 | 🐛 1 | 🌐 Python | 📅 2026-06-16**: Resource hub of skills, MCP servers, and agent tooling for OpenClaw.

* **[whatiskadudoing/fp-ts-skills](https://github.com/whatiskadudoing/fp-ts-skills) ⭐ 11 | 🐛 0 | 📅 2026-01-30**: Practical fp-ts skills for TypeScript – fp-ts-pragmatic, fp-ts-react, fp-ts-errors (v4.4.0).

* **[fullstackcrew-alpha/privacy-mask](https://github.com/fullstackcrew-alpha/privacy-mask) ⭐ 11 | 🐛 0 | 🌐 Python | 📅 2026-03-24**: Local image privacy masking for AI coding agents. Detects and redacts PII, API keys, and secrets in screenshots via OCR + 47 regex rules. Claude Code hook integration for automatic masking. Supports Tesseract and RapidOCR. 100% offline (MIT).

* **[stareezy-1/frontend-architecture-skill](https://github.com/stareezy-1/frontend-architecture-skill) ⭐ 10 | 🐛 0 | 📅 2026-06-14**: Source for the `frontend-lighthouse` skill - portable Lighthouse CI Core Web Vitals gates, performance budgets, and GitHub Actions reporting (MIT).

* **[timwukp/agent-skills-best-practice](https://github.com/timwukp/agent-skills-best-practice) ⭐ 10 | 🐛 0 | 🌐 Python | 📅 2026-09-05**: Source for the `fsi-compliance-checker` skill - financial-services compliance triage for PCI-DSS v4.0 and MAS TRM control mapping (MIT).

* **[AgentPhone-AI/skills](https://github.com/AgentPhone-AI/skills) ⭐ 9 | 🐛 0 | 📅 2026-09-04**: AgentPhone plugin for Claude Code — API-first telephony workflows for AI agents, including phone calls, SMS, phone-number management, voice-agent setup, streaming webhooks, and tool-calling patterns.

* **[connerkward/mcp-apple-notes](https://github.com/connerkward/mcp-apple-notes) ⭐ 8 | 🐛 1 | 🌐 HTML | 📅 2026-06-17**: Source for the `apple-notes-search` skill - semantic and keyword search, related-note discovery, bridge finding, entity threads, and cited synthesis across local Apple Notes via MCP (MIT).

* **[connerkward/screenstudio-alternative-skill](https://github.com/connerkward/screenstudio-alternative-skill) ⭐ 8 | 🐛 0 | 🌐 Python | 📅 2026-06-23**: Source for the `screenstudio-alt` skill - open-source screen recording polish with auto-zoom, idle speed-up, cursor treatment, captions, and vertical export workflows (MIT).

* **[rich-elicitation](https://github.com/CyberZenithX/Rich-Elicitation-Skill) ⭐ 8 | 🐛 1 | 📅 2026-05-07**: Source for the `rich-elicitation` skill - asks clarifying questions in multiple rounds before starting ambiguous tasks.

* **[heyneuron/flowhunt-skill](https://github.com/heyneuron/flowhunt-skill) ⭐ 8 | 🐛 1 | 📅 2026-05-21**: Source for the FlowHunt automation discovery audit skill - workflow intake, tool-by-tool audit, and opportunity prioritization for productivity automation.

* **[riffkit/skill](https://github.com/riffkit/skill) ⭐ 7 | 🐛 0 | 📅 2026-08-25**: Official upstream source for the `riffkit` skill - short-form video riffing and UGC ad generation in nine natively generated languages (MIT).

* **[cruisekkk/time-ledger](https://github.com/cruisekkk/time-ledger) ⭐ 7 | 🐛 1 | 📅 2026-07-07**: Source for the `time-ledger` skill - natural-language time tracking parsed into the user's own Notion database with ask-instead-of-guessing reconciliation (MIT).

* **[aomi-labs/skills](https://github.com/aomi-labs/skills) ⭐ 7 | 🐛 13 | 🌐 Shell | 📅 2026-09-03**: Source for the `aomi-transact` skill — natural-language driver for the Aomi CLI with account-abstraction-first execution and simulate-then-sign across 25+ DeFi apps (MIT).

* **[SHADOWPR0/security-bluebook-builder](https://github.com/SHADOWPR0/security-bluebook-builder) ⭐ 7 | 🐛 0 | 📅 2025-12-24**: Security documentation/buildbook skill for agent workflows.

* **[maxbaluev/accreted-intelligence](https://github.com/maxbaluev/accreted-intelligence) ⭐ 7 | 🐛 2 | 🌐 Shell | 📅 2026-07-05**: Source for the `accint-solve` skill — routes coding-agent work through AccInt's MCP memory loop with retrieval, continuation frames, commitments, and outcome feedback (Apache 2.0).

* **[atdy/maoxuan-product-agent](https://github.com/atdy/maoxuan-product-agent) ⭐ 6 | 🐛 0 | 🌐 Markdown | 📅 2026-07-10**: Source for the `product-decision-agent` skill - Chinese-first product judgment across prioritization, growth, operations, data, delivery, and cross-functional collaboration, with 36 tested scenarios (MIT).

* **[sparklingneuronics/sparkling-skills](https://github.com/sparklingneuronics/sparkling-skills) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-07-11**: Source for the `dispatch` skill - multi-CLI delegation from Claude Code to Codex, Antigravity, and Gemini agents (MIT).

* **[connerkward/ckw-design-skill](https://github.com/connerkward/ckw-design-skill) ⭐ 6 | 🐛 0 | 🌐 JavaScript | 📅 2026-06-17**: Source for the `ckw-design` skill - frontend design direction, design-system guidance, visual philosophy, spatial checks, usability review, and production UI polish workflows (MIT).

* **[ZeroPointRepo/zillow-skills](https://github.com/ZeroPointRepo/zillow-skills) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-08-23**: Source for the `us-property-data` skill - U.S. property lookup, valuation, listing, tax, school, photo, and price-history guidance through the independent Zillapi API (MIT-0).

* **[vipin-si/article-illustrations](https://github.com/vipin-si/article-illustrations) ⭐ 6 | 🐛 0 | 📅 2026-06-23**: Source for the `article-illustrations` skill - Grav-style hand-drawn article illustrations with whiteboard sketches, sparse annotations, and visual metaphor QA guidance (MIT).

* **[sarveshtalele/linkedin-content-skill](https://github.com/sarveshtalele/linkedin-content-skill) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2026-06-01**: Source for the `linkedin-content-generator` skill - LinkedIn post, carousel, newsletter, and content-calendar generation workflows with local feedback memory (MIT).

* **[cruisekkk/trading-ledger](https://github.com/cruisekkk/trading-ledger) ⭐ 5 | 🐛 1 | 📅 2026-07-07**: Source for the `trading-ledger` skill - decision-quality trade journaling that captures entry thesis, plan, and emotion into the user's own Notion database (MIT).

* **[bin1874/before-you-build-skill](https://github.com/bin1874/before-you-build-skill) ⭐ 5 | 🐛 0 | 🌐 JavaScript | 📅 2026-07-01**: Source for the `before-you-build` skill - pre-coding product risk review across demand, alternatives, switching costs, channels, and validation steps (MIT).

* **[qinghui316/ecl-harness-engineer](https://github.com/qinghui316/ecl-harness-engineer) ⭐ 5 | 🐛 0 | 🌐 Python | 📅 2026-09-02**: Source for the `ecl-harness-engineer` skill - ECL Agent Harness infrastructure for AI coding workflows, repository guidance, change tracking, lint checks, CI gates, and handoff docs (MIT).

* **[commitshow/production-audit](https://github.com/commitshow/production-audit) ⭐ 5 | 🐛 0 | 📅 2026-05-04**: Source for the `production-audit` skill - shipped-app readiness auditing across deployment health, RLS, webhooks, secrets exposure, grants, Stripe idempotency, and mobile UX.

* **[warmskull/idea-darwin](https://github.com/warmskull/idea-darwin) ⭐ 5 | 🐛 0 | 📅 2026-04-07**: Darwinian idea-evolution workflow for structured ideation rounds, mutation, crossbreeding, critique, and lineage tracking.

* **[SSOJet/skills](https://github.com/ssojet/skills) ⭐ 5 | 🐛 0 | 📅 2026-02-24**: Production-ready SSOJet skills and integration guides for popular frameworks and platforms — Node.js, Next.js, React, Java, .NET Core, Go, iOS, Android, and more. Works seamlessly with SSOJet SAML, OIDC, and enterprise SSO flows. Works with Cursor, Antigravity, Claude Code, and Windsurf.

* **[yehudalevy-collab/polis-protocol](https://github.com/yehudalevy-collab/polis-protocol) ⭐ 5 | 🐛 11 | 🌐 Python | 📅 2026-09-03**: Source for the `polis-protocol` multi-agent coordination skill with capability cards, routing history, and protocol amendments (MIT).

* **[flyingsquirrel0419/squirrel-skill](https://github.com/flyingsquirrel0419/squirrel-skill) ⭐ 5 | 🐛 0 | 🌐 Shell | 📅 2026-04-29**: Full-cycle software development skill — plans, builds, tests, lints, fixes bugs, and writes production-grade docs. Auto-detects project state and adapts its 8-phase pipeline. Works on 9 AI coding agent platforms (Apache 2.0).

* **[AntonioCardenas/generate-nanobanana](https://github.com/AntonioCardenas/generate-nanobanana) ⭐ 5 | 🐛 0 | 📅 2026-08-04**: Source for the `generate-nanobanana` skill - image and video generation via Google's Gemini media models (Nano Banana 2 Lite/Standard/Pro, Gemini Omni Flash) with cost-approval gates before paid runs, real reference-image support, and a prompt/seed log beside every output (MIT).

* **[JularDepick/user-thoughts.SKILL](https://github.com/JularDepick/user-thoughts.SKILL) ⭐ 4 | 🐛 0 | 🌐 Python | 📅 2026-07-24**: Source for the `user-thoughts` skill - persistent project idea repository workflows for capturing decisions, tech stack notes, UI/UX rationale, and MDBASE-backed project memory (MIT).

* **[lewiswigmore/agent-skills](https://github.com/lewiswigmore/agent-skills) ⭐ 4 | 🐛 0 | 📅 2026-05-05**: Source for the `vscode-extension-guide-en` skill - VS Code extension development workflows, packaging, Marketplace publishing, TreeView, and webview patterns.

* **[Wolfe-Jam/faf-skills](https://github.com/Wolfe-Jam/faf-skills) ⭐ 4 | 🐛 0 | 🌐 Shell | 📅 2026-08-18**: AI-context and project DNA skills — .faf format management, AI-readiness scoring, bi-sync, MCP server building, and championship-grade testing (7 skills, MIT).

* **[UrRhb/agentflow](https://github.com/UrRhb/agentflow) ⭐ 4 | 🐛 0 | 🌐 Shell | 📅 2026-04-01**: Kanban-driven AI development pipeline for orchestrating multi-worker Claude Code workflows with deterministic quality gates, adversarial review, cost tracking, and crash-proof execution (MIT).

* **[Phelan164/codex-howto](https://github.com/Phelan164/codex-howto) ⭐ 3 | 🐛 4 | 🌐 Python | 📅 2026-09-04**: Source for the `maintain-codex-wiki` skill - review-first engineering knowledge with provenance, explicit capture and promotion, and deterministic structural checks (MIT).

* **[connerkward/macos-screen-recorder-system-audio](https://github.com/connerkward/macos-screen-recorder-system-audio) ⭐ 3 | 🐛 0 | 🌐 Swift | 📅 2026-08-17**: Source for the `macos-screen-recorder` skill - macOS ScreenCaptureKit recording with system audio, CLI workflows, permission handling, and export guidance (MIT).

* **[Antheurus/anywrite](https://github.com/Antheurus/anywrite) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-07-31**: Source for the `anywrite` skill - low-context CLI access to Anytype's local API for objects, properties, files, search, chat, and other workspace operations (MIT).

* **[demo112/yunqu-ai-skills](https://github.com/demo112/yunqu-ai-skills) ⭐ 3 | 🐛 1 | 🌐 HTML | 📅 2026-05-13**: Source for WeChat official account, Xiaohongshu content strategy, and MCP tool development skills for Chinese-language platform workflows (MIT).

* **[2slides/slides-generation-2slides-skills](https://github.com/2slides/slides-generation-2slides-skills) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2026-02-12**: Source for the `2slides-ppt-generator` skill - AI presentation generation, PDF deck creation, narration, theme search, and slide export workflows using the 2slides API (MIT).

* **[Slashworks-biz/idea-os](https://github.com/Slashworks-biz/idea-os) ⭐ 3 | 🐛 0 | 📅 2026-04-18**: Source for the `idea-os` skill - five-phase pipeline (triage -> clarify -> research -> PRD -> plan) that turns raw ideas into a build-ready PRD and execution plan.

* **[Wittlesus/cursorrules-pro](https://github.com/Wittlesus/cursorrules-pro) ⭐ 3 | 🐛 0 | 🌐 Shell | 📅 2026-02-21**: Professional .cursorrules configurations for 8 frameworks - Next.js, React, Python, Go, Rust, and more. Works with Cursor, Claude Code, and Windsurf.

* **[mishanefedov/skill-issue](https://github.com/mishanefedov/skill-issue) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-06-02**: Source for the `skill-issue` activation-audit skill for grading SKILL.md trigger metadata, prompt matching, and collision clusters (MIT).

* **[christopherlhammer11-ai/tool-use-guardian](https://github.com/christopherlhammer11-ai/tool-use-guardian) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-04-27**: Source for the Tool Use Guardian skill — tool-call reliability wrapper with retries, recovery, and failure classification.

* **[christopherlhammer11-ai/recallmax](https://github.com/christopherlhammer11-ai/recallmax) ⭐ 3 | 🐛 0 | 🌐 TypeScript | 📅 2026-04-27**: Source for the RecallMax skill — long-context memory, summarization, and conversation compression for agents.

* **[CodeShuX/tokenwise](https://github.com/CodeShuX/tokenwise) ⭐ 3 | 🐛 0 | 🌐 HTML | 📅 2026-08-26**: Source for the `tokenwise` skill — measurement-driven Haiku/Sonnet/Opus router for Claude Code with per-task NDJSON logging, A/B test mode, and verified $-saved reports (MIT).

* **[chenli-yy/entropy-box-public](https://github.com/chenli-yy/entropy-box-public) ⭐ 2 | 🐛 0 | 🌐 HTML | 📅 2026-09-03**: Source for the `entropy-box` skill - grounded embodied-AI research and workflow assembly through Consult, Search, Lookup, Evidence, and the Panorama Graph, with public-service privacy and physical-system safety boundaries (CC BY 4.0).

* **[Ghost011118/project-state-governor](https://github.com/Ghost011118/project-state-governor) ⭐ 2 | 🐛 1 | 📅 2026-08-25**: Source for the `project-state-governor` skill - evidence-backed canonical project state across sessions, branches, reviews, and research cycles (Apache-2.0).

* **[JanYork/using-lwc](https://github.com/JanYork/using-lwc) ⭐ 2 | 🐛 0 | 🌐 Shell | 📅 2026-08-14**: Source for the `using-lwc` skill - durable, source-grounded project memory with independently verified document and code graphs (Apache-2.0).

* **[supernovae-st/nika-agents](https://github.com/supernovae-st/nika-agents) ⭐ 2 | 🐛 2 | 🌐 Python | 📅 2026-09-04**: Official upstream source for the `nika` skill and its deterministic, budget-aware AI workflow runner (MIT skill content; AGPL-3.0 engine).

* **[chaunsin/agent-skills](https://github.com/chaunsin/agent-skills) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-06-18**: Source for the `pre-release-review` and `drizzle-migration-conflict` skills - deploy-readiness audits and Drizzle Kit migration-conflict workflows (Apache-2.0).

* **[takeaseatventure/devops-skills](https://github.com/takeaseatventure/devops-skills) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2026-07-27**: Source for the `cron-doctor` skill - cron expression diagnosis, validation, trap detection, and zero-dependency schedule analysis tooling (MIT).

* **[Genefold/arrowspace-skills](https://github.com/Genefold/arrowspace-skills) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-06-26**: Source for the `arrowspace` skill - spectral vector search using graph Laplacian eigenstructure for structurally aware retrieval (Apache-2.0).

* **[connerkward/web-media-getter-skill](https://github.com/connerkward/web-media-getter-skill) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2026-06-17**: Source for the `web-media-getter` skill - unified search across free image, video, and GIF APIs with license-aware media selection guidance (MIT).

* **[mturac/recsys-pipeline-architect](https://github.com/mturac/recsys-pipeline-architect) ⭐ 2 | 🐛 0 | 📅 2026-05-15**: Source for the `recsys-pipeline-architect` skill - recommendation, ranking, and feed pipeline architecture using Source, Hydrator, Filter, Scorer, Selector, and SideEffect stages (MIT).

* **[tsilverberg/webapp-uat](https://github.com/tsilverberg/webapp-uat) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2026-03-15**: Full browser UAT skill — Playwright testing with console/network error capture, WCAG 2.2 AA accessibility checks, i18n validation, responsive testing, and P0-P3 bug triage. Read-only by default, works with React, Vue, Angular, Ionic, Next.js.

* **[fruitwyatt/puzzle-activity-planner](https://github.com/fruitwyatt/puzzle-activity-planner) ⭐ 2 | 🐛 0 | 📅 2026-04-11**: Puzzle activity-planning skill for classrooms, parties, and events with generator-link workflows.

* **[Sharrmavishal/operating-kit](https://github.com/Sharrmavishal/operating-kit) ⭐ 2 | 🐛 0 | 📅 2026-07-07**: Source for the `pre-ship-gate` skill - a pre-deploy gate that walks the silent failure modes (migrations, feature flags, stale build cache, release pointer, staged rollout, missing env) and verifies the live revision instead of trusting deploy output (MIT).

* **[Junaid-PK/laravel-development-workflow](https://github.com/Junaid-PK/laravel-development-workflow) ⭐ 1 | 🐛 0 | 📅 2026-09-02**: Source for the `laravel-development-workflow` skill - root-cause Laravel bug fixes and repository-native feature work with regression coverage and risk-based verification (MIT).

* **[alexprivalov/boost-asio-skill](https://github.com/alexprivalov/boost-asio-skill) ⭐ 1 | 🐛 0 | 📅 2026-08-22**: Source for the `boost-asio-pro` skill - version-aware async C++ networking with Boost.Asio and standalone Asio across coroutine, callback, and classic `io_service` styles (MIT).

* **[5dive-ai/skills](https://github.com/5dive-ai/skills) ⭐ 1 | 🐛 0 | 📅 2026-09-03**: Source for the `compile-knowledge` skill - durable, atomic, interlinked knowledge stores with explicit hygiene, provenance, expiry, and secret-handling boundaries (MIT).

* **[saudademjj/luopan](https://github.com/saudademjj/luopan) ⭐ 1 | 🐛 0 | 📅 2026-08-10**: Source for the `travel-planner` skill - Chinese-first travel itinerary planning with mandatory budget confirmation, source-traceable facts, workload-aware daily pacing, and rule self-checks (MIT).

* **[OJPalenzuela/agents-generator](https://github.com/OJPalenzuela/agents-generator) ⭐ 1 | 🐛 0 | 📅 2026-08-03**: Source for the `agents-generator` skill - project-specific `AGENTS.md` and companion rule generation with package-manager detection, monorepo handling, dry-run/update modes, backups, and validated commands (MIT).

* **[agentbody/skills](https://github.com/agentbody/skills) ⭐ 1 | 🐛 1 | 🌐 Python | 📅 2026-08-27**: Source for the `people-data` skill - LinkedIn and YouTube professional-profile and public business-contact research via the Agent Body MCP server (MIT).

* **[0xsarwagya/ontoly](https://github.com/0xsarwagya/ontoly) ⭐ 1 | 🐛 2 | 🌐 TypeScript | 📅 2026-08-12**: Source for the `ontoly-software-graph` skill - deterministic TypeScript software graphs, MCP-backed architecture review, request tracing, impact analysis, and dependency analysis (MIT).

* **[hafiz-actyte/idea-autopsy](https://github.com/hafiz-actyte/idea-autopsy) ⭐ 1 | 🐛 0 | 📅 2026-07-10**: Source for the `idea-autopsy` skill - business-idea validation that hunts the one sentence that kills an idea before you build: kill-list check, five hard filters, free-AI one-prompt test, and live ad-market verification (MIT).

* **[takeaseatventure/sql-sentinel](https://github.com/takeaseatventure/sql-sentinel) ⭐ 1 | 🐛 1 | 🌐 JavaScript | 📅 2026-08-02**: Source for the `sql-sentinel` skill - SQL warehouse cost and performance anti-pattern audits across BigQuery, Snowflake, Redshift, and Postgres (MIT).

* **[connerkward/deterministic-design-skill](https://github.com/connerkward/deterministic-design-skill) ⭐ 1 | 🐛 0 | 🌐 JavaScript | 📅 2026-06-17**: Source for the `deterministic-design` skill - rendered UI layout and usability audits using deterministic measurement plus vision-judged review loops (MIT).

* **[connerkward/lookdev-auto-skill](https://github.com/connerkward/lookdev-auto-skill) ⭐ 1 | 🐛 0 | 📅 2026-06-17**: Source for the `lookdev-auto` skill - automated visual tuning loops where a vision or video model rates rendered variants and suggests improvements (MIT).

* **[connerkward/lookdev-studio-skill](https://github.com/connerkward/lookdev-studio-skill) ⭐ 1 | 🐛 0 | 📅 2026-06-17**: Source for the `lookdev` skill - human-in-the-loop visual and prose tuning through rendered variants, sliders, swatches, inline edits, and selection-driven refinement (MIT).

* **[mskadu/opencode-agent-skills](https://github.com/mskadu/opencode-agent-skills) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-06-06**: Source for opencode behavior, permission, skill-suggestion, and smart Git automation skills.

* **[mycelos-ai/bumblebee-skill](https://github.com/mycelos-ai/bumblebee-skill) ⭐ 1 | 🐛 0 | 🌐 Shell | 📅 2026-05-27**: Source for the `bumblebee` skill - multi-agent implementation workflows with repeatable planning, coding, review, and verification loops (MIT).

* **[tellmefrankie/news-engine](https://github.com/tellmefrankie/news-engine) ⭐ 1 | 🐛 6 | 🌐 TypeScript | 📅 2026-05-13**: Source for the `news-sentiment-engine` skill - news ingestion, sentiment analysis, and market/news intelligence workflows (MIT).

* **[Kench001/antigravity-awesome-skills](https://github.com/Kench001/antigravity-awesome-skills) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-05-03**: Source for the `recursive-context-pruning-token-budgeting` skill - context pruning, token budgeting, and long-session compression guidance (MIT).

* **[CodeShuX/mockhunter](https://github.com/CodeShuX/mockhunter) ⭐ 1 | 🐛 1 | 📅 2026-05-11**: Source for the `mock-hunter` skill - Playwright-based live-page audits that classify visible values as real, mock, LLM-generated, hardcoded, broken, or unknown (MIT).

* **[274326424/video-content-extractor](https://github.com/274326424/video-content-extractor) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-06-06**: Source for the `video-content-extractor` skill - FFmpeg and Tesseract OCR workflows for extracting timestamped screen text and structured Markdown reports from MP4 videos (MIT).

* **[metrox-eth/quit-sponsor](https://github.com/metrox-eth/quit-sponsor) ⭐ 1 | 🐛 0 | 📅 2026-07-14**: Source for the `quit-sponsor` skill - evidence-based quit-smoking sponsorship for agents with persistent memory: 44-source cited protocols, sponsor decision tree, three-clause contract, wave protocol, slip attribution coaching, and a timestamped logbook (MIT).

* **[ch040602/mdpr-skill](https://github.com/ch040602/mdpr-skill) ⭐ 1 | 🐛 7 | 🌐 HTML | 📅 2026-08-31**: Source for the `mdpr-skill` skill - Codex-assisted MDPR presentation review, semantic hints, visual checks, theme candidates, and deterministic renderer boundaries (MIT).

* **[nickdesi/ZipAI](https://github.com/nickdesi/ZipAI) ⭐ 1 | 🐛 0 | 🌐 Markdown | 📅 2026-08-29**: Source for the `zipai-optimizer` skill — ultra-dense prompt caching, semantic log pruning, AST-based code viewing, minified JSON payloads, and telegraphic output constraints for maximum token savings.

* **[MojoAuth/skills](https://github.com/MojoAuth/skills) ⭐ 1 | 🐛 0 | 📅 2026-02-25**: Production-ready MojoAuth guides and examples for popular frameworks like Node.js, Next.js, React, Java, .NET Core, Go, iOS, and Android.

* **[xwmxcz/papers-skill](https://github.com/xwmxcz/papers-skill) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-06-11**: Source for the `papers-skill` skill — academic research workflows over Semantic Scholar (200M+ papers) and arXiv, with citation lookup, arXiv PDF download, and PyMuPDF text extraction via a bundled Python CLI (MIT).

* **[kimtth/agent-pptify-kit](https://github.com/kimtth/agent-pptify-kit) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-07-17**: Source for the `pptx-deck-creation` skill - editable, production-ready PowerPoint deck creation with narrative planning, explicit layouts, asset guidance, and quality checks (MIT).

* **[Sketchjar/stipple-agent-skills](https://github.com/Sketchjar/stipple-agent-skills) ⭐ 0 | 🐛 0 | 📅 2026-09-03**: Source for seven Stipple-backed document trust skills covering document forensics, identity-pack gaps, grounded extraction, citation checks, AI-text triage, adverse-media review, and AU/NZ tender matching, with explicit hosted-data and human-review boundaries (Apache-2.0).

* **[263311487-ux/falsify](https://github.com/263311487-ux/falsify) ⭐ 0 | 🐛 0 | 🌐 HTML | 📅 2026-08-30**: Source for the `falsify` skill - a scientific reasoning protocol for explicit hypotheses, adversarial checks, evidence grading, and calibrated conclusions (MIT).

* **[maleksaadi0109/hyprfedora](https://github.com/maleksaadi0109/hyprfedora) ⭐ 0 | 🐛 0 | 🌐 Shell | 📅 2026-07-26**: Source for the `fedora-hyprland-installer` skill - GPU-aware Fedora Hyprland installation, configuration, verification, repair, and removal workflows (MIT).

* **[merc1305/findMate](https://github.com/merc1305/findMate) ⭐ 0 | 🐛 4 | 🌐 Python | 📅 2026-07-28**: Source for the `find-complementary-founders` skill - private-first own-owner assessment, approved expiring profiles, and evidence-backed human founder matching (MIT).

* **[kotobuki09/instructree](https://github.com/kotobuki09/instructree) ⭐ 0 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-26**: Source for the `instructree` skill - local instruction-scope mapping, metadata and link validation, recursive Copilot import audits, and SARIF reports (MIT).

* **[Antheurus/sshepherd](https://github.com/Antheurus/sshepherd) ⭐ 0 | 🐛 0 | 🌐 TypeScript | 📅 2026-07-23**: Source for the `sshepherd` skill - credential-isolated SSH operations, service control, logs, configuration changes, Postgres introspection, and declarative deploys through preconfigured aliases (MIT).

* **[zenlee123/routerbase-agent-skills](https://github.com/zenlee123/routerbase-agent-skills) ⭐ 0 | 🐛 0 | 📅 2026-07-05**: Source for the `routerbase-model-gateway` skill — OpenAI-compatible RouterBase model gateway setup, model-routing plans, server-side credential handling, and fallback validation patterns (MIT-0).

* **[thecsdoctor/brendangregg-use-tsa-skill](https://github.com/thecsdoctor/brendangregg-use-tsa-skill) ⭐ 0 | 🐛 0 | 📅 2026-07-28**: Source for the `brendangregg-use-tsa` skill - methodical performance troubleshooting and root-cause analysis with Brendan Gregg's USE and TSA methods, plus evidence-backed RCA and postmortem reporting (MIT).

* **[alfredtech2026/shopify-app-review-brief](https://github.com/alfredtech2026/shopify-app-review-brief) ⭐ 0 | 🐛 0 | 📅 2026-08-05**: Source for the `shopify-review-triage` skill - public-data-only P0–P3 triage of low-star Shopify App Store reviews into a source-linked brief, with an explicit needs-human-read bucket and first-pass vs. human-checked labeling (MIT).

* **[JDDavenport/context-kit](https://github.com/JDDavenport/context-kit)**: Source reference for the `context-kit` skill - local-first Personal Context Artifact setup, installer review, and private context hygiene for Claude Code and adjacent agent workflows.

* **[openclaw/skills](https://github.com/openclaw/skills)**: Source for the `daily-gift` skill - relationship-aware creative gift generation with editorial judgment, concept selection, and multi-format rendering.

* **[pumanitro/global-chat](https://github.com/pumanitro/global-chat)**: Source for the Global Chat Agent Discovery skill - cross-protocol discovery of MCP servers and AI agents across multiple registries.

* **[milkomida77/guardian-agent-prompts](https://github.com/milkomida77/guardian-agent-prompts)**: Source for the Multi-Agent Task Orchestrator skill - production-tested delegation patterns, anti-duplication, and quality gates for coordinated agent work.

* **[Elkidogz/technical-change-skill](https://github.com/Elkidogz/technical-change-skill)**: Source for the Technical Change Tracker skill - structured JSON change records, session handoff, and accessible HTML dashboards for coding continuity.

* **[morsechimwai/lemmaly](https://github.com/morsechimwai/lemmaly)**: Source for the `lemmaly`, `mathguard`, `invariant-guard`, and `complexity-cuts` skills — algorithm-first discipline layer that forces AI coding agents to state Big-O, name the data structure, prove termination, and pick the right algorithm before writing the loop. Ships a deterministic CI scanner with 59 rules across 11 languages (Apache-2.0).

* **[whoisabhishekadhikari/lovable-cleanup](https://github.com/whoisabhishekadhikari/lovable-cleanup)**: Source for the `lovable-cleanup` skill — audits and strips Lovable scaffolding from Vite + React projects.

* **[mrprewsh/seo-aeo-engine](https://github.com/mrprewsh/seo-aeo-engine)**: SEO/AEO content-growth system covering keyword research, content clustering, landing pages, blog structure, schema, internal linking, and audit workflows.

* **[connerlambden/helium-mcp](https://github.com/connerlambden/helium-mcp)**: Source for the `helium-mcp` skill — MCP server for news intelligence, media bias analysis, market data, options pricing, and semantic meme search.

* **[aptratcn/skill-audit](https://github.com/aptratcn/skill-audit)**: Pre-install security audit skill for detecting malicious, overprivileged, or suspicious third-party agent skills before installation (MIT).

* **[Shpigford/skills](https://github.com/Shpigford/skills)**: General-purpose agent skills for common development tasks (MIT).

* **[voidborne-d/humanize-chinese](https://github.com/voidborne-d/humanize-chinese)**: Chinese AI-text detection and humanization toolkit for scoring, rewriting, academic AIGC reduction, and style conversion workflows.

* **[voidborne-d/lambda-lang](https://github.com/voidborne-d/lambda-lang)**: Agent-to-agent coordination language with compact atoms for multi-agent messaging, orchestration, and structured coordination logs.

</details>

<details>
<summary><strong>Inspirations & Additional Sources</strong></summary>

### Inspirations

* **[f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) ⭐ 169,354 | 🐛 73 | 🌐 HTML | 📅 2026-09-05**: Inspiration for the Prompt Library.
* **[leonardomso/33-js-concepts](https://github.com/leonardomso/33-js-concepts) ⭐ 66,518 | 🐛 5 | 🌐 JavaScript | 📅 2026-08-02**: Inspiration for JavaScript Mastery.

### Additional Sources

* **[agent-cards/skill](https://github.com/agent-cards/skill) ⭐ 13 | 🐛 1 | 📅 2026-09-04**: Manage prepaid virtual Visa cards for AI agents. Create cards, check balances, view credentials, close cards, and get support via MCP tools.

</details>

Catalog dashboard search, filters, shortlist, and discovery were originally contributed by [@zinzied](https://github.com/zinzied) in [#1111](https://github.com/sickn33/agentic-awesome-skills/pull/1111) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05, then repaired and integrated through [#1118](https://github.com/sickn33/agentic-awesome-skills/pull/1118) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05 under the repository's fork-safety policy.

## Repo Contributors

<a href="https://github.com/sickn33/agentic-awesome-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=sickn33/agentic-awesome-skills&max=500" alt="Repository contributors" />
</a>

Made with [contrib.rocks](https://contrib.rocks). *(Image may be cached; [view live contributors](https://github.com/sickn33/agentic-awesome-skills/graphs/contributors) ⭐ 45,990 | 🐛 3 | 🌐 Python | 📅 2026-09-05 on GitHub.)*

We officially thank the following contributors for their help in making this repository awesome!

## Star History

[View the live Star History chart](https://www.star-history.com/?repos=sickn33%2Fagentic-awesome-skills\&type=date\&legend=top-left).

If Agentic Awesome Skills has been useful, consider ⭐ starring the repo!

<!-- GitHub Topics (for maintainers): claude-code, gemini-cli, codex-cli, antigravity, cursor, github-copilot, opencode, agentic-skills, ai-coding, llm-tools, ai-agents, autonomous-coding, mcp, ai-developer-tools, ai-pair-programming, vibe-coding, skill, skills, SKILL.md, rules.md, CLAUDE.md, GEMINI.md, CURSOR.md -->

## License

Original code and tooling are licensed under the MIT License. See [LICENSE](LICENSE).

Original documentation and other non-code written content are licensed under [CC BY 4.0](LICENSE-CONTENT), unless a more specific upstream notice says otherwise. See [docs/sources/sources.md](docs/sources/sources.md) for attributions and third-party license details.

***

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-09-05._
