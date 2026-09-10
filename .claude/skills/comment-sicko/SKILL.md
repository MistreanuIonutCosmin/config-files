---
name: comment-sicko
description: Favor self-documenting code and scannable function structure over long or obtuse comments. Use when writing or refactoring code, especially comments, names, and long functions.
---

Don't write long or obtuse comments. Make the code speak for itself. Reading it should feel like skimming a presentation or a table of contents.

Use the call site as the readability test:

- Treat “hard to grok at a glance” as design feedback. Explain the current behavior, then use the awkward parts of that explanation to reshape the code instead of leaving clarity in prose alone.
- Name operations for their concrete domain effect, not a vague category or implementation mechanism. Prefer names like `stream_events_without_citation_handles` over names like `filter_private_text_events` or `emit_released_text`.
- Keep orchestration functions focused on sequencing. When a cohesive parser, state machine, transformation, or lifecycle starts dominating an orchestrator, move it behind a domain-owned module and import the resulting operation.
- Centralize lifecycle rules such as buffering, draining, terminal ordering, and error propagation. A caller should not need repeated helper calls or intimate knowledge of internal phases.
- Make intentional one-to-many behavior obvious in the API. If one input can produce multiple outputs, name and structure that boundary so the small iteration at the call site is unsurprising.
- After refactoring, read only the imports and top-level function. If the behavior is not clear from those names and their order, keep refining the boundary instead of explaining it with comments.

Use examples to identify the naming principle, not as vocabulary to copy into unrelated domains.
