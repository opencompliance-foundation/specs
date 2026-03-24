# Mapping Methodology

## Current rule

OpenCompliance does not map raw framework clauses directly into Lean theorems.

The current public corridor works in three layers:

1. Source frameworks such as ISO 27001, SOC 2, IRAP, and GDPR.
2. Narrow OpenCompliance controls that isolate a single atomic or near-atomic obligation.
3. Lean 4 predicates for the decidable slice of those OpenCompliance controls.

That is why the current public `control-boundaries.json` uses family-proxy mappings. The proofs attach to the OpenCompliance control layer, not to raw standards text.

## Why a direct clause-to-theorem model is wrong

Most real controls are mixed objects.

- Some parts are decidable from system state.
- Some parts require signed attestation.
- Some parts are irreducibly human judgment.

If the project tries to map an entire ISO 27001 clause or SOC 2 criterion to one theorem, it collapses those distinct epistemic categories and becomes misleading.

## Current state

The public corridor is still draft and family-proxy only.

- OpenCompliance controls are machine-readable and route-aware.
- Lean proofs exist for a narrow decidable subset.
- OSCAL-shaped mapping collections exist for the same synthetic corridor.
- Exact reviewed source anchors are not yet published for the public corridor.

## State-of-the-art target

State of the art is a reviewed multi-layer mapping system:

1. Anchor every mapping to framework-native source identifiers.
   Examples: ISO clauses, Annex A controls, SOC 2 criteria, SOC 2 points of focus, IRAP/ISM controls, GDPR articles or other framework-native anchors.
2. Decompose each source requirement into atomic obligations before proof assignment.
3. Route each atomic obligation explicitly as `decidable`, `attestation`, `judgment`, or `mixed`.
4. Persist per-edge mapping metadata.
   Minimum fields: relation, mapping method, review status, and confidence.
5. Keep proof boundaries explicit.
   A Lean theorem proves only the decidable atom, not the whole source requirement by implication.
6. Publish coverage and non-coverage.
   Consumers must be able to see which source anchors are mapped, which are only partially covered, and which remain unresolved.
7. Export the result in OSCAL-native mapping artifacts at the right granularity.

## Practical interpretation for ISO 27001 and SOC 2

For ISO 27001 and SOC 2, the right pipeline is usually:

1. Start from the authoritative source requirement.
2. Decompose it into smaller obligations.
3. Bind each obligation to evidence types and route.
4. Formalize only the narrow decidable obligations in Lean 4.
5. Keep attestations and human judgments outside the proof kernel, but attached to the same obligation graph.

## Immediate next step

The next credible step is not a fake "full mapping".

It is to upgrade the public corridor from family proxies toward reviewed source anchors with:

- explicit mapping maturity,
- exact-anchor plans per control,
- machine-checked mapping metadata,
- and eventually a first reviewed pilot set of clause- or criterion-grade mappings for a small number of controls.
