# Learned Rules

## Active Rules

### R-001 Root Constitution

The workspace root `AGENTS.md` is the default operating contract for future sessions.

### R-002 Append-Only Memory

`corrections.jsonl` and `observations.jsonl` must remain append-only so the memory trail stays trustworthy.

### R-003 Path Before Policy

When a directory develops stable local risk, capture it in the nearest `AGENTS.md` or `rules/` before adding more global instructions.

### R-004 Evidence Before Promotion

Promote a rule only when there is enough correction or observation evidence to justify reuse.

### R-005 Delegation Is Optional

Role separation is always required conceptually, but actual subagent delegation is optional and must respect runtime or user constraints.

## Pending Promotions

- None yet. Promote only after real task evidence accumulates.

## Update Protocol

When editing this file:

1. Reference the supporting corrections or observations.
2. Add a dated note to `evolution-log.md`.
3. Remove or revise rules that no longer match reality.
