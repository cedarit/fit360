# Lat Pulldown Lab — curriculum specification

**Position in curriculum:** Term 1, Module 4, Chapter 4.6 (flagship lab). Prerequisites: [1.4](../term-01-the-body.md#module-1-anatomy-for-movement) (muscle naming), [4.1](../term-01-the-body.md#module-4-movement-vocabulary-and-introductory-biomechanics) (joint actions), [4.2](../term-01-the-body.md#module-4-movement-vocabulary-and-introductory-biomechanics) (force, torque, leverage), [4.5](../term-01-the-body.md#module-4-movement-vocabulary-and-introductory-biomechanics) (descriptive, non-evaluative language).

**Status:** curriculum specification with sourced final content for the "Explanations" section below (FIT-30), drafted once all four prerequisite chapters (1.4, 4.1, 4.2, 4.5) had lessons drafted. No app feature is built from this document yet, and the prerequisite lessons are themselves still on open, unmerged branches at time of writing.

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

## Explanations (sourced final content)

The content below (FIT-30) replaces the earlier claim-category placeholders now that all four prerequisite chapters have drafted lessons. Every claim is traced to a specific verified source; nothing here is invented, and roles or muscles that could not be directly verified are named explicitly as excluded rather than guessed (see "Source limitations" at the end of this section).

### Joint actions, per state

Applying the joint-action vocabulary from [Lesson 4.1.1](../lessons/term-01-module-4-chapter-1-lesson-1.md) to the movement path described in ACE's Exercise Library entry for the [seated lat pulldown](https://www.acefitness.org/resources/everyone/exercise-library/158/seated-lat-pulldown/) (learner reaches up to grasp the bar, then pulls it down toward the chest, leading with the elbows moving down and back):

| State | Shoulder | Elbow |
| --- | --- | --- |
| Start (dead-hang / starting position) | Flexed (arms extended overhead) | Extended |
| Pull (concentric phase) | Extension and adduction | Flexion |
| Controlled return (eccentric phase) | Flexion and abduction (reversing the pull, under control) | Extension |

This table is descriptive kinematic reasoning built from Lesson 4.1.1's already-cited joint-action vocabulary; per the sourcing note below, it does not need a separate claim-specific citation beyond that vocabulary's own sourcing.

### Muscle roles ("commonly described as")

Sourced to OpenStax, *Anatomy and Physiology 2e*, [§11.5, "Muscles of the Pectoral Girdle and Upper Limbs"](https://openstax.org/books/anatomy-and-physiology-2e/pages/11-5-muscles-of-the-pectoral-girdle-and-upper-limbs) (verified directly before citing; same CC BY-NC-SA licensing consideration as every other OpenStax citation in this curriculum, see [DECISIONS.md](../../DECISIONS.md#open) #12):

- **Latissimus dorsi (general anatomy sourced; exercise-specific "primary mover" role unresolved):** §11.5's figure legend states that "the muscles that move the humerus inferiorly generally originate from middle or lower back (e.g., latissimus dorsi)." That is a general anatomical statement about which muscles move the humerus inferiorly — it does not itself say latissimus dorsi is *this exercise's* primary mover, and Codex's review correctly caught that this document had overstated it. Assigning a specific "primary mover" role to this exercise needs a direct, exercise-specific source (for example, a verified fetch of ExRx.net or a comparable exercise-science reference), which this task could not obtain (see Source limitations below). Until such a source is found and verified, the exercise-specific primary-mover assignment is left as an **explicit unresolved content requirement**, not a settled claim — only the general anatomical fact above is asserted.
- **Contributors:**
  - The **teres major** is commonly described as a contributor: §11.5 states it "extends the arm, and assists in adduction and medial rotation of it" — the same shoulder actions (extension and adduction) as the pull phase above. This role survives review because the source directly states teres major's own action, matching the movement described, rather than only offering an illustrative example the way the latissimus dorsi figure legend does.
  - The elbow flexors — **biceps brachii, brachialis and brachioradialis** — are commonly described as contributors during the pull's elbow-flexion component: §11.5 states "the forearm flexors include the biceps brachii, brachialis, and brachioradialis."
- **Stabilisers:**
  - The **rhomboid major and rhomboid minor** are commonly described as stabilising the scapula: OpenStax's table of muscles that position the pectoral girdle lists both muscles' movement as "Stabilizes scapula during pectoral girdle movement," distinct from trapezius in the same table, whose listed movement is "elevates shoulders (shrugging); pulls shoulder blades together; tilts head backwards" — a mover, not a stabiliser, per this specific table, so trapezius is deliberately not included as a stabiliser here.
  - **Rotator cuff (anatomy sourced; stabilising role unresolved):** §11.5 states "the tendons of the deep subscapularis, supraspinatus, infraspinatus, and teres minor connect the scapula to the humerus, forming the rotator cuff (musculotendinous cuff), the circle of tendons around the shoulder joint." That sentence defines the rotator cuff anatomically; it does not itself state that the rotator cuff stabilises the shoulder joint, and Codex's review correctly caught that gap too. As with the primary-mover claim above, this document does not assert a stabilising role for the rotator cuff until a source directly supports it — left as an **explicit unresolved content requirement**, not a settled claim.

Every settled role above uses "is commonly described as," never "your muscle activates" or "the primary mover for you," per this document's own requirement. The two items marked "unresolved" are deliberately not phrased as settled roles at all, per Codex's review.

### Movement-path description

The bar travels from an overhead position down toward the upper chest, with the elbows leading the movement downward and back during the pull, and reversing during the controlled return (ACE Exercise Library, "Seated Lat Pulldown": "initiate the downward pull by first depressing... your scapulae, then pulling the bar downward towards the top or mid-section of your chest... in a motion that drives your elbows directly down towards the floor," continuing "until the bar nears or touches your chest, or... you observe your elbows no longer moving downward, but now beginning to move backwards"). This is a kinematic, descriptive claim built from vocabulary already sourced in Module 4; per this document's own rule, it needs no claim-specific citation beyond that vocabulary's own sourcing and the movement-path source above.

### Grip width / attachment and leverage

Applying Lesson 4.2.1's force/torque/lever-arm framework: changing grip width or attachment changes the geometry of the pull, which changes the torque relationships at the shoulder and the muscle force needed to produce the same movement — consistent with Lesson 4.2.1's general finding that changing a lever arm changes the torque needed at a joint, without specifying which muscle "works hardest" as a result. This is general biomechanical reasoning, not a specific effect size, exactly as this document's "Source requirements" section below requires; no source found or cited claims a specific numeric or comparative effect of grip width on this exercise, so none is asserted.

### Source limitations

- An automated search surfaced a broader, ExRx.net-style muscle list for this exercise (including posterior deltoid and triceps long head as a "dynamic stabilizer"). ExRx.net itself could not be fetched directly (blocked by a bot-detection challenge), and a second attempt to verify additional muscle roles from the OpenStax source itself produced a contradictory, anatomically implausible reading (describing "elbow" movements for muscles that act at the shoulder) on retry with the same tool. Given this contradiction, posterior deltoid and triceps are **not** included above — only roles independently confirmed against the raw, directly-fetched source text are included. This is a real gap, not a settled exclusion: if a future task finds and verifies a reliable source for these additional roles, they can be added then.
- §11.5 does not give a single sentence directly stating "latissimus dorsi extends and adducts the arm" in the same explicit phrasing used for teres major; its only direct statement about latissimus dorsi's action is the figure legend's "moves the humerus inferiorly." Codex's review correctly caught that this general statement, and the rotator cuff's anatomical definition, had been overstated into exercise-specific "primary mover" and "stabilises the shoulder joint" claims respectively. Both are now recorded as unresolved content requirements instead (see "Muscle roles" and "Open questions" above) rather than settled claims.
- This section makes no population-specific claim, so no Indian-population evidence caveat applies.

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

Not a product decision, but a genuine content gap: the "Muscle roles" section above leaves the exercise-specific "primary mover" (latissimus dorsi) and "stabilises the shoulder joint" (rotator cuff) assignments as unresolved content requirements rather than settled claims, after Codex's review correctly found the previously-cited OpenStax passages support the general anatomy but not those specific exercise-role assignments. Before any app feature builds a "primary mover" or "rotator cuff stabiliser" toggle state for this lab, a directly-verified, exercise-specific source is needed for those two roles (for example, a successfully-fetched ExRx.net page, or a comparable exercise-science reference) — this is future sourcing work, not a design decision, and should not be filled in with an invented or unverified role assignment.

Otherwise, no open question specific to this lab beyond what [DECISIONS.md](../../DECISIONS.md#open) already tracks. The quiz-scoring recommendation above is noted as a recommendation precisely so it isn't mistaken for a decision.
