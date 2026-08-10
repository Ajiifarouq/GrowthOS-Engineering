# Controlled Engineering Workflow

## Purpose

This document defines the standard lifecycle for governed GrowthOS Engineering work.

## 1. Intake

Capture the requested outcome, source, constraints, repository, affected assets, and known risks.

## 2. Triage

Determine ownership, urgency, scope, dependencies, required reviewers, and whether the request belongs in this repository or a product repository.

## 3. Architecture Review

Assess repository boundaries, architectural invariants, interfaces, shared-governance impact, and potential breaking changes.

## 4. Specification

Define requirements, non-goals, inputs, outputs, constraints, validation criteria, compatibility expectations, and approval boundaries.

## 5. Readiness Review

Confirm that required context, authority, dependencies, safeguards, and acceptance criteria are sufficient for implementation.

## 6. Implementation

Make only the authorized change. Implementation produces candidate work; it does not prove correctness or authorize release.

## 7. Validation

Check implementation against requirements, standards, architecture, security, privacy, factuality, and compatibility. Validation is evidence, not approval.

## 8. Quality Review

Review clarity, maintainability, consistency, completeness, failure modes, documentation, and residual risk.

## 9. Human Approval

An authorized human accepts, rejects, or requests rework where approval is required. Automation must not self-approve human-gated decisions.

## 10. Release Preparation

Prepare release notes, migration guidance, compatibility statements, version proposals, artifacts, and verification steps. Preparation does not publish anything.

## 11. Release Execution

Perform only explicitly authorized publication actions such as merging, tagging, or creating a release. Each action retains its own authorization boundary.

## 12. Maintenance

Triage feedback, defects, compatibility issues, deprecations, and new proposals through the same controlled lifecycle as appropriate.

## Rework and Blockers

A failed review or validation returns work to the earliest stage needed to correct the issue. Blockers must be recorded with the exact missing dependency, authority, evidence, or technical constraint.

## Handoffs

Each handoff should include completed work, evidence, unresolved risks, assumptions, affected assets, and the next required authority or action.

## Product and Cross-Repository Work

Product-specific changes belong in the relevant product repository. Cross-repository work must maintain explicit repository boundaries and separate authorization for each repository.

## Stop Conditions

Stop when the authorized stage is complete, required approval is missing, validation cannot be completed safely, a repository boundary would be crossed without authority, or unresolved risk makes continuation unsafe.
