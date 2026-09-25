# Fit360 delivery lifecycle

Fit360 ships curriculum-informed, safe, tested product changes through a small, traceable delivery lifecycle.

## Environments

Only two environments are supported:

- **Local development** for implementation, automated testing, and developer verification.
- **Production** for released user-facing software.

There is no separate staging, QA, preview, or other deployed environment in this workflow.

## Lifecycle

1. **Frame the work:** create or refine a Jira issue with the user need, acceptance criteria, curriculum impact, safety implications, and evidence/content-review needs.
2. **Plan the change:** identify affected Next.js/React/TypeScript/Tailwind/Supabase areas and define the test approach before implementation.
3. **Develop locally with TDD:** write a failing focused test where practical, implement the smallest appropriate change, then refactor with tests passing.
4. **Verify locally:** run relevant unit and integration tests; run Playwright UI coverage for user-facing workflows; manually verify key accessibility and safety copy when relevant.
5. **Review through a pull request:** push a focused Git branch, open a PR linked to the Jira issue, include test evidence and screenshots or recordings when UI behavior changes, and request review.
6. **Merge and release:** merge only after required checks and review pass, then deploy to production according to the repository’s release process.
7. **Observe and learn:** capture defects, user feedback, safety concerns, and follow-up work in Jira. Urgent safety issues take priority.

## Test layers

| Layer | Purpose | Typical Fit360 coverage |
| --- | --- | --- |
| Unit | Verify isolated behavior quickly | TypeScript utilities, React components, validation, learning-state logic |
| Integration | Verify components work together | Next.js routes, Supabase interactions, authorization, persistence |
| UI / end-to-end | Verify critical user journeys | Playwright flows for navigation, learning progression, and safety disclosures |

## Required safeguards

- Treat curriculum and safety-boundary changes as first-class acceptance criteria.
- Never merge unreviewed clinical-sounding language, diagnosis, treatment, rehabilitation, or therapeutic nutrition functionality.
- Keep changes focused and reversible through Git and pull requests.
- Record material trade-offs, test gaps, and follow-up items in the Jira issue or PR.
