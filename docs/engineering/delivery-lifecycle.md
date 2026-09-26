# Fit360 delivery lifecycle

Fit360 ships curriculum-informed, safe, tested changes through a small, traceable lifecycle. It applies to all three team members: Pankaj, Claude and Codex.

**Repository:** https://github.com/cedarit/fit360
**Jira project key:** `FIT`

## Environments

- **Local development:** implementation, automated tests and developer checks.
- **Production:** released software.
- **Optional later:** pull-request preview deployments with **synthetic data only**. Never real users' data.

There is no shared staging environment.

## Roles

| Who | Does | Does not |
| --- | --- | --- |
| Pankaj | Owns Jira, approves curriculum and safety wording, handles releases; merges any PR the cross-reviewer hasn't unambiguously cleared, any safety-policy change, and any non-curriculum/process change | Approve their own work (not applicable) |
| Claude | Works assigned Jira issues on its own branch; reviews Codex's PRs; may squash-merge its own ordinary curriculum PR once Codex reports no blockers (see AGENTS.md's conditional auto-merge rule) | Approve its own work; merge a PR that isn't clearly cleared, a safety-policy change, or a non-curriculum change, without Pankaj |
| Codex | Works assigned Jira issues on its own branch; reviews Claude's PRs; may squash-merge its own ordinary curriculum PR once Claude reports no blockers (see AGENTS.md's conditional auto-merge rule) | Approve its own work; merge a PR that isn't clearly cleared, a safety-policy change, or a non-curriculum change, without Pankaj |

## Lifecycle

1. **Frame:** create or refine a Jira issue with the user need, acceptance criteria, curriculum impact, safety implications, content and source needs, and an **assignee** (Pankaj, Claude or Codex).
2. **Plan:** identify the affected areas and define the test approach before implementation.
3. **Develop with TDD:** write a failing test, make the smallest change that passes, then refactor with tests green.
4. **Verify locally:** run unit and integration tests. Run Playwright for user-facing flows. Check accessibility and safety copy where relevant.
5. **Pull request:** push a focused branch (`feature/FIT-123-description`, `fix/…`, `docs/…`, `content/…`). The PR title starts with the Jira key. Include test evidence, and screenshots or recordings for UI changes.
6. **Review:** the other AI reviews first where practical, then Pankaj. The reviewer checks code, tests, safety wording, sources and scope.
7. **Merge and release:** squash merge only after checks pass. For an ordinary curriculum PR the cross-reviewer has unambiguously cleared, the author may squash-merge directly (see AGENTS.md's conditional auto-merge rule); every other PR still needs Pankaj's approval and merge. Deploy, run smoke checks and have a rollback plan.
8. **Observe:** log defects, feedback, safety concerns and follow-ups in Jira. Urgent safety issues come first.

## Handoffs between collaborators

- Jira and the PR are the source of truth for status. Leave a short "done, tested, remaining" note there before stopping.
- Decisions and open questions go in [`docs/DECISIONS.md`](../DECISIONS.md).
- Always `git pull` and `git status` before starting. Never work on another collaborator's branch unless the issue is reassigned.

## Test layers

| Layer | Tools | Typical coverage |
| --- | --- | --- |
| Unit | Vitest, React Testing Library | Utilities, components, validation, learning-state logic, workout rules |
| Integration | Local Supabase | Routes, persistence, authorisation, RLS isolation |
| End-to-end | Playwright | Navigation, lesson progression, workout logging, safety disclosures |
| Accessibility | Playwright plus axe | Key screens |
| AI safety (later) | Automated prompt test set | Assistant refusals and referrals, per the safety policy |

## Required checks

Typecheck, lint and format, unit, integration and E2E tests, dependency audit, and production build. AI safety tests are added once the assistant exists.

## Required safeguards

- Curriculum and safety-boundary changes are first-class acceptance criteria.
- Never merge unreviewed clinical-sounding language, or diagnosis, treatment, rehabilitation or therapeutic-nutrition functionality.
- No secrets and no real health data in code, fixtures, logs, screenshots or PRs.
- Keep changes focused and reversible; record trade-offs and test gaps in the issue or PR.
