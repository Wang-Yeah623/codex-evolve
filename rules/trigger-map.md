# Trigger Map

This file defines the checkpoints that should eventually be automated with hooks, and that should already be followed manually today.

## Prompt Start

- Read root `AGENTS.md`.
- Read the nearest path-local `AGENTS.md`.
- Load the relevant path rules.
- Skim `memory/learned-rules.md` before making broad changes.

## Before Edit

- Identify the active risk path.
- Decide how the change will be verified.
- Note the most likely regression or failure mode.

## After Failure Or Course Correction

- Append a concrete entry to `memory/corrections.jsonl`.
- Capture what changed, why it failed, and how it was verified.

## After A Repeated Pattern

- Append an entry to `memory/observations.jsonl`.
- Decide whether the pattern is strong enough to promote into a learned rule.

## Task Complete

- Run the checklist in `skills/retro-capture.md`.
- If rules changed, record the reason in `memory/evolution-log.md`.

## Automation Note

If the host runtime supports hooks, these checkpoints are the first surfaces to automate.
