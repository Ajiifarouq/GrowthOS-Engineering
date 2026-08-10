# Versioning and Compatibility

## Purpose

This document defines versioning, compatibility, migration, deprecation, tagging, and release-authority rules for GrowthOS Engineering artifacts.

## Repository Status

Current repository status: **Active**.

Current release candidate: **`0.1.0`**.

No prior semantic version has been formally released. Release candidate `0.1.0` becomes a published release only when the immutable release tag `v0.1.0` and the corresponding GitHub release both target the exact approved release commit.

## Semantic Versioning

Formal releases use semantic versioning in the form `MAJOR.MINOR.PATCH` when it accurately represents compatibility impact.

- MAJOR: approved breaking change.
- MINOR: backward-compatible capability or governance addition.
- PATCH: backward-compatible correction or clarification.

## Pre-1.0 Policy

Before `1.0.0`, compatibility expectations must still be documented. Pre-1.0 does not mean changes are consequence-free. Breaking changes require explicit identification and migration consideration.

## Artifact Versions

Repository, document, module, prompt, and template versions may be tracked independently when their consumers require stable references. Do not add version fields without a real maintenance need.

## Compatibility Classes

A change may be:

- backward compatible;
- conditionally compatible;
- breaking;
- deprecated but supported;
- retired.

## Breaking Changes

Breaking changes require impact analysis, affected-consumer identification where knowable, migration guidance, approval, and an appropriate version change once release versioning is active.

## Migration

Migration guidance should state the old behavior, new behavior, required consumer action, validation, rollback or recovery considerations where applicable, and unresolved limitations.

## Deprecation and Retirement

Deprecation communicates that an artifact remains available but should no longer be adopted for new use. Retirement ends supported use. Neither state should be declared without authority and clear compatibility consequences.

## Git Tags

Tags represent approved release points only. Release tags use the form `vMAJOR.MINOR.PATCH`. Do not create or move a release tag without explicit release authority. Published release tags are immutable; correction normally requires a new release rather than rewriting history.

## Release Withdrawal

If a release must be withdrawn, preserve traceability. Document the reason, affected scope, recommended replacement or mitigation, and approving authority. Do not erase release history to simulate nonexistence.

## Human Release Authority

Automation may prepare release materials and execute explicitly authorized release actions, but it cannot grant itself release approval.
