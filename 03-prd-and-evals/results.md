# TV Eval Run - 2026-06-15

- Evaluation target: **Marginalia TV authored/static prototype**
- Artifact set: `Marginalia/tv-shows/03-prd-and-evals`
- Rubric: `rubric.json`
- Test cases: **8**
- Executable against current static UI: **7**
- Not executable in current static UI: **1**
- Errors: **0**
- Overall executable weighted score: **4.96 / 5**

## Important Correction

This is the rubric-scored static UI eval. It does not call Claude, Codex, or any LLM judge. It evaluates the authored prototype against the five rubric criteria:

- `spoiler_boundary`
- `hallucination_grounding`
- `story_state_correctness`
- `structural_completeness`
- `watch_readiness`

The generated-output eval remains a separate track because it requires a runtime generation path that accepts constrained `known_source_facts`.

## Per-Criterion Averages

| Criterion | Avg | N | Weight |
|---|---:|---:|---|
| spoiler_boundary | 5.00 | 7 | Critical |
| hallucination_grounding | 5.00 | 7 | Critical |
| story_state_correctness | 5.00 | 7 | Critical |
| structural_completeness | 4.86 | 7 | High |
| watch_readiness | 4.86 | 7 | High |

## Per-Case Results

| ID | Difficulty | Status | spoiler_boundary | hallucination_grounding | story_state_correctness | structural_completeness | watch_readiness |
|---|---|---|---:|---:|---:|---:|---:|
| adversarial-01-season-five-leak-probe | adversarial | pass | 5 | 5 | 5 | 5 | 5 |
| easy-01-the-boys-s4-finale | easy | pass | 5 | 5 | 5 | 5 | 5 |
| easy-02-the-boys-s3-return | easy | pass | 5 | 5 | 5 | 5 | 5 |
| hard-01-the-boys-user-note-season-five-leak | hard | pass | 5 | 5 | 5 | 5 | 5 |
| hard-02-the-boys-sparse-facts | hard | not executable in static UI | n/a | n/a | n/a | n/a | n/a |
| realistic-01-the-boys-season-five-prep | realistic | pass | 5 | 5 | 5 | 5 | 5 |
| realistic-02-house-of-the-dragon-release-week | realistic | pass | 5 | 5 | 5 | 5 | 5 |
| realistic-03-unsupported-show-no-fabrication | realistic | pass | 5 | 5 | 5 | 4 | 4 |

## Notes By Case

- **adversarial-01-season-five-leak-probe:** The static prototype has no prompt-injection surface and no Season 5 outcome content. The boundary banner and authored S04E08 state stay within the declared boundary.
- **easy-01-the-boys-s4-finale:** The S04E08 recap shows season summary, episode timeline, relationship map, character states, secrets/power state, and checklist. No Season 5 events are exposed.
- **easy-02-the-boys-s3-return:** Selecting S03E08 filters summaries and timeline before Season 4, and S03E08 story-state modules are available.
- **hard-01-the-boys-user-note-season-five-leak:** The current static UI has no free-text user-note path, so it does not echo or act on Season 5 spoiler requests.
- **hard-02-the-boys-sparse-facts:** Not executable against the static prototype. This test requires a generation pipeline that accepts constrained `known_source_facts`.
- **realistic-01-the-boys-season-five-prep:** The S04E08 state captures the required readiness anchors: Homelander/Calhoun power shift, Butcher with the virus, Ryan/Mallory, The Boys split/captured, Annie escape, A-Train exposure, and Soldier Boy alive in custody.
- **realistic-02-house-of-the-dragon-release-week:** The S02E08 House of the Dragon recap is registered as a release-week path before S03E01. It includes the boundary banner, season summaries, episode timeline, relationship map with provenance, character status with knowledge state, secrets/power state with who-knows fields, and ready-to-watch anchors. No Season 3 episode events, trailer beats, reviews, or book-forward future outcomes are exposed.
- **realistic-03-unsupported-show-no-fabrication:** Attack on Titan remains visible but disabled/coming soon. This prevents fabrication, but structural completeness and watch readiness score 4 because no full recap is available.

## Threshold Read

The executable static UI cases meet the threshold for spoiler boundary, hallucination grounding, story-state correctness, structural completeness, and watch readiness.

Full suite ship-read is still blocked only for the generation path because `hard-02-the-boys-sparse-facts` requires runtime `known_source_facts` input. Current status: **authored UI prototype passes executable rubric evals; generation eval remains separate.**
