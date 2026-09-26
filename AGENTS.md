# Fit360 — guidance for AI collaborators

Fit360 is built by a three-member team: **Pankaj Bhagat** (founder, product owner, final approver), **Claude** (Anthropic) and **Codex** (OpenAI Codex CLI). This file is the shared rulebook for both AI collaborators. `CLAUDE.md` points here so both tools read the same instructions.

## Read before any work

1. [docs/PROJECT_CONTEXT.md](docs/PROJECT_CONTEXT.md): what Fit360 is and why it exists.
2. [docs/product/safety-and-ai-policy.md](docs/product/safety-and-ai-policy.md): the scope boundary. It is not optional.
3. [docs/DECISIONS.md](docs/DECISIONS.md): decisions already made and questions still open. Do not reopen a settled decision without saying so explicitly.
4. The docs for your area: [curriculum](docs/curriculum/README.md), [roadmap](docs/product/roadmap.md), [business](docs/business/business-model.md) or [engineering](docs/engineering/delivery-lifecycle.md).

## Non-negotiable rules

- **Medical literacy, not medical practice.** Never add diagnosis, interpretation of an individual's test results, treatment, rehabilitation, medication advice or therapeutic-diet functionality or copy. See the safety policy for the in-app AI rules.
- **Sources over AI.** Neither Claude nor Codex is a scientific authority. Every factual health or fitness claim in content needs a source from the evidence policy. Never invent numbers, percentages, study results or muscle-activation data.
- **Curriculum is canonical.** `docs/curriculum/` is the source of truth for learning content. The app serves the curriculum, not the other way round.
- **No secrets and no real health data** in the repo, in test fixtures, in screenshots or in PR descriptions. Use synthetic data only.
- **Original or licensed assets only.** Do not copy certification-course material, proprietary models or other apps' designs. Design references (for example Mobbin) are for inspiration only.

## How the team works

- **Pankaj owns decisions.** Product scope, curriculum approval, safety wording and pricing are his calls. Merges to `main` are his calls too, except the narrow, conditional curriculum auto-merge described below. When a choice is his, say so and ask. Don't decide silently.
- **One Jira issue, one owner, one branch.** Each issue is assigned to Pankaj, Claude or Codex. Two agents never work on the same branch at the same time.
- **Cross-review.** Where practical, the AI that did not write a change reviews it before it merges. Reviewers check safety wording, sources, tests and scope as well as code.
- **Conditional auto-merge for curriculum PRs (decided 2026-09-26; see `DECISIONS.md`).** For an ordinary Term 1 curriculum PR — a Jira task under the FIT-5 epic, editing content under `docs/curriculum/` — once the cross-reviewing AI explicitly and unambiguously reports no blockers (for example "no blockers — cleared for auto-merge"), the author may squash-merge it to `main` directly, without waiting for Pankaj, and must record the merge in the PR and the Jira issue. If the reviewer's verdict is mixed, hedged or unclear, treat it as **not** cleared and wait for Pankaj, same as before.
  This does **not** apply to:
  - Any change touching `docs/product/safety-and-ai-policy.md` (that file's own header still requires Pankaj's explicit approval, regardless of reviewer verdict).
  - Any PR where the reviewer or author flags an open product decision that needs Pankaj's judgement, not just a content fix.
  - Any process, engineering, or non-curriculum change — including changes to this file (`AGENTS.md`) itself.
  This rule is bidirectional: it applies the same way whether Claude or Codex is the PR's author.
- **Leave a trail.** Before you finish, update the Jira issue or PR with what changed, what was tested and what's left. Record any new decision or open question in `docs/DECISIONS.md` rather than in chat, because the other collaborator can't see your chat.
- **Check before you touch.** Run `git status` and pull before starting. Never overwrite, reformat or "tidy" files outside your issue's scope.
- **Disagree in writing.** If you think a doc, decision or another agent's change is wrong, raise it in the PR or in `DECISIONS.md` with your reasoning, and let Pankaj decide.

## Engineering basics

- Branches are named `feature/FIT-123-short-description` (or `fix/`, `docs/`, `content/`). PR titles start with the Jira key.
- Write tests first (TDD) where practical. The required checks are typecheck, lint/format, tests, dependency audit and build.
- Full workflow: [docs/engineering/delivery-lifecycle.md](docs/engineering/delivery-lifecycle.md).
