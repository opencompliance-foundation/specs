# Specs Status

## What exists today

- Draft format documents for the main public artifacts.
- Synthetic `ExampleCo` example bundles that follow those draft formats.
- A blocked Verify path via typed punch-lists, a first-class failed-claim path for present-but-bad evidence, a first-class stale-evidence path for expired claims, and a certificate path via the issued synthetic corridor.
- Replay-bundle artifacts that pin the public synthetic rerun inputs and expected outputs.
- Seed OSCAL projections for the same synthetic examples.
- Conformance vectors derived from the same examples.
- Draft linkage rules from proof-bundle claims into synthetic corridor control identifiers.
- A machine-readable control-boundary file for the current synthetic corridor.
- Explicit mapping-maturity metadata that says the current public corridor is still family-proxy and names the exact-anchor target state.
- A draft mapping-methodology note and a control-boundaries schema so mapping maturity and review intent are machine-checkable.
- Draft JSON Schemas for the main machine-readable verification artifacts, now exercised by the public conformance check.
- A draft classification-result artifact and schema for the public prove/attest/judgment routing surface, plus a first public `mixedControls` decomposition format in the medium ExampleCo corridor.
- The proof-runner output now derives Lean batch imports and verified claim bindings from control-boundary metadata and surfaces omitted proved claims as explicit boundary inventory instead of silently dropping them.
- Draft lifecycle and composed-certificate artifacts for drift handling, delta recheck planning, and higher-level certificate composition.
- A draft signed-artifact manifest format plus synthetic public example signature bundles over the issued and lifecycle packs.
- Draft transparency-log and inclusion-proof artifacts plus public transparency outputs for the synthetic ExampleCo corridors.

## What does not exist yet

- No normative schema registry.
- No compatibility guarantees beyond `0.x` draft expectations.
- No signed release process for these formats.
- No independent implementation conformance programme.
- No reviewed clause-, Annex A-, criterion-, or point-of-focus anchor set for the public corridor yet.

## Publishing rule

If the examples and the specs diverge, the mismatch is a bug.
