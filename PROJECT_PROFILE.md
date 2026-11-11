# Project Profile — Project HQ

This profile binds the reusable HQ operating methodology to the repository that maintains the methodology itself. It is not a consumer-project profile.

## Identity

- **Project:** Project HQ
- **Repository:** https://github.com/zarkmakerburg/project-hq
- **Default branch:** `main`
- **Canonical operations / decisions / evidence board:** https://github.com/zarkmakerburg/project-hq/issues/1
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

## Continuation

For work on this repository, continue from the latest verified state when the user sends `.` or `..` in a conversation where HQ is active. This rule does not override `HQ OFF`.
