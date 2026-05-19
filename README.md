# Homeprint

A one screen "submit your address + last 12 months of PG&E bills, get a Manual J sized heat pump, a panel load verdict, and a binding price" tool - bolts onto the Remix/Django stack and shaves a truck roll out of every five.

## Why This Exists

Electric Air's Push Button - Get Heat Pump post promises a "Free Online Quote" that runs EnergyPlus + Manual J + NEC + Manual D behind the scenes. But the public site funnel collects "address, heating type, and thermostat count" and quotes a price - it cannot answer the real homeowner question: "with my house, my PG&E rate, my panel, my ductwork, what does my actual electric bill look like in February, and will my 100A panel pop?

## What It Builds

- Replays synthetic `electric` and `button` cases against the project's evidence rules.
- Scores `electric_coverage`, `button_risk`, and `promises_precision` so regressions are visible in CSV and JSON.
- Plants `electric drift` and `button gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `homeprint` without hosted services.

## Local Run

```bash
uv sync
uv run homeprint all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://www.electricair.io/posts/stronger-together-electric-air-and-helios-climate
- https://www.electricair.io/posts/push-button---get-heat-pump
- https://www.electricair.io/discover
- https://jobs.ashbyhq.com/electricair/0a246bea-18a2-4564-910c-2f39573a747e
- https://www.ycombinator.com/companies/electric-air-2/jobs/0zeoBWa-senior-full-stack-engineer
- https://www.ycombinator.com/launches/IBA-electric-air-tesla-for-heat-pumps
- https://www.electricair.io/faq
- https://linkedin.com/in/christophermui/
- https://www.crunchbase.com/person/chris-mui-60b5

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
