# Proof Bundle

## Purpose

A proof bundle is the machine-readable result of one verification run.

It is the artifact that later signing, transparency logging, replay, and witness verification depend on.

## Minimum required fields

- `bundleId`
- `generatedAt`
- `verifierVersion`
- `organisation`
- `scope`
- `claims`
- `summary`

## Claim object

Each claim entry should include:

- `claimId`
- `title`
- `result`
- `frameworkFamilies`
- `evidenceRefs`
- `basis`

## Allowed result values

- `proved`
- `attested`
- `judgment_required`
- `evidence_missing`

## Bundle rules

1. The same evidence package under the same verifier version should produce the same bundle content.
2. Evidence references must be stable identifiers, not opaque prose.
3. A proof bundle may be published without a certificate.
4. A proof bundle is replayable only if its required inputs are pinned or disclosed well enough for independent rerun.
