# Agents

These files define role prompts, not tool permissions.

Use them as separate subagents only when the runtime and the user explicitly allow delegation. Otherwise emulate the same role order in a single thread.

Roles in this scaffold:

- `planner.md`: task framing, path scope, risk, and verification plan
- `reviewer.md`: regression finding and quality pressure
- `verifier.md`: evidence-driven checks
- `collector.md`: correction capture and rule promotion

Keep ownership distinct even in a single thread. Do not let memory capture replace review, and do not let review replace verification.
