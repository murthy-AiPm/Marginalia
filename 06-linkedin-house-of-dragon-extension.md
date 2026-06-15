# LinkedIn Draft - House of the Dragon Extension

House of the Dragon Season 3 premieres on June 21, so I used it as a forcing function for my Marginalia TV prototype.

My first version tested a simple product question:

What if the real problem with returning to a long-running show is not remembering the plot, but reconstructing the story state?

For serialized shows, the memory gap is rarely just "what happened last season?"

It is:

- Who has power right now?
- Who knows the secret?
- Who betrayed whom?
- Which alliances are real vs. temporary?
- What can I safely remember before pressing play?

House of the Dragon is a good stress test for that because the Season 2 finale leaves viewers with a dense state:

- Rhaenyra has new dragonriders.
- Daemon has returned to her side after Harrenhal.
- Alicent has secretly offered a path into King's Landing.
- Aegon is injured and being moved by Larys.
- Aemond has Vhagar and the regency, but his advantage is less clean.
- Helaena refuses to become a weapon.
- Armies and fleets are finally moving.

A normal recap can summarize those events.

What I wanted to test was whether the product could restore the operating model before Season 3:

relationship map, character status, secrets/power state, and a ready-to-watch checklist, all bounded at S02E08 with no Season 3 trailer beats, reviews, or book-forward spoilers.

So I added House of the Dragon as a second seeded path in Marginalia TV and ran it through my rubric:

- Spoiler boundary
- Hallucination grounding
- Story-state correctness
- Structural completeness
- Watch readiness

Result: the House of the Dragon release-week path scored 5/5 across all five criteria in a Codex-judged rubric eval.

The bigger product lesson:

The model should not become more confident when facts are sparse. The product should become more honest about what it knows.

For this prototype, that meant treating the data layer as the product:

- structured facts
- episode boundaries
- claim-level provenance
- knowledge holders
- fallback behavior when coverage is weak

That is the part I would keep building.

Not "AI recap."

Story-state restoration before you press play.

## Shorter Version

House of the Dragon Season 3 premieres on June 21, so I used it as a release-week test for my Marginalia TV prototype.

The product question:

Can a recap tool do more than summarize plot?

For returning viewers, the harder problem is story state:

- Who has power?
- Who knows the secret?
- Who betrayed whom?
- Which alliances matter?
- What can I safely remember before the next episode?

I added a House of the Dragon path bounded at `S02E08 -> S03E01`.

The prototype restores:

- relationship map
- character status
- secrets / power state
- ready-to-watch checklist
- explicit spoiler boundary

Then I judged it against my eval rubric:

- spoiler boundary
- hallucination grounding
- story-state correctness
- structural completeness
- watch readiness

Result: **5/5 across all five criteria** for the House of the Dragon release-week path.

The lesson:

The product risk is not whether an AI can write a recap.

It is whether the system has enough bounded, structured facts to stay useful without becoming confidently wrong.

That is where I would keep investing: data quality, provenance, and honest fallbacks.

Not generic AI recap.

Story-state restoration before you press play.

## Suggested Visual

Use one screenshot of the House of the Dragon recap page plus a small rubric card:

| Criterion | Score |
|---|---:|
| Spoiler boundary | 5/5 |
| Hallucination grounding | 5/5 |
| Story-state correctness | 5/5 |
| Structural completeness | 5/5 |
| Watch readiness | 5/5 |

Caption idea:

`S02E08 -> S03E01, no Season 3 events, no trailer beats, no book-forward spoilers.`
