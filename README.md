# Claims Cite

A reproducible benchmark + verification toolkit that scores any claims handling AI on citation faithfulness under adversarial document perturbations, designed to be the artifact a carrier procurement team can run before signing Solva.

![Claims Cite working dashboard](outputs/project_working.svg)

## Why it exists

Solva's wedge is "every recommendation is source cited from the claim/policy documents" - i.e., they're betting that citations are the trust primitive insurers buy on.

Most internal demos stop at a pretty chart. This repository is built around the harder part: a repeatable path from fixture, to failure, to evidence, to the operator action a serious team would actually trust.

## What is inside

- A deterministic replay harness tuned around solva, wedge, and recommendation.
- Company-specific strategy code in `src/claims_cite/strategy.py`, not just README-level customization.
- Citation-locked reports where every decision claim has to point back to a generated evidence ID.
- Two visual artifacts generated from the latest run: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, and benchmark artifacts.

![Claims Cite evidence map](outputs/evidence_map.svg)

## Signals it measures

- `solva coverage`
- `wedge risk`
- `recommendation precision`
- `source latency`

## Failure modes it plants

- solva drift
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

## Sources

- https://www.solvatechnology.com/about-us
- https://www.ycombinator.com/companies/solva
- https://www.ycombinator.com/launches/O7o-solva-harvey-for-insurance
- https://www.ycombinator.com/companies/solva/jobs/V9X1F0T-founding-engineer
- https://www.linkedin.com/posts/y-combinator_solva-automates-insurance-claims-with-secure-activity-7358572547300364308-9L0I
- https://www.linkedin.com/in/sorenaamini/
- https://coverager.com/company/solva/
- https://huggingface.co/BAAI/bge-reranker-v2-m3
- https://huggingface.co/microsoft/deberta-v3-base-mnli

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
