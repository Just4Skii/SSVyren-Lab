# SSVyren Lab

Public experiments and reproducible tooling for the SSVyren research program.

## Purpose

SSVyren-Lab is the public research and validation repository for controlled Windows experiments around resource observability, workload behavior, heterogeneous storage, memory pressure, and safe resource coordination.

The main SSVyren product/research repository remains separate. This repository is intentionally limited to experiments, measurement tooling, controlled workloads, protocols, and publishable results.

## Current research stage

The lab supports Phase 3 empirical validation.

The first prototype is **read-only**: it observes system behavior and records measurements. It does not migrate files, manipulate working sets, inject code, intercept arbitrary application I/O, modify page tables, or attempt transparent memory tiering.

## What the lab is for

- Measure Windows resource behavior under controlled workloads.
- Correlate memory pressure, storage activity, process activity, and user-visible timing.
- Quantify observer overhead.
- Compare cold/warm behavior and different storage tiers where available.
- Produce reproducible experiment artifacts and documented results.
- Test hypotheses before any intervention mechanism is considered.

## What the lab is not

- It is not the SSVyren product.
- It is not a transparent system-wide cache.
- It is not a replacement for Windows memory management.
- It does not include unreleased SSVyren coordination logic.
- It does not require or encourage undocumented kernel interfaces, DLL injection, page-table manipulation, or forced global working-set control.

## Repository structure

`src/` contains experimental tooling.

`workloads/` contains controlled workload definitions and test assets.

`docs/` contains experiment protocols, metrics, and safety boundaries.

`results/` is reserved for reproducible experiment outputs. Large raw datasets should normally be kept out of Git history.

## Experimental principle

Every intervention hypothesis must first survive measurement.

> Observe → measure → reproduce → explain → compare → only then consider intervention.

## Status

Early experimental foundation. Results should not be treated as validated until the corresponding protocol, baseline, measurements, and limitations are documented.
