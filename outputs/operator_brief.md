# Operator Brief: Electric Air

Electric Air gets a local, deterministic pressure test around electric, button, and promises. The useful part is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- electric evidence replay -> block release until cited evidence is regenerated (electric_coverage, evidence ev_0000).
- online operator packet -> accept only if decision claims cite fixture evidence (button_risk, evidence ev_0055).
- promises regression harness -> open a regression issue with trace and benchmark delta (promises_precision, evidence ev_0066).
- button boundary probe -> route to reviewer with evidence packet (online_latency, evidence ev_0033).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
