# Niytrix

Niytrix is the planning repository for an evidence-gated trading platform. The
current phase is **definition and discovery**: the repository documents what the
platform should do, how risk is governed, and which questions must be answered
before implementation begins.

No application or infrastructure has been initialized yet.

## Start here

1. Read the [documentation index](docs/README.md).
2. Open the [Unified Trading Strategy & Wealth Operating Plan](docs/unified-trading-strategy.html)
   for the complete, designed reading experience.
3. Use the focused Markdown documents when discussing or changing one decision
   area at a time.

## Current direction

- **Swing V1** is the primary strategy candidate.
- The **15-minute NSE intraday strategy** is an isolated research laboratory.
- Shared platform capabilities are allowed, but strategy schedules, capital,
  ledgers, limits, and performance evidence remain separate.
- Evidence and explicit promotion gates release capital; forecasts and confidence
  do not.

## Repository map

```text
.
├── AGENTS.md
├── README.md
└── docs/
    ├── README.md
    ├── platform-charter.md
    ├── strategy-portfolio.md
    ├── risk-and-governance.md
    ├── platform-architecture.md
    ├── evidence-and-operations.md
    ├── roadmap-and-open-decisions.md
    └── unified-trading-strategy.html
```

## Status

Documentation foundation only. Strategy rules, acceptance criteria, data policy,
broker behaviour, compliance assumptions, and architecture boundaries must be
resolved before technical implementation starts.
