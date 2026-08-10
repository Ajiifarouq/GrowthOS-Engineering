# GrowthOS Engineering

**Status:** Active  
**Maturity:** Foundation  
**Release candidate:** `0.1.0`  
**Repository:** `Ajiifarouq/GrowthOS-Engineering`

## Purpose

GrowthOS Engineering is the shared engineering-governance source for GrowthOS product repositories. It defines reusable architecture rules, project standards, workflows, versioning policy, document and module templates, engineering roles, and prompt-governance patterns.

## Scope

This repository governs shared engineering practices that may be adopted by GrowthOS product repositories. Product-specific behavior, domain logic, customer workflows, commercial claims, and product roadmaps belong in their respective product repositories.

## Repository Relationship

GrowthOS product repositories may depend on and adopt governance from GrowthOS Engineering. The dependency direction is product repository → GrowthOS Engineering. GrowthOS Engineering must not import product-specific implementation logic back into shared governance.

## Foundation Documents

- [AGENTS.md](AGENTS.md) — agent operating requirements.
- [CODEX.md](CODEX.md) — authority and execution governance.
- [ARCHITECTURE.md](ARCHITECTURE.md) — shared architecture boundaries.
- [PROJECT_STANDARDS.md](PROJECT_STANDARDS.md) — repository and documentation standards.
- [WORKFLOW.md](WORKFLOW.md) — controlled engineering lifecycle.
- [VERSIONING.md](VERSIONING.md) — versioning and compatibility rules.
- [DOCUMENT_TEMPLATE.md](DOCUMENT_TEMPLATE.md) — canonical governance-document template.
- [MODULE_TEMPLATE.md](MODULE_TEMPLATE.md) — canonical module specification template.
- [ROLE_LIBRARY.md](ROLE_LIBRARY.md) — reusable engineering roles.
- [PROMPT_LIBRARY.md](PROMPT_LIBRARY.md) — reusable engineering prompt patterns.
- [CHANGELOG.md](CHANGELOG.md) — release and unreleased change record.
- [ROADMAP.md](ROADMAP.md) — governance roadmap.

## Source of Truth

For shared engineering governance, this repository is authoritative unless an approved product-level extension explicitly narrows or extends a rule without contradicting a shared invariant. Product repositories remain authoritative for product-specific behavior.

## Release State

This baseline is prepared as release candidate `0.1.0`. It is considered formally released only when the immutable release tag `v0.1.0` and the corresponding GitHub release both target the exact approved release commit. Until both publication steps are verified, `0.1.0` remains a release candidate rather than a published release.
