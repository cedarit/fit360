# Safety and AI policy

Fit360 provides **medical literacy, not medical practice**. This policy applies to all content (lessons, videos, evidence cards, app copy) and to every product feature, including the built-in AI assistant. Changes to it need Pankaj's explicit approval.

## What Fit360 may do

- Explain how the body works, and the general science of training, nutrition, body composition, ageing and lifestyle disease.
- Explain what a health test measures, why it exists and what published screening guidelines generally say, with sources.
- Summarise research in plain language, including its strength and limits.
- Give general training guidance and editable programmes to healthy adults, with the reasoning shown.
- Help a learner write down good questions to take to their doctor.

## What Fit360 must never do

- Diagnose a condition, or suggest that a person probably has or doesn't have one.
- Interpret a person's own test results as normal or abnormal, or as a verdict on their risk.
- Prescribe or adjust treatment, medication, or supplement doses for a medical purpose.
- Provide rehabilitation or injury-management programmes.
- Give therapeutic-diet advice (for example, diets to treat diabetes, kidney disease or other conditions).
- Encourage anyone to train through pain or concerning symptoms.

## Language rules

- Use educational, non-diagnostic language: "this test measures…" rather than "your result means…".
- Separate general education clearly from individual clinical care.
- Use the standing referral line wherever content touches symptoms, injury, illness, medication or test results: *"Stop and speak to a qualified doctor or clinician. Fit360 is education, not medical assessment or treatment."*

## Training features

- Before generating a programme, users complete a pre-activity readiness screen (a standard questionnaire such as PAR-Q+, used as licensed or permitted). If any answer is flagged, Fit360 advises seeing a clinician before starting and does not generate a programme.
- Programmes come from transparent, editable rules. Each recommendation shows its rationale, its source and its safety limits.
- Pain or symptoms logged in a check-in trigger the referral line. They never trigger an automatic "fix".

## Rules for the built-in AI assistant

1. **Grounded:** it answers from Fit360's approved curriculum, evidence cards and sources, and cites them. If Fit360 has no approved content on a topic, it says so instead of improvising.
2. **Bounded:** it follows every "must never" rule above, whatever the user's wording or insistence.
3. **Reports and results:** if a user shares or uploads their own lab report or values, the assistant may explain *in general* what each marker measures and link to the related lesson. It must not say whether the user's values are good, bad, normal or risky. It must direct them to their doctor and offer to help list questions for that visit. The product should discourage uploading reports and must not store them unless a decision says otherwise (see [DECISIONS.md](../DECISIONS.md)).
4. **Urgent symptoms:** chest pain, fainting, severe breathlessness, signs of stroke or similar trigger an immediate message to seek emergency care (in India, dial 112), not an explanation.
5. **Tested:** the assistant ships only with an automated test set of unsafe prompts (asking for a diagnosis, interpretation of a report, a medication dose, a rehab plan, an eating-disorder pattern, a minor user and so on). The tests must pass on every model or prompt change.
6. **Honest:** it states its uncertainty, never invents studies or numbers, and says it is an AI.

## Special groups

- **Under-18s:** not supported at launch (see the business model for the legal reason).
- **Pregnancy, chronic illness, eating disorders and recent injury:** general education only, plus the referral line. No programme generation.

## Review

Any content or feature that touches this policy lists "safety review" as an acceptance criterion in its Jira issue. The reviewer (the other AI and then Pankaj) checks the copy against this page before merge.
