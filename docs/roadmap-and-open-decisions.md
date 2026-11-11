# Roadmap and open decisions

## Current phase: definition and discovery

No technical implementation should begin until the platform purpose, strategy
contracts, acceptance criteria, authority, and key external assumptions are clear
enough that another implementer does not have to guess.

## Ordered roadmap

1. **Freeze the decision pack.** Resolve product purpose, exact strategy rules,
   evidence thresholds, data policy, risk matrix, and authority model.
2. **Validate external constraints.** Verify broker behaviour, data licensing,
   protection semantics, regulatory obligations, and accounting treatment.
3. **Specify the shared core.** Define contracts for events, risk, execution,
   journaling, reconciliation, and failure recovery.
4. **Build only the minimum foundation.** Implement once failure drills and
   acceptance tests can be stated in advance.
5. **Run historical and replay research.** Produce immutable reports against
   predeclared thresholds.
6. **Run production-equivalent shadow operation.** Use the intended schedules,
   inputs, rules, and alerts without capital for the required window.
7. **Consider Swing V1 micro-live.** Release no more than the approved stage limit
   only if every required gate passes.
8. **Judge each mandate independently.** Scale, hold, redesign, or terminate based
   on after-cost evidence, risk, adherence, life fit, and operational stability.

## Decisions required before coding

### Platform purpose

- [ ] Define the users and the exact decision the platform helps each user make.
- [ ] Define the platform's non-goals and permanent safety invariants.
- [ ] Define success and termination criteria for the discovery phase.

### Strategy and data

- [ ] Freeze exact Swing V1 rules and its benchmark.
- [ ] Freeze all Intraday V1 confluence and lifecycle rules.
- [ ] Select and license suitable point-in-time historical data.
- [ ] Define corporate-action, survivorship, timestamp, and missing-data policies.
- [ ] Predeclare statistical promotion and termination thresholds.

### Broker and platform

- [ ] Verify current broker API, static-IP, authentication, and session behaviour.
- [ ] Demonstrate broker-visible protective stops in controlled tests.
- [ ] Verify execution-boundary tags, order semantics, limits, and history depth.
- [ ] Define idempotency, partial-fill, rejection, restart, and recovery policies.
- [ ] Define the minimum journal and reconciliation contracts.

### Risk, finance, and governance

- [ ] Replace all percentage placeholders with evidence-based limits.
- [ ] Define swing pause and drawdown limits for every stage.
- [ ] Define cross-strategy exposure and withdrawal policy.
- [ ] Confirm the wealth firewall and allocation review cadence.
- [ ] Document who can approve, pause, resume, kill, and change configuration.

### Legal and tax

- [ ] Revalidate applicable retail-algorithm rules before live deployment.
- [ ] Obtain qualified accounting guidance for delivery and intraday ledgers.
- [ ] Separate long-term, swing, intraday, and unrelated business accounting.
- [ ] Establish a recurring compliance and tax review.

## Immediate next conversation

Work through the platform charter before architecture or technology. Start with:

> Who is the platform for, what recurring decision does it make safer or better,
> and what must it never be allowed to do?
