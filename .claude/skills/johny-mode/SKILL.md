---
name: johny-mode
description: Load and apply John's personal engineering workflow skills before completing a task. Use when the user starts a request with /johny-mode or $johny-mode.
---

Read the linked skills before starting the requested task, then apply each one when its condition is relevant:

- [check-types-at-the-perimeter](../check-types-at-the-perimeter/SKILL.md): Consult when writing or reviewing TypeScript or Python code that handles APIs, external integrations, databases, or client-server validation.
- [tdd](../tdd/SKILL.md): Consult when implementing a change with testable success criteria so separate subagents can own the tests and implementation.
- [comment-sicko](../comment-sicko/SKILL.md): Consult whenever writing or refactoring code so comments stay concise and the code remains self-documenting and easy to scan.
- [make-it-fast](../make-it-fast/SKILL.md): Consult when investigating slowness, instrumenting latency, or making a performance improvement. Establish a baseline and verify the result against the same workload.
- [small-pieces](../small-pieces/SKILL.md): Consult when planning or delivering a change that may need multiple reviewable PRs or could exceed 500-750 lines of code.
- [uv-lock-editing](../uv-lock-editing/SKILL.md): Consult whenever editing Python dependencies, `pyproject.toml`, or `uv.lock`, or running `uv` commands that may update a lockfile.
- [dead-code-society](../dead-code-society/SKILL.md): Consult during implementation, refactoring, or review when obsolete code, low-value tests or configuration, and unnecessary comments can be removed safely.
- [yagni](../yagni/SKILL.md): Consult before implementing or while reviewing code to challenge speculative edge cases, abstractions, and complexity that are unlikely to provide current value.
- [stack-em-up](../stack-em-up/SKILL.md): Consult when evaluating or responding to code review feedback that may be valid but outside the scope of the current PR.
- [babysit](../babysit/SKILL.md): Consult when monitoring a PR through CI and all forms of review feedback, using YAGNI and stacked follow-ups to decide what belongs in the current change.
- [tell-the-story](../tell-the-story/SKILL.md): Consult after significant functionality or refactoring work to check whether the code clearly communicates its behavior and deserves a stacked cleanup PR.

Treat the text following `/johny-mode` or `$johny-mode` as the task and continue with it after loading the relevant instructions.

Adapted from the `woody-mode` skill by Chris Wood.
