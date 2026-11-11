# Strategy portfolio

## Portfolio decision

The platform supports two separate strategy mandates, not a blended strategy.
Signals, statistics, schedules, capital accounts, limits, ledgers, and promotion
decisions must remain separate. Either strategy must be stoppable without changing
the other.

## Swing V1 — primary candidate

| Dimension | Current direction |
| --- | --- |
| Purpose | Primary candidate for long-run systematic trading |
| Instrument | NSE cash equity, delivery-oriented |
| Cadence | End-of-day scan with a controlled weekly workflow until automation is proven |
| Current stage | Research and production-equivalent shadow operation |
| Earliest live ceiling | ₹60,000, two positions, and no more than ₹250 risk per trade |
| Earliest promotion evidence | Robust backtest plus 12 shadow weeks |
| Priority | Receives research and engineering capacity first |

### Rule-freeze requirement

The exact universe, setup, entry, initial stop, exit, gap handling, corporate-action
handling, benchmark, cost model, and acceptance thresholds are not yet frozen.
Another implementer must be able to reproduce every decision without guessing
before this mandate becomes an implementation specification.

## Intraday V1 — bounded laboratory

| Dimension | Current direction |
| --- | --- |
| Purpose | Test whether a five-condition, 15-minute confluence survives realistic costs |
| Instrument | Liquid NSE cash equity using an intraday product |
| Cadence | Closed candles during the defined market window, followed by controlled square-off |
| Current stage | Data capture, replay, and shadow evaluation only |
| Earliest live ceiling | ₹25,000–₹30,000, one position, and no more than ₹300 risk per trade |
| Earliest promotion evidence | 300 historical events, 100 replay trades, and 30–50 shadow sessions |
| Priority | Must not delay Swing V1 or interfere with paid work |

### Rule-freeze requirement

The five confluence conditions, bar semantics, symbol eligibility, order semantics,
stop and target rules, time exits, stale-data behaviour, and cost assumptions must
be made exact before implementation.

## Portfolio invariants

- Do not transfer protected wealth into either strategy to recover losses.
- Do not compare or combine performance unless costs and capital bases are
  consistently defined.
- Cross-strategy exposure and correlated risk require an explicit portfolio gate.
- Promotion of one strategy does not validate or fund the other.
- Intraday experimentation may not consume the capacity required to validate the
  primary swing mandate.

## Questions for the next review

1. What outcome is Swing V1 explicitly designed to exploit?
2. What are the exact, testable rules for both mandates?
3. Which benchmark and point-in-time universe make each mandate falsifiable?
4. Which constraints are permanent principles, and which are temporary pilot
   limits?
