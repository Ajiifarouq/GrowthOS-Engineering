# Agent Operating Requirements

## Purpose

This document defines mandatory operating behavior for AI agents and automated engineering actors working in GrowthOS Engineering.

## Required Start Sequence

Before changing repository content, an agent must:

1. Verify the repository identity and intended branch.
2. Inspect current repository state and relevant history.
3. Read [CODEX.md](CODEX.md).
4. Read governance documents relevant to the requested change.
5. Identify the exact authorized scope.
6. Preserve unrelated existing work.

## Scope Discipline

Agents must modify only explicitly authorized files, branches, or resources. They must not expand a task merely because adjacent work appears useful.

## Existing-Work Protection

Do not overwrite, delete, rename, reformat, or supersede unrelated work without explicit authorization. When conflicting instructions or unexpected repository state are discovered, stop or constrain work to the safe subset.

## Validation

Agents must validate changed artifacts against applicable architecture, standards, workflow, security, privacy, factuality, and compatibility requirements before reporting completion.

## Git and Publication Boundaries

Without explicit authorization, agents must not:

- commit or push changes;
- create pull requests;
- modify the default branch;
- merge branches or pull requests;
- create or move tags;
- create releases;
- publish artifacts;
- alter repository visibility;
- perform destructive history rewrites;
- modify another repository.

Authorization for one action does not automatically authorize the next action.

## Reporting

Completion reports must distinguish intended work from verified results. Never claim that a remote branch, commit, file, merge, tag, release, or deployment exists without evidence.

## Stop Conditions

Stop when:

- the authorized scope is complete;
- required authority is missing;
- repository identity is uncertain;
- an operation would affect unrelated work;
- required validation cannot be performed;
- a security, privacy, or factuality issue cannot be resolved safely.
