# AGENTS.md

## Mission

Turn repeated corrections into reusable engineering assets. Optimize for durable quality, not one-off success.

## Four Layers

1. Cognitive core: define goals, boundaries, and done criteria here.
2. Path-scoped rules: load only the constraints relevant to the files being touched.
3. Role separation: keep planning, review, verification, and memory capture conceptually distinct.
4. Memory loop: record corrections, extract observations, and promote stable rules.

## Operating Order

1. Read this file first, then read the nearest child `AGENTS.md` for the active path.
2. Restate the task in terms of success criteria, boundaries, and likely failure modes.
3. Load only the rules relevant to the touched paths. See `rules/path-risk-matrix.md`.
4. Follow the role order below:
   - planning -> `agents/planner.md`
   - review -> `agents/reviewer.md`
   - verification -> `agents/verifier.md`
   - memory capture -> `agents/collector.md`
5. If the runtime or the user does not allow delegation, emulate the same order in a single thread.
6. After a meaningful correction, append factual entries to `memory/corrections.jsonl` or `memory/observations.jsonl`.
7. Promote repeated lessons into `memory/learned-rules.md` and log the upgrade in `memory/evolution-log.md`.

## Definition Of Done

- The request is satisfied.
- The strongest practical verification has been run, or the gap is stated explicitly.
- Important risks or residual uncertainty are called out.
- Non-obvious corrections are captured in memory.
- Rule changes are backed by evidence, not vibes.

## Guardrails

- Do not treat a single anecdote as a global rule unless the cost of repeating it is high.
- Do not rewrite memory logs to hide failed attempts; append follow-up entries instead.
- Do not add path rules without naming the path, the risk, and the trigger condition.
- Do not delegate or parallelize unless the runtime and the user explicitly allow it.
- Prefer the smallest change that removes the failure mode.
- When a rule conflicts with reality, update the rule and log why it changed.

## Rule Loading

- Root `AGENTS.md` is the workspace constitution.
- The nearest nested `AGENTS.md` defines local boundaries for a directory.
- Files under `rules/` store reusable policies and trigger notes.
- Path-local rules beat global preferences when they conflict.

## Upgrade Ladder

1. Correction: record a concrete fix.
2. Observation: extract the recurring pattern.
3. Learned rule: codify a reusable policy.
4. Evolution log: record when and why the system itself changed.

## Minimum Routine After Each Non-Trivial Task

1. Ask what failed, almost failed, or required human steering.
2. Write one correction entry if a concrete mistake was fixed.
3. Write one observation entry if a pattern appeared.
4. Promote to a rule only if the lesson is likely to recur.

## File Map

- `rules/README.md`
- `rules/path-risk-matrix.md`
- `rules/trigger-map.md`
- `skills/retro-capture.md`
- `agents/*.md`
- `memory/*`

## Change Protocol

When you add or update a rule:

1. Update the relevant file under `rules/` or `memory/learned-rules.md`.
2. Add a dated note to `memory/evolution-log.md`.
3. Reference the supporting evidence from corrections or observations.

## Implementation Note

This scaffold is convention-first. It is useful immediately through `AGENTS.md`, and it is ready to be wired into host-specific hooks or memory services later without changing the high-level model.
