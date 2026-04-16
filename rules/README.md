# Rules

This directory stores reusable policies that are too broad for a single task but too specific to live only in the root constitution.

Each rule should answer five questions:

1. What path or scenario does it apply to?
2. What risk is it trying to reduce?
3. What trigger should cause the rule to load?
4. What action is required?
5. How should compliance be verified?

Use the nearest `AGENTS.md` for hard path boundaries. Use `rules/*.md` for reusable operating policies.

Add a new rule only when:

- the same correction has repeated,
- the blast radius is high, or
- the verification cost is meaningfully lower than the cost of another failure.
