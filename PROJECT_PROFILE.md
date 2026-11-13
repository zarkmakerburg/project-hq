# Project Profile — Project HQ

This profile binds the reusable HQ operating methodology to the repository that maintains the methodology itself. It is not a consumer-project profile.

## Identity

- **Project:** Project HQ
- **Repository:** https://github.com/zarkmakerburg/project-hq
- **Default branch:** `main`
- **Canonical operations / decisions / evidence board:** https://github.com/zarkmakerburg/project-hq/issues/1
- **Independent roadmap:** NONE (Issue #1 is the canonical operations board only, not a roadmap).
- **Purpose:** maintain the reusable HQ playbook, command contracts, templates and integration guidance.

## Scope and isolation

- This repository owns only the generic operating method.
- Consumer projects must keep their own repository, project profile, canonical board, evidence, permissions, credentials, environments and release state.
- Do not add consumer-project identifiers, host inventories, secrets, approvals or operational history to this repository.
- The HQ repository's own board is not a substitute for any consumer project's board.

## Environments and permissions

- No LAB or production hosts are registered for Project HQ.
- No real-host operations are in scope.
- Merge, release and publishing remain separate gates governed by repository settings and explicit owner authorization.
- The playbook does not grant tool access, install plugins, or configure ChatGPT account settings.

## Continuation commands

When HQ is active and this profile is bound, interpret the user's shorthand as follows:

| Command | Required behavior |
|---|---|
| `.` | Continue the current task from its latest verified state. Perform the next safe, authorized action; if no task is active, follow the `..` behavior; do not replace execution with a status-only recap. |
| `..` | Reinspect the currently open tasks on the canonical board, prioritize them using current dependencies, risks and acceptance gates, then execute the highest-priority safe task. |
| `...` | Disabled as a distinct roadmap mode while `roadmap: NONE`; report `Roadmap: NONE` and follow the `..` behavior. Enable roadmap reassessment only after the owner declares an independent roadmap in this profile. |

All continuation commands remain subordinate to security policy, project isolation, required approvals and independent merge/release/deploy gates. A shorthand command never grants authority for a gated action. The canonical operations board is not a roadmap. Do not infer roadmap priorities from Issue #1.

These meanings apply only while HQ is active and this profile is bound. They do not override `HQ OFF` or automatically configure other chats.
