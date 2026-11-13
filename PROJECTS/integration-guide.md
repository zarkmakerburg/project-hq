# Integrating a Project with HQ

1. Keep the HQ core in its own repository; do not copy the core into product source unless a project needs a pinned snapshot.
2. Add a project-local `AGENTS.md` entry point that links to the HQ playbook and identifies the project profile.
3. Create a project profile from `PROJECT_PROFILE.template.yml`.
4. Declare exactly one canonical operational/evidence board, repository identity, default branch, registered environments and authorization boundaries. Set `project.roadmap: NONE` unless the owner explicitly identifies an independent roadmap; never relabel the canonical board as a roadmap.
5. Keep secrets in protected GitHub/environment settings; profile files contain identifiers and policy only.
6. Configure the ChatGPT Project/custom instructions or new conversation to load HQ `AGENTS.md` when needed. A GitHub repository alone does not automatically configure every ChatGPT chat.
7. Verify the project binding and access before the first operation. No permissions are inherited from other projects.
8. Preserve the continuation command contract: `.` continues the current task; `..` prioritizes open canonical-board tasks; `...` performs roadmap reassessment only when an independent roadmap is declared. With `roadmap: NONE`, `...` reports that no roadmap exists and falls back to `..`.
