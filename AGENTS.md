# Repository guidance

## Purpose

This repository is being shaped into an evidence-gated trading platform. Until
the platform definition is approved, prefer documentation and decision records
over application, dependency, deployment, or infrastructure files.

## Working rules

- Read `README.md` and `docs/README.md` before making changes.
- Treat `docs/unified-trading-strategy.html` as the consolidated reading edition.
- Keep focused Markdown documents aligned with the consolidated plan.
- Do not silently convert an open question or placeholder into a settled rule.
- Label assumptions, placeholders, decisions, and evidence requirements clearly.
- Preserve the separation between Swing V1 and Intraday V1 capital, ledgers,
  schedules, limits, and performance assessment.
- Never describe a backtest, forecast, or attractive chart as proof of an edge.
- Revalidate financial, tax, legal, broker, and platform claims before relying on
  them; do not present repository content as financial advice.
- Use descriptive, lowercase, hyphenated names for new documentation files.
- Link new documents from `docs/README.md`.

## Change discipline

- Make the smallest change that closes a documented decision or improves clarity.
- Record material decisions and their rationale in the relevant focused document.
- Keep implementation details out of the repository until the corresponding
  platform behaviour and acceptance criteria have been agreed.
