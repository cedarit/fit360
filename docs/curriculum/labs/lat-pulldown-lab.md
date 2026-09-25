# Lat Pulldown Lab — curriculum specification

**Position in curriculum:** Term 1, Module 4, Chapter 4.6 (flagship lab). Prerequisites: [1.4](../term-01-the-body.md#module-1-anatomy-for-movement) (muscle naming), [4.1](../term-01-the-body.md#module-4-movement-vocabulary-and-introductory-biomechanics) (joint actions), [4.2](../term-01-the-body.md#module-4-movement-vocabulary-and-introductory-biomechanics) (force, torque, leverage), [4.5](../term-01-the-body.md#module-4-movement-vocabulary-and-introductory-biomechanics) (descriptive, non-evaluative language).

**Status:** curriculum specification only, drafted for review under FIT-5. No app feature is built from this document yet.

## What this lab is, and what it is not

The Lat Pulldown Lab is an **educational movement map**. It shows which muscles are commonly described as involved in a lat pulldown and why, and how the movement path and joint actions change across the rep. It is **not an EMG display**, does not show or imply measured muscle activation, and must never present activation percentages — real, estimated, illustrative or implied by wording ("fires more," "works harder," "targets X more than Y").

This distinction governs every section below. Where a requirement conflicts with making the lab feel more like a personal training or diagnostic tool, this document resolves it in favour of staying an educational map.

## Learner outcomes

By the end of the lab, a learner should be able to:

1. Identify, on a front and posterior view, the muscles commonly described as primary movers, contributors and stabilisers in a lat pulldown, using the prime-mover/synergist/stabiliser vocabulary from Chapter 1.4.
2. Describe the joint actions occurring at the shoulder and elbow across the start, pull and controlled-return states, using the vocabulary from Chapter 4.1.
3. Explain, in general and qualitative terms, how changing grip width or attachment relates to torque and leverage at the shoulder (Chapter 4.2), without claiming it changes which muscle "activates most."
4. Describe the movement using only neutral, descriptive language (Chapter 4.5) — never labelling a variant as safe/unsafe or normal/abnormal for an individual learner.

## Interaction states

| State | What it represents | What the lab explains |
| --- | --- | --- |
| Start (dead-hang / starting position) | The top of the rep, arms extended overhead holding the bar | Starting joint positions at shoulder and elbow; which muscles are lengthened; what is held isometrically before the pull begins |
| Pull (concentric phase) | The bar travelling down toward the body | The joint actions producing the movement (for example shoulder extension and adduction, elbow flexion); which muscles are commonly described as primary movers during this phase |
| Controlled return (eccentric phase) | The bar returning to the start under control | That the same muscles are commonly described as controlling the return; why "controlled" is a description of tempo, not a coaching instruction — this is the natural place to reinforce that the lab describes movement, it doesn't prescribe it |

**Views:** front and posterior, matching [PROJECT_CONTEXT.md](../../PROJECT_CONTEXT.md#first-interactive-lab).
**Toggle groups:** primary movers / contributors / stabilisers, shown independently so a learner can isolate one group at a time.
**Slider:** scrubs continuously through the rep (start → pull → controlled return); muscle highlighting and joint-action text update live as the learner moves it.

## Explanations (content requirements)

Each explanation below is a claim category, not final copy. Final copy is written when the lab is drafted for real, against the sources named in "Source requirements."

- **Joint actions at the shoulder and elbow, per state** — an anatomy/kinesiology-textbook-level claim (for example the general description of shoulder extension/adduction and elbow flexion during a pulling motion).
- **Which muscles are "commonly described as" primary movers, contributors or stabilisers** — phrased exactly that way ("commonly described as"), never as "your muscle activates" or "the primary mover for you," and sourced to anatomy/biomechanics textbooks or professional-organisation resources.
- **Movement-path description** (the bar's path relative to the body) — a kinematic, descriptive claim built from the vocabulary already sourced in Module 4; it does not need a claim-specific citation beyond that vocabulary's own sourcing.
- **Grip width / attachment and leverage** — general biomechanical reasoning only (wider or narrower grip changes the lever arm and therefore the torque demand at the shoulder), explicitly not tied to a claimed change in which muscle "works hardest."

## Quiz approach

Formative and ungraded, consistent with Module 4's assessment approach. No score gates progress — the lab is a comprehension tool, not a certification. (This is a recommendation for Pankaj's review, not a settled product decision; if a later product decision wants the lab gated or scored, that is a separate call, not made here.)

Suggested items (4–6 total):
- Label-the-muscle-group items: given a diagram state, mark a muscle as primary mover, contributor or stabiliser.
- Match-the-joint-action items: given a rep state (start / pull / controlled return), match the joint action occurring at a named joint.
- At least one "spot the unsafe language" item, reusing the Chapter 4.5 rewrite skill: show a claim such as "pulling behind the neck is dangerous" or "this proves the lats fire hardest here," and ask the learner to identify what's wrong with it (an unqualified individual safety verdict, or an invented activation claim).

## Source requirements

- Every muscle-involvement and joint-action claim needs at least one source that meets the [evidence policy](../../PROJECT_CONTEXT.md#4-evidence-policy) — textbooks and professional-organisation resources (evidence-policy tiers 3–4) are the expected minimum; prefer a systematic review or primary source (tiers 1–2) wherever one exists for a specific claim.
- Any claim about how grip width or attachment affects the exercise must be presented as general biomechanical reasoning, not a specific effect size, unless a specific cited source supports a specific claim — and even then, activation percentages stay excluded regardless of source. That exclusion is a product-level line, not a question of evidence strength.
- Record source limitations in the lab itself with a short "how sure are we" note, consistent with how Module 0 (Chapter 0.2) teaches evidence literacy — for example, naming whether a muscle's "contributor" role is broadly agreed or debated across sources.
- No number, percentage or study result may be invented to fill a gap in the available sources. If a source doesn't exist for a claim, the claim is cut, softened to purely descriptive language, or flagged as unresolved — never guessed.

## Safety wording

- The lab never says a technique variant is "safe," "unsafe," "correct" or "incorrect" for the learner individually (Chapter 4.5's rule applies directly).
- The lab gives no load, rep or programming recommendations — that is Term 2/3 scope, and even there, only through transparent, editable rules, never through this lab.
- If the lab later allows free-text or AI-assisted questions from a learner (a future product decision, not part of this spec), those questions are bound by the AI assistant rules in the [safety and AI policy](../../product/safety-and-ai-policy.md): grounded, bounded, no diagnosis or interpretation of individual results, and the standing referral line for any reported symptom.
- The standing referral line is shown or linked wherever the lab's copy discusses discomfort or pain during the movement.

## Explicit exclusions

The lab must never include:

- EMG data, EMG-style visuals, or wording that implies measured activation ("fires more," "activates 80%," "targets X% more than Y") — under any framing, including ranges, hedged language ("roughly"), or comparisons ("more than").
- Individual injury-risk claims ("this is dangerous for your shoulder").
- Form-correction or coaching cues framed as fixing a fault (for example a verdict like "your elbows are too far forward") — the lab describes movement; it does not coach or correct it.
- Programming or load prescription (sets, reps, weight).
- Rehabilitation or conditional clinical guidance (for example "if you have shoulder pain, avoid this") — that belongs to the standing referral line, not lab content.

## Open questions

None specific to this lab beyond what [DECISIONS.md](../../DECISIONS.md#open) already tracks. The quiz-scoring recommendation above is noted as a recommendation precisely so it isn't mistaken for a decision.
