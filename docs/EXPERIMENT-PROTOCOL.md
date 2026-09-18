# Experiment Protocol

## Goal

Turn a performance hypothesis into a reproducible measurement rather than an implementation claim.

## Required experiment record

1. Hypothesis.
2. Workload.
3. Hardware and Windows version.
4. Storage devices and relevant filesystem details.
5. Background activity.
6. Instrumentation configuration.
7. Baseline condition.
8. Test condition.
9. Repetitions.
10. Primary metrics.
11. Observer overhead.
12. Results.
13. Interpretation.
14. Alternative explanations.
15. Known limitations.

## Baseline rule

Whenever possible, collect a baseline without the lab observer running, then repeat the same workload with observation enabled.

Do not interpret a performance difference as a workload effect until observer overhead has been measured.

## Cold and warm states

Explicitly distinguish cold-start and warm-cache conditions.

## Tail behavior

Report distributions, not only averages. Use P50, P95 and P99 where appropriate.

## Causality discipline

Correlation between two signals is not by itself proof of cause.

For example, a hard page fault is evidence of a faulting event, not automatically proof of page-file thrashing.

## Safety

Initial tooling is observation-first and should fail closed. It should not modify application state or system resource placement as part of measurement.
