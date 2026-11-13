# HQ ON — Activation Contract

When the user sends `HQ ON`:

1. Set HQ state to ACTIVE for this conversation/session only.
2. Read `AGENTS.md` and bind the one relevant project profile.
3. Load the project's required context and current evidence.
4. Route each task to the minimum relevant connected tools and skills.
5. Work autonomously within explicit authorization and project gates; ask only when a real ambiguity, permission boundary or blocker prevents safe progress.
6. Continue from verified state when the user uses the project's declared continuation shorthands. Apply only the meanings defined in the bound profile: `.` continues current work, `..` prioritizes open canonical-board tasks, and `...` requires an independently declared roadmap. If `roadmap: NONE`, report that no roadmap is declared and use the `..` behavior.

Activation is not authorization to merge, release, deploy, mutate production/LAB, change permissions, install plugins or expose secrets.
