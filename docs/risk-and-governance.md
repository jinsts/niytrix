# Risk and governance

## Wealth firewall

Trading capital is a bounded experimental allocation. Salary, emergency reserves,
insurance, family assets, long-term investments, and unrelated business capital
remain outside the trading loss-recovery path.

Deposits do not count as evidence. Capital can move to a higher stage only after
the strategy independently passes its predeclared evidence and operating gates.

## Proposed capital ladder

| Stage | Capital ceiling | Starting constraint | Promotion intent |
| --- | ---: | --- | --- |
| Research and shadow | ₹0 | No live risk | Establish statistical and operational evidence |
| Swing micro | ₹60,000 | 2 positions; ≤₹250 risk per trade | At least 20 compliant trades and 8 weeks |
| Controlled swing | ₹1,20,000 | 4 positions; ≤₹400 risk per trade | 30 additional trades and stable execution |
| Full swing pilot | ₹2,40,000 | 6 positions; ₹750–₹900 risk per trade | Approximately 100 trades or 6 months plus all gates |
| Intraday micro | ≤₹30,000 | 1 position; ≤₹300 risk per trade | Unlocked only by the intraday evidence pack |

These are planning ceilings, not promises or final risk settings. The lower of the
stage's rupee cap, configured percentage cap, liquidity constraint, exposure cap,
and broker constraint determines allowed quantity.

## Authority model

### The system may

- Evaluate frozen rules and risk gates.
- Create eligible orders through an approved broker boundary.
- Reject entries, pause new entries, reconcile records, and alert the operator.
- Preserve a complete record of signals, vetoes, orders, fills, costs, and state.

### A human may

- Approve or reject a proposed change.
- Reduce quantity, tighten risk, pause, kill, or exit during an emergency.
- Resume only after the documented recovery conditions are met.

### A human may not

- Increase generated quantity, widen a stop, average down, inject an ungenerated
  trade, erase a skip, or rewrite historical evidence.

### AI may not

Generate live authority, change quantity, widen stops, approve its own proposal,
or deploy a configuration. Its role is limited to labeled summaries and hypotheses
that a human can independently review.

## Breach and recovery

An unexplained order, fill, or position mismatch pauses new entries. The broker is
the position source of truth. Following a material risk breach, diagnose the root
cause, test the correction, complete four new shadow weeks, and restart at micro
risk rather than the previous size.

## Unresolved controls

- Swing daily, weekly, and drawdown pause limits by stage.
- Evidence-derived replacements for the intraday percentage placeholders.
- Cross-strategy and correlated exposure limits.
- Withdrawal eligibility and treatment during drawdown.
- Tax, accounting, and compliance treatment confirmed by qualified professionals.
