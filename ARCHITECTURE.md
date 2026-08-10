# GrowthOS Engineering Architecture

## Purpose

This document defines the shared governance architecture and repository boundaries for GrowthOS Engineering.

## Architectural Responsibility

GrowthOS Engineering owns reusable engineering governance, including standards, lifecycle controls, versioning rules, templates, engineering roles, and prompt-governance patterns.

GrowthOS product repositories own product-specific requirements, domain behavior, implementation, interfaces, data models, customer workflows, deployment choices, and product roadmaps.

## Dependency Direction

The permitted governance dependency direction is:

`Product repository → GrowthOS Engineering`

GrowthOS Engineering must not depend on product-specific logic as a prerequisite for its shared rules.

## Source-of-Truth Rules

- Shared engineering governance: GrowthOS Engineering.
- Product-specific implementation and behavior: the relevant product repository.
- Approved deviations: documented where the deviation is applied, with rationale, scope, compatibility impact, and approval authority.

## Extensions

A product may extend shared governance when the extension:

- does not contradict a shared architectural invariant;
- is clearly identified as product-specific;
- has a defined scope;
- does not silently redefine the shared source of truth.

## Deviations

A deviation must identify the shared rule, reason, affected scope, risk, validation, compatibility impact, owner, and approval. Temporary deviations should include an exit or review condition without inventing dates.

## Architectural Invariants

- Shared governance remains product-agnostic.
- Product logic remains outside this repository.
- Human approval boundaries cannot be delegated implicitly to automation.
- Repository changes must preserve traceability.
- Compatibility and migration impact must be considered for breaking governance changes.
- Security, privacy, and factuality constraints cannot be bypassed by local convenience.

## Change Classification

Changes should be classified as one or more of:

- editorial;
- compatible governance clarification;
- compatible capability addition;
- behavioral change;
- breaking governance change;
- deprecation;
- retirement;
- security or privacy change.

Classification informs review, versioning, compatibility, and migration requirements.

## Out of Scope

This repository does not define Freelancer Growth OS features, customers, pricing, product-specific prompts, product UI, domain workflows, or deployment implementation.
