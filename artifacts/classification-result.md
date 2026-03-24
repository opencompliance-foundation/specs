# Classification Result

## Purpose

A classification result is the persisted routing surface for one verification bundle.

It makes the prove vs attest vs judgment split inspectable before anyone reads the proof bundle.

## Minimum required fields

- `classificationResultId`
- `generatedAt`
- `bundleId`
- `verifierVersion`
- `organisation`
- `profileId`
- `routeSummary`
- `items`

## Item rules

Each item should include:

- `claimId`
- `title`
- `route`
- `controlRefs`
- `expectedClaimType`
- `evidenceRequired`
- `leanBacked`
- `rationale`

## Rules

1. The classification result should cover the same claims as the proof bundle for the same bundle id.
2. `routeSummary` must equal the count of item routes.
3. `leanBacked` should state whether the current control boundary has a public Lean-backed predicate for the referenced controls.
4. This artifact records routing, not verdicts. It should not be used as a substitute for the proof bundle or verification result.
