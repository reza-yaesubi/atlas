# Changelog

All notable changes to Project ATLAS are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.0] - 2026-07-22

### Added

- **PR #1 — Repository Foundation.** Establishes the scaffolding, conventions,
  and governance the rest of ATLAS builds on.
  - `PROJECT.md` — internal charter: mission, audience, writing style (the
    seven-question framework), technology choices, repository conventions,
    roadmap, Definition of Done, and release strategy.
  - `.github/copilot-instructions.md` — repository-level AI guidance so every AI
    tool contributes under the same conventions.
  - `README.md` — public front door derived from the charter.
  - `docs/index.md` — documentation landing page and information architecture.
  - `mkdocs.yml` — Material for MkDocs configuration with navigation, Mermaid
    support, and light/dark palette.
  - `adr/0001-template.md` — Architecture Decision Record template.
  - `adr/README.md` — ADR index, conventions, and workflow.
  - `adr/0002-record-architecture-decisions.md` — first ADR, adopting ADRs as the
    decision-record mechanism.
