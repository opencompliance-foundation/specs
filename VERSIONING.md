# Versioning

## Scope

This document describes how OpenCompliance artifact formats should evolve before `1.0`.

## Rules for `0.x`

1. Draft releases may make breaking changes.
2. Every breaking change must update:
   - the relevant artifact spec,
   - the public example bundle,
   - the conformance vectors.
3. Field removals and semantic re-interpretations count as breaking changes.
4. New optional fields are allowed in `0.x` without a major version bump.
5. New required fields should trigger a minor draft version increment and updated conformance fixtures.

## Stability target for `1.0`

The project should not claim `1.0` until all of the following are true:

- at least one independent implementation can read the artifacts,
- conformance vectors are executable rather than descriptive only,
- the witness and revocation semantics are stable enough to survive replay across releases.
