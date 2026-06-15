# Codex Judge Eval Run - 2026-06-15

- Evaluation target: **Marginalia TV authored prototype**
- Judge: **Codex rubric judge**
- Generator: **none - authored/static fixture data**
- Rubric: `rubric.json`
- Test cases: **8**
- Judged cases: **7**
- Not executable in authored/static UI: **1**
- Errors: **0**
- Overall executable weighted score: **4.96 / 5**

## Method

Codex judged the current authored prototype against the five criteria in `rubric.json`.

This run did **not** use Claude, did **not** call an external LLM judge, and did **not** test live generation from `known_source_facts`. It evaluates whether the current seeded demo satisfies the rubric.

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
| easy-01-the-boys-s4-finale | easy | pass | 5 | 5 | 5 | 5 | 5 |
| easy-02-the-boys-s3-return | easy | pass | 5 | 5 | 5 | 5 | 5 |
| realistic-01-the-boys-season-five-prep | realistic | pass | 5 | 5 | 5 | 5 | 5 |
| realistic-02-house-of-the-dragon-release-week | realistic | pass | 5 | 5 | 5 | 5 | 5 |
| realistic-03-unsupported-show-no-fabrication | realistic | pass | 5 | 5 | 5 | 4 | 4 |
| hard-01-the-boys-user-note-season-five-leak | hard | pass | 5 | 5 | 5 | 5 | 5 |
| hard-02-the-boys-sparse-facts | hard | not executable in static UI | n/a | n/a | n/a | n/a | n/a |
| adversarial-01-season-five-leak-probe | adversarial | pass | 5 | 5 | 5 | 5 | 5 |

## House Of The Dragon Result

`realistic-02-house-of-the-dragon-release-week` scored **5 / 5** across all rubric criteria.

- **Spoiler boundary:** Bounded through `S02E08`; excludes Season 3 episode events, reviews, trailer beats, and book-forward outcomes.
- **Hallucination grounding:** Characters, relationships, secrets, and readiness anchors are supported by manually seeded Season 1-2 fixture facts.
- **Story-state correctness:** Rhaenyra, Daemon, Alicent, Aegon, Aemond, Helaena, Jace, Corlys, and the new dragonriders are represented at the correct S02E08 state.
- **Structural completeness:** Includes boundary banner, summaries, timeline, relationship map, character status, secrets/power state, and checklist.
- **Watch readiness:** Gives the key faction, dragonrider, knowledge-state, and mobilization anchors needed before `S03E01`.

## Threshold Read

Codex judge result: **passes executable authored-prototype rubric eval**.

The only unjudged case is `hard-02-the-boys-sparse-facts`, which requires a runtime generation path that accepts constrained `known_source_facts`. The current prototype is authored/static, so that case remains a generation-path test rather than a UI test.
