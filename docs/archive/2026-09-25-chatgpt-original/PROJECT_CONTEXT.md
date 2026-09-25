# Fit360 project context

**Product, project, and repository name:** Fit360  
**Tagline:** Learn · train · understand

Fit360 is a personal, university-style fitness and health-science learning system. It is initially for Pankaj’s own learning and safe application with family—not primarily a trainer credential or an immediate professional coaching business.

## Purpose and learning objective

Fit360 builds rigorous working knowledge of anatomy, physiology, biomechanics, exercise science, resistance and cardio training, nutrition, fat-loss and muscle-gain principles, supplementation, behavior change, aging and longevity, preventive-health literacy, recovery, evidence appraisal, and practical self-application.

A commercial CPT may later be a benchmark or optional learning resource, but it is not a prerequisite to begin learning. Do not copy certification content or proprietary models.

## Safety and scope boundary

Fit360 provides medical literacy, not medical practice. It may explain general concepts, support general low-risk education, and help learners form questions for qualified clinicians. It must not:

- Diagnose or interpret individual test results as a diagnosis.
- Prescribe treatment, medication, or a therapeutic diet.
- Provide rehabilitation.
- Give clinical AI recommendations.

Content must use clear, educational language and direct learners to qualified clinicians for symptoms, injury, illness, medication questions, test-result interpretation, or individualized therapeutic guidance.

## Evidence policy

Use sources in this order of preference:

1. Primary sources and authoritative guidelines.
2. Systematic reviews and meta-analyses.
3. Established textbooks.
4. Professional organizations.
5. Fit360’s original explanations and interactive labs, clearly linked to their sources.

AI is a teaching and design assistant, never the scientific authority.

## Learning architecture

The learning hierarchy is **Program → Term → Module → Chapter → Lesson → Lab/Quiz/Practical**.

Every chapter begins with:

- Why it matters
- Learning objectives
- Learner capabilities
- Prerequisites
- Keywords
- Concept map
- Safety and scope boundary
- Short diagnostic quiz

Every lesson follows: **question → explanation → visual/lab → self-check → practical observation → recall cards → sources**.

The canonical curriculum lives in [`docs/curriculum/`](curriculum/README.md).

## Term 1: The Body

Term 1 is **The Body**: anatomy, physiology, energy systems, and movement vocabulary. Its detailed outline is in [Term 1 — The Body](curriculum/term-01-the-body.md).

| Module | Focus |
| --- | --- |
| 0. Orientation | Evidence, scope, and safety |
| 1. Anatomy for Movement | Language; skeleton, joints, connective tissue; muscles |
| 2. Physiology of Movement | Nervous system; muscle; cardiorespiratory and endocrine foundations |
| 3. Energy Systems and Recovery | Energy systems, activity demands, and recovery foundations |
| 4. Movement Vocabulary and introductory Biomechanics | Movement terminology and introductory biomechanics |

Future terms are: **Movement; Adaptation; Nutrition; Evidence; Longevity**.

## First interactive lab

The flagship initial interactive lab is the **Lat Pulldown Lab**. It should include start, pull, and controlled-return states; front and posterior views; toggleable primary movers, contributors, and stabilizers; joint-action and movement-path explanations; a slider; source notes; and a quiz.

It is an educational movement map, not an EMG display. Never invent activation percentages.

## Product vision

- **Learn:** video, sources, quizzes, and evidence cards.
- **Understand by doing:** diagrams and simulations.
- **Train:** planner, exercise explainers, logs, and recovery.
- **Evaluate:** nutrition logging, measurements, evidence appraisal, and bounded self-experiments.

### Initial feature scope

- Personal dashboard
- Lesson player
- Workout planner and set-by-set log
- Exercise library
- Recovery check-in
- Evidence-card library
- Manual nutrition and meal logging

Workout recommendations start as transparent, editable rules—not unbounded AI—and must show their rationale and safety limits. Do not use Expo initially; consider it only for meaningful native requirements.

## Technical direction

- Next.js, React, TypeScript, Tailwind CSS, and shadcn/ui
- Supabase PostgreSQL, Auth, RLS, and Storage as the preferred initial backend
- YouTube for video
- React Hook Form, Zod, and Recharts
- Interactive SVG, Canvas, or WebGL only where justified

Use original or licensed visual assets. Do not treat AI calorie estimates as truth.

### Core data shape

- `profiles`
- `courses`, `modules`, `chapters`, `lessons`, `sources`, `learner_progress`
- `exercises`, `programs`, `program_sessions`, `workout_logs`, `workout_sets`
- `daily_checkins`
- `foods`, `meals`, `meal_items`
- `evidence_cards`, `citations`

Private-record isolation must be proven with Supabase RLS tests.

## Engineering and delivery

Supported environments are a local developer laptop and production only. There is no shared staging environment. Optional pull-request previews may be added later, but never with real health data.

- `main` is the protected production branch.
- Each Jira issue uses a branch such as `feature/HP-123-description` (or an analogous name).
- Changes go through pull requests only; PR titles begin with the Jira key.
- Require one approval and passing checks before squash merge.
- Follow TDD: write a failing test, make the smallest passing change, then refactor.
- Use Vitest and React Testing Library for unit tests; local Supabase for integration tests; Playwright for E2E; and Playwright plus axe for accessibility.
- Required checks: typecheck, lint/format, unit/integration/E2E tests, dependency audit, and production build.
- Deploy only reviewed merges to `main`, with post-deploy smoke checks and a rollback plan.

## Collaboration

Claude Code may be used as a team collaborator for UI prototypes, interactive visualizations, and focused implementation. All work still passes requirements, safety, source, test, and pull-request review standards.

## Current priority

Curriculum comes first. Do not build broad app features until the course architecture and first vertical lesson slice are approved.
