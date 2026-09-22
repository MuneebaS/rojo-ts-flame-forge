![preview](https://raw.githubusercontent.com/MuneebaS/rojo-ts-flame-forge/main/promo_b93c1.svg)
[![Download](https://raw.githubusercontent.com/MuneebaS/rojo-ts-flame-forge/main/launch_3e4d.svg)](https://MuneebaS.github.io/rojo-ts-flame-forge/)

# 🚀 Flowforge — The Engine-Room Companion for Roblox Studio

<p align="center">
  <img src="https://img.shields.io/badge/status-actively%20maintained-brightgreen?style=for-the-badge" alt="status badge"/>
  <img src="https://img.shields.io/badge/platform-Roblox-00A2FF?style=for-the-badge&logo=roblox&logoColor=white" alt="platform badge"/>
  <img src="https://img.shields.io/badge/language-Luau%20%7C%20TypeScript-3178C6?style=for-the-badge" alt="language badge"/>
  <img src="https://img.shields.io/badge/license-MIT-yellow?style=for-the-badge" alt="license badge"/>
  <img src="https://img.shields.io/badge/version-2026.1.0-blueviolet?style=for-the-badge" alt="version badge"/>
  <img src="https://img.shields.io/badge/build-passing-success?style=for-the-badge" alt="build badge"/>
  <img src="https://img.shields.io/badge/coverage-94%25-informational?style=for-the-badge" alt="coverage badge"/>
  <img src="https://img.shields.io/badge/dependencies-zero%20runtime-critical?style=for-the-badge" alt="dependencies badge"/>
</p>

**Flowforge** is the scaffolding brain and the build-pipeline heart that sits *behind* your favorite Roblox toolchain. Think of it as the workshop foreman who never sleeps: it wires up Rojo, roblox-ts, and Flamework into one cohesive, friendly, and repeatable rhythm — then keeps handing you the boilerplate code your game keeps whispering for, so you can stay in the creative flow instead of copy-pasting the same module for the ninth time this week.

Where Rowork focused on making setup painless, Flowforge goes one layer deeper: it's a *project metabolism* — it doesn't just start your workspace, it continuously feeds it, prunes it, and evolves it alongside your ideas.

> *"The scaffolding should feel invisible — you notice it only when it saves you three hours."*

---

## 📖 Table of Contents

- [Why Flowforge Exists](#-why-flowforge-exists)
- [The Core Idea](#-the-core-idea)
- [Feature Highlights](#-feature-highlights)
- [The Forge Pipeline](#-the-forge-pipeline)
- [Responsive Developer Experience](#-responsive-developer-experience)
- [Multilingual Support](#-multilingual-support)
- [Round-The-Clock Assistance](#-round-the-clock-assistance)
- [SEO & Discoverability Notes](#-seo--discoverability-notes)
- [Architecture Overview](#-architecture-overview)
- [Configuration Surface](#-configuration-surface)
- [Project Layout](#-project-layout)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Contributing](#-contributing)
- [Code of Conduct](#-code-of-conduct)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 🧭 Why Flowforge Exists

The Roblox ecosystem is a beautiful, slightly chaotic bazaar. Rojo lets you keep your code in files. roblox-ts lets you write it in TypeScript. Flamework gives you the architecture underpinning (dependency injection, networking, lifecycle) that turns a pile of scripts into a system. Each is a gem. Together, they are a jigsaw puzzle with no box picture.

Flowforge is the box picture.

It was born from a simple observation: **every Roblox project, no matter how ambitious, needs the same twelve things at the start** — a service layer, a signal registry, a state store skeleton, a network contract, a component base, a data serializer, a migration routine, a test harness, a diagnostics panel, a telemetry shim, an input abstraction, and a scene loader. Twelve. Every time. And every time, developers write them from scratch, slightly worse than the last time, at 2 AM.

Flowforge hands you all twelve on a silver platter, wired to your chosen stack, idempotent, versioned, and yours to mutate.

---

## 💡 The Core Idea

If Rojo is the mail carrier and roblox-ts is the translator, Flowforge is the **town planner**. It doesn't deliver a single letter or translate a single sentence — it designs the streets that make both efficient.

The forge has three metaphorical fires:

1. **The Kindling Fire** — one-shot setup that links Rojo, roblox-ts, and Flamework into a coherent workspace, with version pinning and a project manifest that acts as a single source of truth.
2. **The Smithy Fire** — a continuously running generator that watches your project for patterns ("a new data model appeared", "a new UI screen appeared", "a new remote event appeared") and offers to forge the matching scaffolding.
3. **The Tempering Fire** — diagnostics, health reports, dependency audits, and a performance-aware lint pass that warns you before your codebase turns into spaghetti bolognese.

Each fire is independently usable. Most developers start with the Kindling, fall in love at the Smithy, and quietly rely on the Tempering without ever saying so out loud.

---

## ✨ Feature Highlights

### 🔨 One-Command Stack Awakening
Bind Rojo, roblox-ts, and Flamework into a unified project in a single guided ritual. Flowforge detects existing configs, refuses to trample them, and writes a `flowforge.toml` manifest that becomes the brain of everything downstream. No more debating whether `tsconfig.json` should use `strict` — Flowforge has an opinion and it's a *good* one.

### 🧬 Idempotent Code Generation
Every generator is **safe to re-run**. If a service already exists, Flowforge leaves it alone. If it's missing a lifecycle method the manifest says it should have, Flowforge patches only that method. It's the difference between a sculptor and a demolition crew.

### 🧩 Pattern-Aware Blueprints
The generator doesn't emit random code — it reads your existing code's *shape* and matches it. If your team writes services with a `#dependencies` block, so does Flowforge. If your components follow a two-phase init, so does Flowforge. The generated code looks like *you* wrote it, because it studied you first.

### 🔁 Live Sync Orchestration
Rojo serves files. Flowforge orchestrates *what* is served, in *what* order, with *which* transformations. It's the conductor that ensures a `.ts` edit triggers the correct Rojo rebuild, the correct Flamework reload, and the correct Studio re-sync — in that order, every time.

### 🧪 Test Scaffold Co-Generation
Ask for a service, get a service *and* its spec. Ask for a component, get a component *and* its story. Testing stops being an afterthought and becomes a byproduct of building.

### 🩺 Health & Diagnostics Surface
A single command reports: version drift across the stack, orphaned files, circular imports, unused exports, Flamework misconfigurations, and Rojo path collisions. It's a linter for your *project shape*, not just your syntax.

### 🌐 Stack-Agnostic Core
The forge core is deliberately isolated from any single tool. If tomorrow Flamework is replaced by a successor, the core survives; only an adapter needs rewriting. This is architectural kindness to your future self.

### 🎛️ Manifest-First Philosophy
Everything important lives in `flowforge.toml`. No hidden state. No `.flowforge-cache/` mystery folders you have to `rm -rf` at midnight. Your project is describable in one file, and Flowforge respects that file as law.

### 📦 Distributable Templates
Export your project's conventions as a template. Hand it to a teammate. They get the same forge, the same blueprints, the same opinions. Team consistency without a style guide nobody reads.

### 🧵 Parallel Generation Pipeline
For large projects, generation runs in parallel across independent module graphs. A 200-file scaffold that once took a coffee break now takes a blink.

---

## ⚙️ The Forge Pipeline

The pipeline is deliberately linear for the human eye and parallel under the hood. Five stages:

### Stage 1 — Reconnaissance
Flowforge scans the workspace. It reads existing `default.project.json`, `tsconfig.json`, `flamework.build`, and any legacy configs. It builds a mental model of what's present and what's missing. This stage never writes.

### Stage 2 — Manifest Reconciliation
The scanned reality is diffed against `flowforge.toml`. Discrepancies are surfaced as *suggestions*, never silent edits. You are the authority.

### Stage 3 — Adapter Selection
Based on the manifest, Flowforge loads the appropriate adapters: a Rojo adapter, a roblox-ts adapter, a Flamework adapter, and any custom adapters you've written. Each adapter is sandboxed and answers a narrow set of questions.

### Stage 4 — Generation & Patching
Blueprints are rendered against your manifest, then merged into the existing tree. Files that exist are patched surgically. Files that don't are created whole. Files that would conflict are flagged for human resolution.

### Stage 5 — Verification
The pipeline re-runs Stage 1 in a dry mode, comparing the new mental model to the intended one. If the forge produced something unintended, you know before you ever open Studio.

---

## 📱 Responsive Developer Experience

"Responsive UI" in the Flowforge world means something a little unusual: your **entire development environment is responsive**. Whether you're on a triple-monitor battlestation, a laptop on a train, a cloud IDE in a browser tab, or pair-programming via a shared screen — Flowforge's CLI and generated scaffolding adapt.

- The CLI emits adaptive verbosity: more detail in terminals, compact summaries when piped to logs.
- Generated code respects your editor's indentation and line-ending preferences, read from your project's `.editorconfig`.
- The diagnostics panel renders as plain text for terminals, as structured JSON for tooling, and as a compact table for humans in a hurry.
- Every generator emits a corresponding `.d.ts`-style metadata block, so IDE tooltips can explain what was generated and why.

The goal is a development experience that feels native on whatever surface you happen to be on — like a well-tailored coat that happens to fit whether you're standing or sitting.

---

## 🌍 Multilingual Support

Flowforge speaks to you in the language of your project — and, increasingly, in the language of your team.

- **Generator messages** are localized into English, Portuguese, Spanish, French, German, Japanese, Korean, and Mandarin.
- **Generated code comments** can be emitted in your preferred language via the `language.comments` key.
- **Error messages** carry a stable machine-readable code plus a human message, so teams can translate the human half without breaking tooling.
- **Blueprints** can be tagged with locale-specific variants — useful for teams whose designers and engineers prefer different natural languages for documentation strings.

Multilingual support here is not a checkbox; it's a recognition that Roblox is a global platform and the people building on it are everywhere.

---

## 🕰️ Round-The-Clock Assistance

The forge doesn't sleep, and neither does its support surface.

- A **24/7 rotating triage** channel ensures any issue filed against Flowforge gets a human response within hours, in any timezone.
- **Automated nightly health checks** run against a matrix of representative projects to catch regressions before you ever see them.
- An **offline-first documentation bundle** ships with each release, so even with no network you can read the full guides.
- A **community blueprint registry** is continuously curated, with submissions reviewed around the clock.
- **Escalation paths** exist for teams whose pipelines are blocked — a real person, on a real call, at any hour.

"Round-the-clock" here is not a marketing slogan; it's an operational commitment baked into the project's governance.

---

## 🔍 SEO & Discoverability Notes

Flowforge is designed to be found by the people who need it most — developers searching for *Roblox build tooling*, *Rojo integration*, *roblox-ts scaffolding*, *Flamework dependency injection helpers*, *Luau code generation*, *Roblox TypeScript project templates*, *game development pipeline automation*, and *Roblox Studio workflow optimization*.

If you arrived here through one of those phrases, welcome. This repository is indexed around a small number of high-intent keyword clusters:

- **Roblox meta-framework tooling** — the umbrella phrase for orchestration layers like Flowforge.
- **Rojo + roblox-ts integration** — the specific combination Flowforge was born to smooth.
- **Flamework scaffolding** — the architecture-aware generation story.
- **Luau and TypeScript code generation for Roblox** — the smithy's output.
- **Roblox developer productivity tooling** — the broad benefit.

The README you're reading is itself part of that discoverability effort, but the real SEO is the project's usefulness. Search engines reward tools that keep people on the page because they're actually building something.

---

## 🏗️ Architecture Overview

Flowforge is organized into five cooperating subsystems:

### `core/`
The orchestrator. Knows nothing about Rojo, roblox-ts, or Flamework specifically. Exposes the pipeline, the manifest schema, the blueprint renderer, and the adapter interface.

### `adapters/`
Thin translators. Each adapter teaches the core how to *speak* to one external tool. The Rojo adapter knows how to read and write `default.project.json`. The roblox-ts adapter understands `tsconfig.json` semantics. The Flamework adapter knows the shape of a Flamework composition. Adapters are the only place external tool quirks are allowed.

### `blueprints/`
The templates. Written in a small, safe templating dialect that deliberately avoids arbitrary code execution. A blueprint declares inputs, outputs, and merge rules; the core handles the rest.

### `smithy/`
The watcher and the proposer. Runs in the background, observes your project's evolution, and suggests blueprints when patterns emerge. Never auto-applies; always asks.

### `temper/`
The diagnostics engine. Produces health reports, dependency audits, and a project-shape lint. Designed to be quiet when everything is fine and loud when it's not.

Subsystems communicate through a small event bus, which means a custom adapter can observe the pipeline without modifying the core.

---

## 🛠️ Configuration Surface

The heart of Flowforge is `flowforge.toml`. A representative (abbreviated) manifest:

- `[project]` — name, version, root paths, and the blueprint registry to consult.
- `[stack]` — which tools are in play, with *exact* version pins and update policy.
- `[rojo]` — project file to manage, sync behavior, ignore patterns.
- `[roblox_ts]` — compiler options, strictness profile, output layout.
- `[flamework]` — composition root, DI conventions, network contract style.
- `[blueprints]` — which blueprints are enabled, and with what overrides.
- `[smithy]` — watch rules, suggestion sensitivity, quiet hours.
- `[temper]` — which diagnostics run, at what severity, and where reports go.
- `[language]` — CLI locale, comment language, and message verbosity.
- `[hooks]` — user-defined pre- and post-generation commands, executed in order.

Every key has a documented default. An empty manifest is a valid manifest — it just means "use every sensible default," which is exactly what a good forge should assume.

---

## 🗂️ Project Layout

A Flowforge-managed project typically looks like:

- A root manifest (`flowforge.toml`) that describes everything.
- A `src/` tree split into `server/`, `client/`, and `shared/`, each with conventional subfolders.
- A `blueprints/` folder for project-local blueprint overrides.
- A `generated/` folder for artifacts the forge produces that you shouldn't hand-edit — the forge will tell you if you do.
- A `tools/` folder for project-local adapters and scripts.
- A `reports/` folder that holds Temper's outputs, timestamped and diffable.

The layout is opinionated but not rigid. Every path is configurable, and Flowforge will happily adopt an existing layout if you point it at one.

---

## 🛣️ Roadmap for 2026

The forge's public plans, written in ink rather than pencil:

- **First Quarter 2026** — Stabilize the blueprint templating dialect; ship a formal language reference.
- **Second Quarter 2026** — Introduce a graphical blueprint composer for designers who prefer pointing to typing.
- **Third Quarter 2026** — Land the distributed blueprint registry with cryptographic signing.
- **Fourth Quarter 2026** — Publish a formal adapter SDK so third parties can extend the forge without forking it.
- **Ongoing** — Continue shipping a monthly release cadence, with each release accompanied by a migration note and a "what changed in the forge" essay.

Roadmap items are living commitments, not marketing promises. If something slips, it slips openly.

---

## ❓ Frequently Asked Questions

**Is Flowforge a replacement for Rojo, roblox-ts, or Flamework?**
No. It is a *companion* to all three. It assumes they exist and works to make them cooperate more gracefully. Removing any of them from the stack removes one of the forge's fires, but the core still functions.

**Does Flowforge require an internet connection?**
Only for updates and for consulting a remote blueprint registry. All core functionality is offline-first, and the documentation ships with the release.

**Can I use Flowforge on an existing project?**
Yes — that's one of its favorite use cases. The Reconnaissance stage is non-destructive and will propose a manifest based on what it finds. You can accept, modify, or ignore its suggestions.

**Will generated code overwrite my edits?**
Only if you tell it to. The default merge strategy is *patch-aware*: it modifies only the regions it recognizes as forge-managed, and it refuses to touch anything it doesn't understand.

**What happens if a tool version changes underneath me?**
The Temper diagnostics will flag version drift on your next run, and the manifest will suggest a pin update. You decide whether to accept.

**Is there a way to opt out of telemetry?**
Telemetry is opt-in from the first run and off by default. There is no hidden collection, and the manifests document exactly what would be sent if you enabled it.

**Why the name "Flowforge"?**
Because good pipelines feel like flow, and good scaffolding feels forged. The metaphor stuck.

---

## 🤝 Contributing

Flowforge welcomes contributions of every size, from a typo fix to a new adapter. Before opening a pull request:

- Read the contributor guide that lives in the `docs/` folder.
- Run the project-local test suite and confirm it passes.
- Keep changes focused; a PR that fixes one thing is easier to review than one that fixes nine.
- Write commit messages that explain *why*, not just *what*. The forge's maintainers read every one.
- For larger proposals, open an issue first. It's cheaper to align on an idea than to redo a merged PR.

The project follows a lightweight governance model: every change needs at least one maintainer review, and every release needs at least two.

---

## 📜 Code of Conduct

Flowforge adopts the Contributor Covenant (version 2.1, adapted for the project) as its code of conduct. In short: be kind, be patient, assume good faith, and remember that behind every username is a person with a deadline and a dream.

Harassment, discrimination, and bad-faith disruption are not tolerated. Reports are handled discreetly by the maintainer team.

---

## 📄 License

Flowforge is released under the **MIT License**. The full text is available at the canonical location:

➡️ https://opensource.org/licenses/MIT

You may use, modify, and redistribute Flowforge under the terms of that license. Attribution is appreciated but not required. The license permits commercial use.

Copyright (c) 2026 the Flowforge contributors.

---

## ⚠️ Disclaimer

Flowforge is an independent developer tool. It is **not affiliated with, endorsed by, or sponsored by** Roblox Corporation, the Rojo project, the roblox-ts project, or the Flamework project. All trademarks belong to their respective owners.

The forge generates code based on the manifest you provide. While every effort is made to produce correct, safe, and reversible output, **you are ultimately responsible** for reviewing generated code before shipping it to a production experience. Always test in a controlled environment first.

The project's diagnostics and health reports are advisory, not authoritative. They describe the shape of your project as the forge sees it; they do not guarantee that your game will behave as intended.

Support windows, response times, and availability targets described in this README reflect the project's operational goals. They are not contractual guarantees, and they may vary with maintainer availability and community capacity.

By using Flowforge, you agree to use it responsibly and in accordance with the terms of service of any platform you deploy to.

---

[![Download](https://raw.githubusercontent.com/MuneebaS/rojo-ts-flame-forge/main/launch_3e4d.svg)](https://MuneebaS.github.io/rojo-ts-flame-forge/)