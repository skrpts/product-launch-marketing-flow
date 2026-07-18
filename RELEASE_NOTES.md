# Release Notes

## v1.1.26
GH#863 Wave 1 (#858-A1 class) — fix the intent/output mismatch (K-045): the bundle shipped `launch-plan-generator` (the launch plan) and `press-release-writer` (the press release) — both headline deliverables — plus docs telling you to run them, but the `execution:` block never invoked either, so those deliverables were never produced. Wired both as execution steps in dependency order behind new backing skills (**Press Release Writing**, **Launch Plan Development**) so they are `from_step`-addressable, and rewired every cross-step input from positional/title refs (`{{steps.<Title>.output}}`, `{{steps.previous.output}}`) to explicit `from_step` bindings via named `context_params` (`{{step.context.*}}`): the press release binds its positioning ← Launch Messaging Development; the launch plan binds positioning ← Launch Messaging Development and channel_strategy ← Channel Strategy. The launch plan is the primary deliverable and now runs as the last content step before polish. Completed the tail: repinned `polish-language` 1.0.1→1.0.6 (the version exposing the bindable `source` slot) and bound `language-polish`'s `source` ← the Launch Plan Development plan, so the `output_step` polishes the actual launch plan rather than its positional previous. No new required workflow inputs.

## v1.1.25
GH#745 — declare per-step `output: {name, type}` on every execution step (messaging/text, channel_strategy/text, measurement_plan/text, audience_segments/list, image_brief/text, consistency_verdict/decision, polished_plan/text). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.24
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 10 inline shared-content files and declare 10 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.23
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.22
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.21
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.20
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.19
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
