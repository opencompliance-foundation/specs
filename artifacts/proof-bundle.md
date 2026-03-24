# Proof Bundle

## Purpose

A proof bundle is the machine-readable result of one verification run.

It is the artifact that later verification-result envelopes, punch-lists or certificates, signing, transparency logging, replay, and witness verification depend on.

## Minimum required fields

- `bundleId`
- `generatedAt`
- `verifierVersion`
- `organisation`
- `scope`
- `claims`
- `summary`
- `proofRunner`

## Claim object

Each claim entry should include:

- `claimId`
- `title`
- `result`
- `frameworkMappings`
- `controlRefs`
- `evidenceRefs`
- `basis`

## Allowed result values

- `proved`
- `attested`
- `failed`
- `judgment_required`
- `evidence_missing`

## Bundle rules

1. The same evidence package under the same verifier version should produce the same bundle content.
2. Evidence references must be stable identifiers, not opaque prose.
3. A proof bundle may be published without a certificate.
4. A proof bundle is replayable only if its required inputs are pinned or disclosed well enough for independent rerun.
5. A proof bundle does not by itself say whether a scoped certificate was issued or withheld. That decision belongs in the verification-result envelope.
6. If a claim is marked `proved`, the proof bundle should disclose which proof runner checked the decidable slice.

## Proof runner object

The `proofRunner` object should include:

- `batchId`
- `fixture` or equivalent scope identifier
- `status`
- `theoremCount`
- `verifiedTheorems`

Allowed status values:

- `verified`

## Framework mapping entry

Each framework mapping entry should include:

- `framework`
- `family`
- optional `controlId`

## Control reference rule

`controlRefs` should identify the narrow OpenCompliance corridor controls that the claim is asserting.

If a claim is intentionally outside the current formal corridor, `controlRefs` may be empty, but that should be a deliberate boundary choice rather than drift.

## Evidence-backed mapping rule

If a claim has `evidenceRefs`, the claim's `frameworkMappings` should match the union of the mapped evidence claims unless the mismatch is explicitly documented as a transformation or reduction step.
