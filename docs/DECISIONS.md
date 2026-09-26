# Fit360 decisions log

The shared memory for Pankaj, Claude and Codex. Record decisions here, not only in chat, because each collaborator can't see the others' conversations. Newest first within each section. Only Pankaj moves an item from **Open** to **Decided**.

## Decided

| Date | Decision | Notes |
| --- | --- | --- |
| 2026-09-25 | GitHub repository is `cedarit/fit360` | https://github.com/cedarit/fit360 |
| 2026-09-25 | Fit360 is to become a business (paid app) | Phased: learn → teach → practise → share → business. See roadmap. |
| 2026-09-25 | Team is Pankaj, Claude and Codex, with shared rules in `AGENTS.md` | `CLAUDE.md` imports `AGENTS.md`. |
| 2026-09-25 | Scope widened beyond workouts | Includes nutrition, supplements, body composition, lifestyle disease, preventive-test literacy, ageing and research literacy, all within the safety policy. |
| 2026-09-25 | Term 1 uses the five-module structure (0 Orientation to 4 Movement Vocabulary) | Reconciles the two earlier Codex-drafted versions. |
| 2026-09-25 | Jira project key `FIT` | Replaces the `HP-123` example. |
| 2026-09-25 | Pull-request previews allowed later, synthetic data only | Resolves a contradiction in the original docs. |
| 2026-09-25 | Adults only (18+) at launch | Legal simplicity for children's data. |
| 2026-09-26 | Module 0 (Chapter 0.1, Lesson 0.1.1 "What Fit360 is and isn't") is Term 1's first vertical lesson slice | Resolves former Open #10. Module 1's anatomy chapters follow in sequence once Module 0 is complete. |
| 2026-09-26 | Module 0 carries an explicit emergency pathway, separate from the ordinary clinician referral line | Chest pain, fainting, severe breathlessness, signs of stroke or similar require immediate emergency care; in India, dial 112. Ordinary "concerning symptoms" still route to the standing referral line (see a clinician when able). See `curriculum/term-01-the-body.md`, Chapter 0.3 and "Safe self-application." Mirrors the emergency-symptom rule already in `product/safety-and-ai-policy.md`'s AI assistant rules, now made explicit in the curriculum layer too. |
| 2026-09-26 | Ordinary Term 1 curriculum PRs (FIT-5 epic, `docs/curriculum/` content) may be squash-merged by their author once the cross-reviewing AI unambiguously reports no blockers, without waiting for Pankaj | Narrows "Pankaj merges everything." Does not apply to any change touching `docs/product/safety-and-ai-policy.md`, any PR flagging an open product decision, or any process/engineering/non-curriculum change (including changes to `AGENTS.md` itself) — those still need Pankaj regardless of reviewer verdict. A mixed, hedged or unclear reviewer verdict is treated as not cleared. Bidirectional between Claude and Codex. See `AGENTS.md` and `docs/engineering/delivery-lifecycle.md`. |
| earlier | Medical literacy, not medical practice | Core boundary. See the safety policy. |
| earlier | Curriculum first; `docs/curriculum/` is canonical | |
| earlier | Web stack: Next.js, React, TypeScript, Tailwind, shadcn/ui, Supabase | |
| earlier | Workout recommendations are transparent, editable rules | Not open-ended AI. |

## Open

| # | Question | Options and notes | Needed by |
| --- | --- | --- | --- |
| 1 | Mobile technology | (a) Expo / React Native sharing TypeScript with the web; (b) PWA first, native later; (c) native per platform. The original "no Expo" rule predates the business plan. | Phase 3 |
| 2 | AI assistant provider and design | Retrieval over approved Fit360 content; which model or provider; cost per user; safety test set. | Phase 3 |
| 3 | Pricing and revenue model | Freemium subscription, per-term purchase, or both; web versus in-app payments. | Phase 3 |
| 4 | Operating legal entity | Existing company or a new one. | Before beta |
| 5 | Lab-report uploads | Disallow entirely, or allow general marker explanations without storing the file. | Phase 3 |
| 6 | Content languages | English only at first, or Hindi and Telugu versions. | Phase 3 |
| 7 | Default split of work between Claude and Codex | Assign per Jira issue; possibly a default by area (curriculum and docs, UI prototypes, backend, tests). | Phase 0 |
| 8 | Order of Terms 2–6 | Proposed order is in `curriculum/README.md`. | After Term 1 approval |
| 9 | Pre-activity readiness screen | PAR-Q+ licensing and terms of use, or an alternative. | Phase 2 |
| 11 | Graded/gating Term 1 assessments | Every Term 1 chapter assessment drafted so far (FIT-5, FIT-6) is formative and ungraded. Open question: should any chapter or module assessment ever become a graded or gating check (for example, required to pass before a learner unlocks the next module, or before Term 2)? Affects `learner_progress` design and product scope, not curriculum content itself. | Before Term 1 assessments are built into the app, or before Term 2 sequencing |
| 12 | Citing/quoting CC BY-NC-SA academic sources (e.g. OpenStax) once Fit360 is a paid product | Lesson 1.1.1 (FIT-10) cites OpenStax *Anatomy and Physiology 2e*, which is CC BY-NC-SA (NonCommercial), not CC BY 4.0 as an earlier draft wrongly stated. Citing facts in original prose (not reproducing the source's text, tables or images) is standard practice and likely outside what the licence restricts, but Fit360's own rule is "original or licensed assets only" (AGENTS.md). Options: (a) keep citing/paraphrasing facts from NC-licensed academic sources in original wording indefinitely, treating that as distinct from "reusing" the licensed work; (b) never use any NC-licensed source's actual diagrams/images/tables, even paraphrased, without separate commercial permission (already implied by AGENTS.md, but not yet stated for text specifically); (c) get explicit legal sign-off on (a) before the app is a paid product. | Before any paid launch that reuses this kind of source |
