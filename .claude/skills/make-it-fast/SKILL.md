---
name: make-it-fast
description: Measure and improve application latency. Use when investigating slowness, adding performance metrics, or optimizing a user-facing operation.
---

Start with the user's experience. Define exactly when the wait begins and
what observable event ends it. For a UI, receiving a response and displaying
the result are separate milestones.

### Establish a baseline

- Measure before changing behavior.
- Use representative real workloads. Replay retained inputs when that makes
  comparisons repeatable without rerunning expensive or variable upstream work.
- Record the revision, environment, workload size, repetitions, and cache state.
- Distinguish live measurements, retained-input replays, and simulated delays.
  Say which parts of the real workflow a benchmark excludes.

### Explain where the time goes

- Trace the full path, including queueing, preparation, computation, storage,
  persistence, transport, and rendering where applicable.
- Measure meaningful stages and relevant work counts: queries, reads, bytes,
  retries, or repeated calculations.
- Make nesting explicit. Do not add overlapping parent and child durations,
  or add independently calculated percentiles.
- Use monotonic clocks for elapsed time. Do not subtract timestamps from
  different machines unless their clock relationship is established.

### Make the measurements useful after this task

- Extend the application's existing telemetry pipeline. Use Datadog where
  that is the application's destination.
- Prefer duration distributions with bounded stage and outcome tags.
  Keep request IDs, user data, and content out of metric dimensions.
- Distinguish successful completion, failure, cancellation, and replay.
  Avoid duplicate observations and misleading success samples.
- Add useful charts through the existing dashboard configuration.
- Keep benchmark samples separate from operational metrics.
- Verify the measurement reaches its intended endpoint. Report whether
  telemetry is implemented, deployed, and observed receiving live samples.

### Improve the measured bottleneck

- Explain the cause before changing it. Connect the proposed change to
  measured time or unnecessary work.
- Prefer eliminating repeated work and avoidable waits before adding
  concurrency or a new abstraction.
- Preserve correctness, authorization, durability, and integrity checks.
  For caching, define the lifetime and invalidation rules explicitly.
- Make one attributable change at a time when practical.

### Prove the result

- Repeat the same workload under comparable conditions.
- Verify output correctness as well as speed. Use separate tests for
  meaningful behavioral guarantees.
- Report absolute before/after times, relative improvement, and changes
  in work counts. Describe variability and avoid claiming production
  percentiles from a handful of local runs.
- Leave a repeatable benchmark when it will support future comparisons.
- End with what improved, what remains slow or unmeasured, and what is
  actually deployed.
