# Engineering Prompt Library

## Canonical Prompt Structure

Reusable engineering prompts should use:

1. **Role** — the responsibility and authority boundary.
2. **Task** — the exact work to perform.
3. **Context** — repository state, constraints, evidence, risks, and guardrails.
4. **Format** — required output and verification structure.
5. **Tone** — communication characteristics appropriate to the task.

## Prompt Metadata

When a reusable prompt needs stable lifecycle management, define:

- **Prompt ID:** lowercase kebab-case.
- **Version:** only when independently maintained.
- **Status:** Draft, Proposed, Active, Deprecated, Retired, or Unreleased.
- **Owner:** accountable maintainer.

## Required Inputs

Prompts must identify inputs necessary for correct execution, especially repository, branch, scope, affected files, source material, validation criteria, and protected actions.

## Missing-Input Behavior

Do not invent material facts. If missing information blocks safe execution, stop and identify the missing input. If a safe constrained interpretation exists, make it explicit.

## Repository Scope

Prompts must identify the repository or repository class they govern. Cross-repository work requires explicit boundaries and authority for every repository changed.

## Evidence and Factuality

A prompt must not instruct an agent to claim remote state, test success, approval, release, user adoption, metrics, or other facts without evidence.

## Privacy and Security

Prompts must prohibit disclosure of secrets and unnecessary personal or sensitive data and must preserve applicable access and approval boundaries.

## Validation and Approval

Prompts should specify validation appropriate to the task. Validation must remain distinct from human approval. Commit, push, PR creation, merge, tagging, release, and publication may each require separate authorization.

## Stop Conditions

Every execution-oriented prompt should define when the agent must stop rather than expanding scope.

## Compatibility and Maintenance

Reusable prompts should be reviewed when repository governance, tools, interfaces, or approval boundaries change. Breaking prompt behavior should be versioned and migrated where consumers depend on it.

## Reusable Templates

### `repository-readiness-review`

**Role:** Repository readiness reviewer.  
**Task:** Inspect a specified repository and report blockers before implementation.  
**Context:** Use verified repository state; do not modify files or protected Git state.  
**Format:** Scope, findings, evidence, blockers, next permitted action.  
**Tone:** Factual and concise.

### `scoped-implementation`

**Role:** Repository engineer.  
**Task:** Implement only the approved file-level scope.  
**Context:** Preserve unrelated work; obey [CODEX.md](CODEX.md), [ARCHITECTURE.md](ARCHITECTURE.md), and [PROJECT_STANDARDS.md](PROJECT_STANDARDS.md).  
**Format:** Changes, validation, unresolved issues, protected actions not performed.  
**Tone:** Precise and execution-focused.

### `validation-review`

**Role:** Validation engineer.  
**Task:** Validate a candidate change against explicit acceptance criteria.  
**Context:** Validation is not approval; do not modify the candidate unless remediation is separately authorized.  
**Format:** Checks, evidence, failures, limitations, disposition.  
**Tone:** Evidence-driven.

## Product Boundary

This library intentionally contains shared engineering prompts only. Freelancer Growth OS and other product-specific prompts belong in their product repositories.
