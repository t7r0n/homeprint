# Homeprint

A one screen "submit your address + last 12 months of PG&E bills, get a Manual J sized heat pump, a panel load verdict, and a binding price" tool - bolts onto the Remix/Django stack and shaves a truck roll out of every five.

![Homeprint working dashboard](outputs/project_working.svg)

## Why it exists

Electric Air's Push Button - Get Heat Pump post promises a "Free Online Quote" that runs EnergyPlus + Manual J + NEC + Manual D behind the scenes.

Most internal demos stop at a pretty chart. This repository is built around the harder part: a repeatable path from fixture, to failure, to evidence, to the operator action a serious team would actually trust.

## What is inside

- A deterministic replay harness tuned around electric, button, and promises.
- Company-specific strategy code in `src/homeprint/strategy.py`, not just README-level customization.
- Citation-locked reports where every decision claim has to point back to a generated evidence ID.
- Two visual artifacts generated from the latest run: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, and benchmark artifacts.

![Homeprint evidence map](outputs/evidence_map.svg)

## Signals it measures

- `electric coverage`
- `button risk`
- `promises precision`
- `online latency`

## Failure modes it plants

- electric drift
- button gap
- promises misroute
- online blindspot

## Run it locally

```bash
uv sync
uv run homeprint all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
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

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
