# Engineering Role Library

## Role Contract

Each role is a reusable responsibility boundary, not an automatic grant of GitHub or release authority. Eligible actors may include humans or automation only where the task and platform permit it. Explicit authorization remains required for protected actions.

## `repository-engineer`

**Responsibility:** Implement scoped repository changes.  
**Permitted actors:** Authorized humans or automation.  
**Permitted actions:** Inspect repository state; edit authorized files; run validation.  
**Prohibited actions:** Unapproved cross-repository changes, merges, releases, force pushes.  
**Inputs:** Approved scope, repository state, requirements.  
**Outputs:** Candidate repository changes and evidence.  
**Validation:** Standards, tests, diff review.  
**Handoff:** Validation or quality review.  
**Approval boundary:** Protected Git actions remain separately authorized.  
**Stop conditions:** Scope complete, blocker, missing authority.

## `architecture-integrity-reviewer`

**Responsibility:** Protect architectural boundaries and invariants.  
**Permitted actors:** Qualified human or authorized review agent.  
**Permitted actions:** Analyze architecture impact and deviations.  
**Prohibited actions:** Self-approve exceptions requiring human authority.  
**Inputs:** Proposed change, architecture, dependencies.  
**Outputs:** Findings, risks, required remediation.  
**Validation:** Trace findings to architecture rules.  
**Handoff:** Specification, remediation, or human approval.  
**Approval boundary:** Architecture exceptions require designated authority.  
**Stop conditions:** Missing context or unresolved boundary violation.

## `standards-engineer`

**Responsibility:** Maintain and apply project standards.  
**Permitted actors:** Authorized human or automation.  
**Permitted actions:** Review naming, structure, metadata, links, evidence, and formatting.  
**Prohibited actions:** Expand standards into product behavior without authority.  
**Inputs:** Standards and candidate artifacts.  
**Outputs:** Compliance findings or scoped updates.  
**Validation:** Standards checklist.  
**Handoff:** Repository engineer or quality reviewer.  
**Approval boundary:** Breaking standards changes require governance approval.  
**Stop conditions:** Conflict with higher-level architecture or policy.

## `workflow-engineer`

**Responsibility:** Maintain lifecycle, handoff, and approval-flow integrity.  
**Permitted actors:** Authorized human or automation.  
**Permitted actions:** Analyze and improve workflow definitions.  
**Prohibited actions:** Remove approval gates without authority.  
**Inputs:** Workflow, process evidence, requirements.  
**Outputs:** Workflow changes or findings.  
**Validation:** Stage, transition, blocker, and stop-condition review.  
**Handoff:** Quality or governance review.  
**Approval boundary:** Governance-significant workflow changes require approval.  
**Stop conditions:** Unsafe or unauthorized gate removal.

## `versioning-compatibility-engineer`

**Responsibility:** Classify compatibility and version impact.  
**Permitted actors:** Qualified human or authorized automation.  
**Permitted actions:** Assess breaking changes, migration, deprecation, version proposals.  
**Prohibited actions:** Create release tags or declare releases without authority.  
**Inputs:** Change set, consumers, versioning policy.  
**Outputs:** Compatibility classification and migration requirements.  
**Validation:** Compare behavior before and after change.  
**Handoff:** Release preparation or remediation.  
**Approval boundary:** Release/version approval remains human-gated where required.  
**Stop conditions:** Unknown impact prevents defensible classification.

## `documentation-engineer`

**Responsibility:** Create and maintain accurate engineering documentation.  
**Permitted actors:** Authorized human or automation.  
**Permitted actions:** Draft, edit, link, and structure documentation.  
**Prohibited actions:** Invent facts, approvals, releases, customers, or evidence.  
**Inputs:** Verified requirements and source material.  
**Outputs:** Documentation artifacts.  
**Validation:** Accuracy, links, structure, terminology.  
**Handoff:** Quality reviewer.  
**Approval boundary:** Publication remains separately authorized.  
**Stop conditions:** Required facts are unavailable.

## `validation-engineer`

**Responsibility:** Produce evidence that implementation satisfies requirements.  
**Permitted actors:** Qualified human or automation.  
**Permitted actions:** Run tests, checks, static validation, and acceptance criteria.  
**Prohibited actions:** Equate validation with approval.  
**Inputs:** Requirements and implementation.  
**Outputs:** Validation evidence and failures.  
**Validation:** Reproducible checks where practical.  
**Handoff:** Quality reviewer or remediation.  
**Approval boundary:** Cannot self-authorize merge or release.  
**Stop conditions:** Required environment or evidence unavailable.

## `quality-reviewer`

**Responsibility:** Evaluate completeness, clarity, maintainability, and residual risk.  
**Permitted actors:** Qualified human or review automation.  
**Permitted actions:** Review artifacts and validation evidence.  
**Prohibited actions:** Conceal unresolved defects or grant unauthorized release approval.  
**Inputs:** Candidate work and evidence.  
**Outputs:** Findings, disposition recommendation, rework requests.  
**Validation:** Trace findings to requirements and standards.  
**Handoff:** Human approval or remediation.  
**Approval boundary:** Recommendation is not release authority.  
**Stop conditions:** Critical evidence missing.

## `security-privacy-reviewer`

**Responsibility:** Review security and privacy risk.  
**Permitted actors:** Qualified human or authorized review automation.  
**Permitted actions:** Identify exposure, unsafe defaults, data risks, and required controls.  
**Prohibited actions:** Approve exceptions beyond delegated authority or expose sensitive material.  
**Inputs:** Change set, data flows, threat context.  
**Outputs:** Findings and required mitigations.  
**Validation:** Security/privacy controls and evidence.  
**Handoff:** Remediation or authorized approval.  
**Approval boundary:** High-risk exceptions remain explicitly human-approved.  
**Stop conditions:** Unresolved critical risk.

## `release-preparation-engineer`

**Responsibility:** Prepare an approved candidate for release execution.  
**Permitted actors:** Authorized human or automation.  
**Permitted actions:** Prepare notes, migration guidance, artifacts, checks, and proposed version.  
**Prohibited actions:** Merge, tag, publish, or release without separate authority.  
**Inputs:** Approved candidate, validation, compatibility assessment.  
**Outputs:** Release package and verification plan.  
**Validation:** Completeness and release-readiness checks.  
**Handoff:** Release execution authority.  
**Approval boundary:** Preparation does not grant publication rights.  
**Stop conditions:** Candidate not approved or evidence incomplete.

## `release-execution-engineer`

**Responsibility:** Execute explicitly approved release actions.  
**Permitted actors:** Human or automation with exact release authorization.  
**Permitted actions:** Only the approved merge, tag, release, or publication operations.  
**Prohibited actions:** Expanding scope, force rewriting history, unapproved publication.  
**Inputs:** Approved release package and exact authorization.  
**Outputs:** Verified release state and execution evidence.  
**Validation:** Confirm resulting remote state.  
**Handoff:** Maintenance.  
**Approval boundary:** Cannot grant itself authorization.  
**Stop conditions:** Any mismatch between approval and requested operation.
