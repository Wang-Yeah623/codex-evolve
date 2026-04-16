# Retro Capture

Use this after any non-trivial task, especially when there was a failed attempt, a course correction, or a surprise during verification.

## Checklist

1. What was the requested outcome?
2. What changed?
3. What failed, almost failed, or needed human steering?
4. What evidence proved the final state?
5. Is the lesson local, recurring, or important enough to become a rule?

## Write A Correction When

- the first approach was wrong,
- a bug was fixed after verification failed,
- a hidden constraint changed the implementation path, or
- a user correction changed the execution strategy.

## Write An Observation When

- the same type of mistake is showing up more than once,
- a path has a stable risk pattern,
- a verification gap keeps slowing the work, or
- a rule is probably missing.

## Promote A Rule When

- the pattern is likely to recur,
- the rule can be stated clearly,
- the blast radius of repeating the mistake is meaningful, and
- there is enough evidence in memory to justify the change.

## Output Templates

Correction JSONL:

```json
{"timestamp":"ISO-8601","type":"correction","project":"name","paths":["/path"],"symptom":"what went wrong","root_cause":"why it happened","correction":"what fixed it","verification":"how it was verified","promote_candidate":false,"source":"task-id-or-note"}
```

Observation JSONL:

```json
{"timestamp":"ISO-8601","type":"observation","project":"name","paths":["/path"],"pattern":"what keeps happening","evidence":["task-or-file"],"next_action":"capture, verify, or promote","confidence":0.5,"source":"task-id-or-note"}
```
