# Evidence and operations

## Evidence chain

Passing one layer never waives another. Promotion thresholds must be declared
before inspecting the evidence used to judge them.

1. **Unit evidence** — rule fixtures, boundaries, gaps, corporate actions, and
   sizing arithmetic.
2. **Historical evidence** — walk-forward evaluation, realistic costs,
   point-in-time universes, and parameter-neighbour tests.
3. **Replay evidence** — event order, closed-candle discipline, duplicates, late
   data, and restart behaviour.
4. **Shadow evidence** — production data, schedules, decisions, and expected
   orders with no money at risk.
5. **Micro-live evidence** — bounded real fills, costs, behaviour, protection,
   and daily reconciliation.

## Promotion dimensions

A promotion decision needs all of the following:

- Positive after-cost out-of-sample evidence against a declared benchmark.
- Acceptable drawdown, duration, loss clustering, and stress behaviour.
- Robustness across regimes, time slices, symbols, and neighbouring parameters.
- Execution within the tested fill, rejection, slippage, and cost envelope.
- At least 95% rule adherence, with every exception classified.
- No unresolved critical operational defects.
- Sustainable operation within the 4–5 hour weekly target.
- Appropriate accounting, tax, and compliance review.

## Operating rhythm

| Window | Intended activity |
| --- | --- |
| Before market | Authenticate; verify mode, freshness, limits, availability, candidates, and reconciliation |
| Market hours | Run closed-candle decisions hands-off; alert only on material events |
| After market | Reconcile signals, orders, fills, positions, fees, and P&L against broker books |
| Weekly | Review taken and skipped signals, incidents, adherence, costs, and regime slices |

The availability gate blocks new live entries during work conflicts, travel,
illness, poor sleep, or other conditions that make accountable operation unsafe.
Automation removes chart watching, not responsibility.

## Failure posture

| Failure | Safe default |
| --- | --- |
| Missing session | No new trades; never chase a missed decision |
| Strategy service unavailable | Broker protection remains; alert and recover |
| Execution boundary unavailable | Pause new entries; do not retry blindly |
| Late or missing data | Skip the cycle and record the reason |
| Partial fill | Protect filled quantity and follow the frozen remainder policy |
| Position mismatch | Pause; reconcile to broker truth; require manual resume |
| Work or health conflict | Block new entries through the availability gate |

## Learning loop

Freeze the period's records, compute evidence, review labeled observations, make a
human decision, validate any accepted hypothesis under a new version, and deploy
only a passing approved configuration. Facts, hypotheses, and approvals must be
separate records; no in-session tuning is allowed.
