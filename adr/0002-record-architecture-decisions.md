# ADR-0002: Record architecture decisions

- **Status:** Accepted
- **Date:** 2026-07-22
- **Deciders:** Project ATLAS maintainers
- **Tags:** governance, documentation, process

## Context

Project ATLAS is a long-lived, documentation-first knowledge base and portfolio.
Its guiding principle is that **the repository is the source of truth**, not any
single conversation. Significant decisions — which frameworks to adopt, how the
site is published, how content is structured — have until now lived in chat
threads and a planning PDF. That memory is fragile: it is not versioned, not
reviewable, and not portable across the AI tools and collaborators that
contribute to ATLAS.

We need a durable, low-friction way to capture decisions and, crucially, the
*reasoning* behind them, so that a reader (or a future AI session) can understand
not just what was chosen but why alternatives were rejected.

## Decision

We will record every significant architectural or process decision as an
**Architecture Decision Record (ADR)** in the [`adr/`](.) directory, following
the format defined in [`0001-template.md`](0001-template.md).

- ADRs are numbered sequentially and named `NNNN-kebab-case-title.md`.
- Each ADR is immutable once **Accepted**. A superseding decision is a new ADR
  that flips the prior record's status to *Superseded by ADR-NNNN*.
- ADRs are proposed and reviewed in pull requests, consistent with the ATLAS
  release workflow (`develop` → PR → `main`).

This ADR is itself the first record and establishes the practice.

## Consequences

**Positive**

- Decisions and their rationale become versioned, diffable, and reviewable.
- ATLAS stays consistent across ChatGPT, GitHub Copilot, and future agents,
  because the reasoning lives in the repository rather than in prompts.
- New contributors can reconstruct the project's history from `adr/` alone.

**Negative / costs**

- A small, recurring authoring cost: significant changes now require an
  accompanying ADR.
- Requires discipline to keep the ADR index current and to supersede rather than
  edit accepted records.

**Neutral**

- ADRs complement, but do not replace, the charter ([`PROJECT.md`](../PROJECT.md))
  and the changelog. The charter states current conventions; ADRs record how and
  why those conventions came to be.

## Alternatives considered

- **Keep decisions in chat threads / the planning PDF** — rejected: not
  versioned, not reviewable, and lost when a conversation ends.
- **A single running `DECISIONS.md` log** — rejected: grows unwieldy, invites
  editing of past entries, and lacks the per-decision context/consequence
  structure that makes decisions auditable.
- **Capture decisions only in commit messages** — rejected: too granular and
  hard to discover; commit messages describe changes, not the weighing of
  alternatives.

## References

- Michael Nygard, ["Documenting Architecture Decisions"](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [MADR — Markdown Architectural Decision Records](https://adr.github.io/madr/)
- Project charter: [`PROJECT.md`](../PROJECT.md)
