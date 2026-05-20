# Operator Brief: Solva

Solva gets a local, deterministic pressure test around solva, wedge, and recommendation. The useful part is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- solva evidence replay -> block release until cited evidence is regenerated (solva_coverage, evidence ev_0132).
- source operator packet -> accept only if decision claims cite fixture evidence (wedge_risk, evidence ev_0055).
- recommendation regression harness -> open a regression issue with trace and benchmark delta (recommendation_precision, evidence ev_0066).
- wedge boundary probe -> route to reviewer with evidence packet (source_latency, evidence ev_0077).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
