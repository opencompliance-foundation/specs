# Review Pilots

This folder holds draft exact-anchor review pilots.

The purpose is to move OpenCompliance beyond family-proxy mappings without pretending that the whole standards corpus is already fully reviewed.

## Interpretation rule

These pilot files are not a claim of full framework coverage.

They are a narrow, review-oriented artifact that records:

- where exact public source anchors have already been reviewed,
- where exact anchors are still only candidates,
- and where exact anchor publication is blocked because the authoritative source text is proprietary or otherwise not publicly available for safe open publication.

## Review status meanings

- `public_source_reviewed`
  Reviewed internally against public official text or public official machine-readable artifacts.
- `candidate_public_source_unreviewed`
  A plausible exact anchor candidate exists, but the mapping is not yet strong enough to call reviewed.
- `blocked_nonpublic_source_review`
  The framework-specific exact-anchor review is blocked on licensed, non-public, or otherwise unavailable source material.

## Quality bar

An exact-anchor pilot should only mark an entry `public_source_reviewed` if all of the following are true:

1. The source anchor is identifiable without reproducing restricted source text.
2. The relation semantics are stated explicitly.
3. The rationale names the proof boundary rather than overstating the claim.
4. The mapping is strong enough to survive hostile review on its own terms.
5. The file still says what has not been reviewed yet.
