# Witness Receipt

## Purpose

A witness receipt records that an independent replay reproduced the expected artifact digests.

It is not a claim that the underlying controls are good. It is a claim that the replay matched.

## Minimum required fields

- `receiptId`
- `issuedAt`
- `bundleId`
- `verifierVersion`
- `replayResult`
- `checkedArtifacts`

## Allowed replay results

- `exact_match`
- `digest_mismatch`

## Checked artifact entry

Each checked artifact entry should include:

- `artifactType`
- `path`
- `sha256`

## Rules

1. A receipt may only be issued for `exact_match`.
2. Digest mismatches must block witness issuance rather than downgrade to a warning.
3. The receipt should identify exactly which artifacts were checked.
4. A serious receipt should include the replayed result and the pinned inputs that materially determined it, not only the final bundle.
