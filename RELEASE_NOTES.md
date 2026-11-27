# Release Notes

## v1.1.30
GH#1334 — re-pin `segment-audience`→1.0.7 so the published fix for the `source` slot reaches this workflow.

The prompt and its skill declared `context_params.source` differently: the skill said `supplied_by: input`, the prompt said nothing. The engine refuses a slot whose two declaration sites disagree rather than choosing between them, so the step could not run. GH#1162 fixed the prompt and published it on 2026-11-08; this package still pinned the version before that fix, which is why it reaches you only now.

No behaviour change beyond the step working: nothing in this workflow produces the material the slot wants — it comes from the person running the skrpt, which is what both sites now say. Checksums resolved from the live catalogue rather than transcribed.

## v1.1.29
GH#1144 part 1 round 2 — re-pin `audience-segmentation`→1.0.3 so the newly declared `supplied_by: input` slot is in scope. A declaration against a pin that predates it is inert: until this re-pin the engine's GH#1139 shape gate could not see it. Checksums resolved from the live catalogue rather than transcribed. No behaviour change here — this step makes the existing `from_input` binding(s) enforced rather than merely correct.

## v1.1.28
GH#1144 part 1 — the `segment-audience` step bound its `source` slot ("Product or Campaign") `from_step: "Launch Messaging Development"`. No workflow step produces a product description, so that was a guess at a producer rather than a supply. It now binds a new required workflow input, `product_or_campaign`, matching the four sibling consumers. This is the binding GH#1139 was filed over: once the slot declares `supplied_by: input`, the old form is refused rather than merely wrong.

## v1.1.27
GH#1100 consumer wave batch 5 — declare the data flow these steps were resolving positionally. 3 binding(s) added: `segment-audience` ← Launch Messaging Development; `create-image-brief` ← Audience Segmentation; `check-consistency` ← Launch Plan Development. Each dependency was also re-pinned to the version that introduced its `source` slot, with checksums resolved from the live catalogue rather than transcribed — a binding against a pin below the slot version is declared but inert, which the canonical scan reports as `execution_bindings_unused_key`.

`segment-audience` is bound to **Launch Messaging Development**, not to the step that precedes it: its slot is labelled "Product or Campaign", and the adjacent predecessor is post-launch measurement. Binding by position would have fed a measurement plan to a slot asking for the product.

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
