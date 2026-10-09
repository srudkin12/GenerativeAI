---
layout: default
title: Evidence ledger
---

# Evidence ledger

A claim-preservation contract states the authorised argument at project level.

An **evidence ledger** links substantive manuscript propositions to the research objects or reasoning that license them.

A useful ledger contains one row per substantive paragraph or claim.

| Field | Question |
|---|---|
| `paragraph_id` | Where is the proposition in the manuscript? |
| `principal_proposition` | What contestable claim does the paragraph make? |
| `warrant_type` | Literature, manuscript evidence, primary evidence or analytic reasoning? |
| `supporting_object` | Which exact citation, result, table, figure, source, derivation or definition supports it? |
| `claim_class` | Observed, descriptive, inferential, causal, mechanistic, qualitative interpretive, simulation-based, or another explicit class? |
| `required_qualification` | What caveat or condition must remain adjacent? |
| `contract_status` | Authorised, prohibited, or requiring substantive reconsideration? |
| `analysis_version` | Which research version supports the paragraph? |
| `audit_status` | Pass, revise, or return to analysis? |

## Why versioning matters

A manuscript sentence can remain fluent after the result that originally supported it has changed.

Live or repeatedly refreshed analysis therefore creates a special risk: textual continuity can be mistaken for evidential continuity.

A robust workflow should:

1. give stable identifiers to central results, figures, tables and claims;
2. map manuscript-generated claims to the object that supports them;
3. re-audit the claim-preservation contract after material analytical changes;
4. mark claims as unchanged, revised, withdrawn or new;
5. re-check paragraphs whose supporting objects changed;
6. return to analysis when a validity problem cannot be repaired by presentation.

## Template

Use the downloadable [Evidence Ledger template](../../templates/evidence-ledger.md).
