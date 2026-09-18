# Metrics

The lab prioritizes measurements that can distinguish resource pressure from ordinary workload activity.

## System-level

- Physical memory and available memory.
- Commit and working-set indicators where observable.
- Memory pressure indicators.
- Storage read/write throughput.
- Storage I/O operation counts.
- Storage queueing/latency where observable.
- CPU utilization.
- Process activity.
- Foreground/background state where observable.
- Experiment elapsed time.

## Workload-level

- Startup time.
- Load or phase transition time.
- Operation latency.
- Application-visible stalls for controlled workloads.
- Completion time.
- Error/interruption state.

## Distribution metrics

Prefer P50, P95, P99, min/max where useful, and run-to-run variance.

## Observer overhead

Record CPU overhead, memory overhead, event/sampling volume, storage written by the observer, and measurable impact on workload latency.

## Resource-tier dimensions

Where hardware permits, characterize each device by capacity, latency, throughput, random I/O behavior, queue behavior, interface characteristics, and reliability/availability conditions relevant to the test.

Do not assume one synthetic benchmark represents an application's real workload.
