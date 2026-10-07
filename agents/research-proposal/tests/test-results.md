# Acceptance test results

**Review date:** 2026-09-20  
**Method:** scenario walkthrough against `agents/research-proposal/AGENTS.md` and `agents/research-proposal/templates/quality-review-checklist.md`. No factual literature or invented numerical results were used.

## First-pass findings and corrections

| Finding | Risk | Correction now in `AGENTS.md` |
| --- | --- | --- |
| Broad but workable ideas could trigger too many intake questions. | Unnecessary interruption. | “One decisive question” and “focused default scope” rules. |
| A method proposal could silently change the intended study. | Loss of user intent. | Scope-preservation and material-reframing explanation rule. |
| Suggested sample sizes might read as facts. | Unsupported specificity. | Use range/rationale or `[confirm access]`, never an invented exact value. |

## Retest results

| Test | Questions only when necessary | Question ↔ method | Method fit | No fabricated information | Coherent proposal sections | Original intent preserved | Result |
| --- | --- | --- | --- | --- | --- | --- | --- |
| T1 Quantitative intervention | Pass — 0 questions | Pass — pre/post outcome comparison | Pass — quasi-experimental with causal limits | Pass — no result or source asserted | Pass — intervention, outcome, comparison, and analysis align | Pass — workshop-writing focus retained | Pass |
| T2 Survey | Pass — 0 questions | Pass — variables and association analysis match | Pass — cross-sectional, non-causal | Pass — constructs are proposals, not facts | Pass — population, measures, and analysis align | Pass — remote-work satisfaction retained | Pass |
| T3 Qualitative | Pass — 0 questions | Pass — interviews/thematic analysis answer process question | Pass — purposive qualitative design | Pass — no barriers or findings invented | Pass — participants, protocol, and analysis align | Pass — rural older-adult focus retained | Pass |
| T4 Mixed methods | Pass — 1 design-critical question maximum | Pass — distinct engagement/experience components | Pass — explicit integration point | Pass — no coding-club effect claimed | Pass — both components and integration align | Pass — both parts of idea retained | Pass |
| T5 Ambiguous education | Pass — 1 scope question maximum | Pass — scope precedes survey/interview choice | Pass — focused default with alternatives | Pass — perception not treated as prevalence | Pass — problem, scope, method choices align | Pass — AI-tool concern retained | Pass |

## Conclusion

All five retests meet the acceptance criteria: necessary questions only; matched methods; appropriate designs; no fabricated information; coherent proposal sections; and no unannounced distortion of the input idea. The corrections above are incorporated in the current `AGENTS.md`.
