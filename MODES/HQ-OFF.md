# HQ OFF — Deactivation Contract

When the user sends `HQ OFF`:

1. Set HQ state to INACTIVE for this conversation/session.
2. Stop applying HQ-specific autonomous execution, task routing and continuation behavior.
3. Do not start new project operations merely because an earlier HQ task was active.
4. Ordinary assistant capabilities remain available; the user may explicitly request a standalone task.
5. Preserve all repository state and work already performed. Deactivation does not undo commits, changes, tool actions or approvals.

A new conversation must not assume HQ is active unless the user or its configured instructions activates it.
