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
