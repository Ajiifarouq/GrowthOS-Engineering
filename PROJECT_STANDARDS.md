# Project Standards

## Purpose

These standards define consistent repository, documentation, identifier, evidence, privacy, security, and validation practices for GrowthOS Engineering.

## Markdown

- Use one H1 per Markdown file.
- Use descriptive H2/H3 headings beneath the H1.
- End text files with a newline.
- Prefer relative links for repository-local references.
- Keep normative requirements distinct from examples and proposals.

## File and Directory Naming

- Governance documents at repository root use descriptive uppercase names where established by this foundation.
- Reusable machine-oriented directories and IDs should use lowercase kebab-case unless a documented exception applies.
- Avoid ambiguous abbreviations.

## Metadata and Status

Where metadata is required, include only fields that are meaningful to the artifact. Approved status terms are:

- Draft
- Proposed
- Active
- Deprecated
- Retired
- Unreleased

Do not imply approval or release from file existence alone.

## Reusable Identifiers

Use lowercase kebab-case for reusable identifiers unless an approved exception is documented.

Examples:

- role: `validation-engineer`
- prompt: `repository-readiness-review`
- module: `compatibility-checker`

Identifiers should be stable once externally referenced.

## Links

Repository-local links must resolve. External links should be authoritative where practical and must not be represented as verified if they were not checked.

## Placeholders and Examples

Use explicit placeholders such as `[owner]`, `[version]`, or `[evidence]`. Examples must be labeled or clearly recognizable and must not be mistaken for production facts.

## Evidence and Factuality

Claims about repository state, test results, releases, users, customers, adoption, metrics, or approvals require evidence appropriate to the claim. Never fabricate missing evidence.

## Privacy and Security

Do not commit credentials, secrets, tokens, private keys, unnecessary personal data, or sensitive operational details. Minimize data collection and exposure.

## Validation

Validation should be proportional to the change and may include structure checks, link checks, schema checks, tests, compatibility analysis, security review, privacy review, and manual inspection.

## Exceptions

Exceptions must document:

- the rule being excepted;
- rationale;
- scope;
- risk;
- compensating controls where relevant;
- approving authority;
- review or exit condition where relevant.
