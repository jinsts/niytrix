# Platform architecture

## Status

This is a **conceptual architecture**, not permission to start implementation.
Technology selections remain proposals until platform behaviours, acceptance
criteria, data requirements, and broker constraints are verified.

## Architectural intent

Build a lean shared platform around isolated strategies. Share contracts and
control capabilities only where doing so does not blend mandates or evidence.

```text
Market data
    ↓
Strategy-specific scheduler
    ↓
Versioned deterministic rule package
    ↓
Risk and availability gate
    ↓
Replaceable broker adapter
    ↓
Broker orders, fills, and positions
    ↓
Journal, reconciliation, and evidence outputs
```

## Capability boundaries

| Capability | Responsibility |
| --- | --- |
| Market data | Acquire inputs and reject stale, incomplete, or invalid data |
| Schedulers | Trigger swing and intraday decisions on separate clocks |
| Rule packages | Produce explainable decisions from versioned inputs and configuration |
| Risk gate | Enforce strategy, capital, exposure, availability, freshness, and kill state |
| Broker adapter | Provide idempotent execution behind a replaceable boundary |
| Journal | Record signals, vetoes, orders, fills, costs, outcomes, and lineage |
| Reconciliation | Compare local intent and state with authoritative broker books |
| Evidence outputs | Produce immutable, reproducible research and operating reports |

## Isolation rules

Swing V1 and Intraday V1 may share event contracts, risk primitives, execution
interfaces, reconciliation logic, and journal conventions. They must not share
signal logic, schedules, capital accounts, strategy ledgers, limits, benchmarks,
or performance assessments.

## Current proposed shape

The consolidated plan proposes a single small cloud boundary, OpenAlgo behind a
narrow adapter, a deterministic strategy service, SQLite for low-concurrency
operational state, and immutable files with Parquet/DuckDB for research. These are
starting hypotheses, not finalized build choices.

PostgreSQL or a more distributed design is justified only by observed needs such
as multiple writers or users, recurring lock contention, audit/query pain, or
recovery requirements that the simpler design cannot meet.

## Required qualities

- Determinism and replayability.
- Idempotent order submission and explicit state transitions.
- Traceability from input data and configuration to every decision.
- Safe default behaviour on stale data, dependency failure, and mismatch.
- Broker-side protection that survives strategy-service failure.
- Recoverability through tested backups, restart, and reconciliation.
- Replaceable external boundaries rather than strategy code coupled to a broker.

## Architecture questions to resolve

1. What exact decisions and events cross each boundary?
2. Which state is authoritative for every lifecycle transition?
3. What does safe degradation mean for each dependency failure?
4. Which broker behaviours can be demonstrated in sandbox or minimum-size tests?
5. Which evidence must be immutable, and for how long?
6. What measured condition would justify each deferred technology?
