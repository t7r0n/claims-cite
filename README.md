# Claims Cite

A reproducible benchmark + verification toolkit that scores any claims handling AI on citation faithfulness under adversarial document perturbations, designed to be the artifact a carrier procurement team can run before signing Claims Cite.

![Claims Cite working dashboard](outputs/project_working.svg)

## Why it exists

Claims Cite's wedge is "every recommendation is source cited from the claim/policy documents" — i.e., they're betting that citations are the trust primitive insurers buy on. But the public artifact that proves the citations are load bearing under adversarial conditions does not exist. Concretely: when a Claims Cite agent says "this claim violates Section 7.

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/claims_cite/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Claims Cite evidence map](outputs/evidence_map.svg)

## Signals it measures

- `Claims Cite coverage`
- `wedge risk`
- `recommendation precision`
- `source latency`

## Failure modes it plants

- Claims Cite drift
- wedge gap
- recommendation misroute
- source blindspot

## Run it locally

```bash
uv sync
uv run claims-cite all
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

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
