# Project ATLAS

**Enterprise AI Platform Architect Playbook** — a Git-based, documentation-first
knowledge base and portfolio on building and operating production AI platforms.

ATLAS is written for senior engineers and architects. It optimizes for
enterprise production systems — reliability, security, evaluation, observability,
cost, and governance — not tutorials. The repository is the source of truth: every
decision lives here, versioned and reviewable.

## Why ATLAS exists

- **A durable body of architecture knowledge.** Opinionated, trade-off-driven
  guidance on enterprise AI platforms, not demos.
- **A working portfolio.** Evidence of architect-level judgment: boundaries,
  failure modes, and production concerns.
- **A tool-agnostic playbook.** Conventions live in the repository, so ATLAS stays
  consistent across ChatGPT, GitHub Copilot, and future AI agents.

## Principles

- **Build systems, not demos.**
- **Documentation as code** — versioned, reviewed, and published from Git.
- **Learn by building** — every concept is grounded in a production concern.

## How the knowledge base is written

Every knowledge document under [`docs/`](docs/) answers seven questions, in order:

1. What is it?
2. Why does it matter?
3. When should I use it?
4. When should I avoid it?
5. How does it fit into an Enterprise AI Platform?
6. How does it apply to Cavosh Innovation?
7. How would I explain it in an interview?

The full house style and governance model are defined in the project charter,
[`PROJECT.md`](PROJECT.md) — read it first.

## Repository layout

| Path | Purpose |
|---|---|
| [`PROJECT.md`](PROJECT.md) | Internal charter — the project's memory and context |
| [`ROADMAP.md`](ROADMAP.md) | 12-month, quarterly roadmap |
| [`CHANGELOG.md`](CHANGELOG.md) | Release history (Keep a Changelog + SemVer) |
| [`docs/`](docs/) | Published knowledge base (the seven-question documents) |
| [`adr/`](adr/) | Architecture Decision Records |
| [`getting-started/`](getting-started/) | Runnable examples (e.g. Promptfoo evaluation) |
| [`mkdocs.yml`](mkdocs.yml) | Material for MkDocs site configuration |

## Roadmap at a glance

| Quarter | Theme | Focus |
|---|---|---|
| Q1 | Foundations | AI-300, Azure AI, Retrieval-Augmented Generation |
| Q2 | Quality | Evaluation, guardrails |
| Q3 | Operations | Observability, agent-to-agent (A2A) systems |
| Q4 | Platform | Platform engineering and portfolio consolidation |

See [`ROADMAP.md`](ROADMAP.md) for the authoritative version.

## Running the documentation site

ATLAS is published with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

```bash
pip install mkdocs-material
mkdocs serve   # live preview at http://127.0.0.1:8000
mkdocs build   # render the static site into ./site
```

## Contributing

ATLAS is developed as a real open-source project: work lands on `develop` and
reaches `main` through reviewed pull requests, and `main` is always publishable.
Conventions, the Definition of Done, and the release strategy are documented in
[`PROJECT.md`](PROJECT.md). AI contributors additionally follow
[`.github/copilot-instructions.md`](.github/copilot-instructions.md).
