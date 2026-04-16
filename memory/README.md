# Memory

This directory closes the loop between one-off corrections and durable system upgrades.

## Files

- `corrections.jsonl`: append-only log of concrete fixes
- `observations.jsonl`: append-only log of recurring patterns
- `learned-rules.md`: promoted rules that are stable enough to reuse
- `evolution-log.md`: dated notes about how the system itself changed

## Logging Policy

- Append only. Do not rewrite history to hide failed attempts.
- Keep entries factual and specific.
- Promote rules from evidence, not intuition alone.
- When in doubt, record a correction first and promote later.

## Suggested Schemas

Correction fields:

- `timestamp`
- `type`
- `project`
- `paths`
- `symptom`
- `root_cause`
- `correction`
- `verification`
- `promote_candidate`
- `source`

Observation fields:

- `timestamp`
- `type`
- `project`
- `paths`
- `pattern`
- `evidence`
- `next_action`
- `confidence`
- `source`
