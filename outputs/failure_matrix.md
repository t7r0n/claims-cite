# Failure Matrix: Claims Cite

| Scenario | Failure mode | Metric | Gate | Evidence |
| --- | --- | --- | --- | --- |
| solva evidence replay | solva_drift | solva_coverage | block release until cited evidence is regenerated | ev_0000 |
| source operator packet | source_blindspot | source_latency | accept only if decision claims cite fixture evidence | ev_0007 |
| source operator packet | source_blindspot | source_latency | accept only if decision claims cite fixture evidence | ev_0011 |
| recommendation regression harness | recommendation_misroute | recommendation_precision | open a regression issue with trace and benchmark delta | ev_0014 |
| wedge boundary probe | wedge_gap | wedge_risk | route to reviewer with evidence packet | ev_0021 |
| recommendation regression harness | recommendation_misroute | recommendation_precision | open a regression issue with trace and benchmark delta | ev_0022 |
| solva evidence replay | solva_drift | solva_coverage | block release until cited evidence is regenerated | ev_0028 |
