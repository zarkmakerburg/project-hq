# Project HQ — Reusable Engineering Command Center

Project HQ is a project-agnostic operating playbook for coordinating ChatGPT conversations, humans, AI agents, connected tools and engineering work. It is **not** a product runtime, hosted service, agent daemon or permission system.

## Quick commands

- `HQ ON` — activate this playbook for the current conversation/session. Read `AGENTS.md`, bind exactly one project profile, inspect its live sources of truth, then operate within its permissions and gates.
- `HQ OFF` — suspend HQ behavior for the current conversation/session and return to ordinary assistant behavior. Do not initiate project operations under HQ rules while off.
- `HQ STATUS` — report whether HQ is active in the current conversation, which project profile is bound, and any unavailable capabilities or blockers.

These are conversational control commands, not GitHub CLI commands or globally persistent switches. A new chat does not automatically inherit the state. To make HQ available in a new chat, attach this repository's `AGENTS.md` through the relevant ChatGPT Project/custom instructions or explicitly ask the assistant to load the playbook. The assistant must never claim global activation unless the current chat actually has the instructions available.

## Start here

1. Read [`AGENTS.md`](AGENTS.md).
2. If maintaining this HQ repository, bind [`PROJECT_PROFILE.md`](PROJECT_PROFILE.md); otherwise select exactly one consumer-project profile from the user's explicit context.
3. Read the selected profile and its declared canonical board, repository and environment rules.
4. Inspect live GitHub state before acting; never rely on stale chat summaries as current evidence.
5. Select only the tools and skills relevant to the task.

## Using HQ in ChatGPT

See [`CHATGPT-INSTRUCTIONS.md`](CHATGPT-INSTRUCTIONS.md) for the compact instructions to place in ChatGPT Project Instructions or Custom Instructions. Loading this repository does not automatically change account settings or activate HQ in every chat.

## HQ repository governance

When maintaining this repository itself, use [`PROJECT_PROFILE.md`](PROJECT_PROFILE.md) and its [canonical operations board](https://github.com/zarkmakerburg/project-hq/issues/1). Consumer projects must not use this board.

## Structure

- `CORE/` — reusable operating model and command protocol.
- `MODES/` — HQ ON/OFF behavior contracts.
- `TOOLS/` — tool routing and skill selection.
- `TEMPLATES/` — project-neutral task, handoff and evidence templates.
- `PROJECTS/` — project profile template and integration guide.
- `PROJECT_PROFILE.md` — profile and governance binding for this HQ repository itself.

## Isolation rule

The core is shared; every project has its own profile, repository, board, evidence, credentials, host registry, permissions and release state. Never copy project-specific identifiers, secrets, hosts, approvals or operational state between projects. A profile binds context; it does not grant permissions.
