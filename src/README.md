# Experimental Tooling

The lab tooling will be added here in small, independently testable components.

The first implementation target is a **read-only Windows telemetry collector** that can record resource behavior during controlled workloads.

Design goals:

- Read-only.
- Low overhead.
- Timestamped measurements.
- Explicit experiment/session boundaries.
- Machine-readable output.
- Versioned collector configuration.
- No undocumented system manipulation.
