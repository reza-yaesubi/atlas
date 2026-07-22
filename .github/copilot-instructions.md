# Copilot Instructions — Project ATLAS

These instructions apply to the entire repository. Every AI contributor
(GitHub Copilot, ChatGPT, Codex, and future agents) must follow them.

**Read [`PROJECT.md`](../PROJECT.md) first.** It is the project charter and the
source of context. When a prompt conflicts with `PROJECT.md` or the Git history,
the repository wins.

## What ATLAS is

A Git-based, documentation-first knowledge base and portfolio on building and
operating **enterprise AI platforms**, written for senior engineers and
architects. It optimizes for production systems, not tutorials.

## Non-negotiable rules

- **Git is the source of truth.** Do not rely on chat memory; encode decisions in
  the repository.
- **No placeholders, no `TODO`s, no filler.** If content is not ready, do not
  commit it. Produce complete, production-quality Markdown.
- **Write for senior engineers and architects.** Explain trade-offs, boundaries,
  and failure modes — not fundamentals.
- **Be concise, practical, and opinionated.** Lead with the decision, then the
  rationale. Take a position.
- **Prefer Mermaid** diagrams over binary images; keep them inline so they are
  diffable.
- **Prefer an ADR over a long discussion.** Capture significant decisions in
  `adr/` using the project ADR template.
- **Reference official documentation** (Microsoft Learn, Azure Architecture
  Center, AWS Prescriptive Guidance) where it strengthens a claim.
- **Optimize for enterprise production systems**: reliability, security,
  evaluation, observability, cost, and governance.

## Writing style

Draw inspiration from Microsoft Learn, the Azure Architecture Center, AWS
Prescriptive Guidance, Martin Fowler, and the Thoughtworks Technology Radar.

### The seven questions

Every **knowledge document** under `docs/` must answer, in order:

1. What is it?
2. Why does it matter?
3. When should I use it?
4. When should I avoid it?
5. How does it fit into an Enterprise AI Platform?
6. How does it apply to Cavosh Innovation?
7. How would I explain it in an interview?

Meta and governance files (`README.md`, `LICENSE`, `CONTRIBUTING.md`,
`CHANGELOG.md`, `mkdocs.yml`, ADRs) are exempt and follow their own formats.

## Conventions

- Documentation is published with **Material for MkDocs**; update `mkdocs.yml`
  navigation when adding or moving published content.
- `CHANGELOG.md` follows **Keep a Changelog** with **Semantic Versioning**.
- Work in small, reviewable increments. Feature work lands on `develop` and
  reaches `main` through reviewed pull requests; `main` is always publishable.
- Definition of Done: complete documentation (seven questions for knowledge
  docs), a diagram where it clarifies, an ADR for significant decisions, updated
  navigation and changelog, and a clean docs build.
