# Claims Cite

A reproducible benchmark + verification toolkit that scores any claims handling AI on citation faithfulness under adversarial document perturbations, designed to be the artifact a carrier procurement team can run before signing Solva.

## Why This Exists

Solva's wedge is "every recommendation is source cited from the claim/policy documents" - i.e., they're betting that citations are the trust primitive insurers buy on. But the public artifact that proves the citations are load bearing under adversarial conditions does not exist. Concretely: when a Solva agent says "this claim violates Section 7.

## What It Builds

- Replays synthetic `solva` and `wedge` cases against the project's evidence rules.
- Scores `solva_coverage`, `wedge_risk`, and `every_precision` so regressions are visible in CSV and JSON.
- Plants `solva drift` and `wedge gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `claims-cite` without hosted services.

## Local Run

```bash
uv sync
uv run claims-cite all
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

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
