# Safety Boundaries

This public lab is deliberately constrained.

## Allowed in the initial phase

- Read-only system observation.
- Process/resource telemetry.
- Controlled file reads/writes performed by explicit benchmark workloads.
- Timing and statistical analysis.
- Public benchmark assets and reproducible protocols.
- Fault-free controlled experiments.

## Explicitly out of scope for the initial prototype

- DLL injection.
- Undocumented kernel hooks.
- Page-table modification.
- Arbitrary interception of third-party application I/O.
- Forced global working-set manipulation.
- Transparent relocation of files owned by unrelated applications.
- Automatic process termination.
- Modification of protected or encrypted application state.
- Claims of universal compatibility.
- Automatic optimization based solely on an unvalidated prediction.

## Data handling

Do not publish personal data, authentication material, secrets, proprietary application data, or private benchmark datasets.

Raw traces may contain environment-specific information. Review generated artifacts before committing them to a public repository.

## Recovery principle

Experiments should leave the machine in the same logical state in which they started. Any test capable of modifying data must use disposable test data and document cleanup.
