# Fit360 project context

**Product, project and repository name:** Fit360
**Tagline:** Learn · train · understand
**Founder and product owner:** Pankaj Bhagat
**Team:** Pankaj, Claude (Anthropic) and Codex (OpenAI Codex CLI). See [AGENTS.md](../AGENTS.md).

This is the full reference for anyone, human or AI, working on Fit360. The one-page version is the [project brief](PROJECT_BRIEF.md).

## 1. Origin and direction

Fit360 started as a personal goal: learn to train safely without paying for personal training. A commercial trainer certification was considered and set aside. Understanding the science matters more than the credential. The founder wants to guide himself by reasoning, knowing each do and don't and *why*, rather than by memorised terminology.

The scope then widened naturally. Training can't be separated from nutrition, diet, supplements, body composition (belly and visceral fat, and why they are common in Indians), lifestyle disease, preventive health tests, ageing, and the ability to read research as a layperson.

Teaching is the best form of learning, so the founder teaches what he learns through YouTube. The combination of learning, guidance, training plans, workout logs, easy access to reasoning and an in-built AI assistant is a product others would pay for. **Fit360 is now intended to become a business**, built in phases (see the [roadmap](product/roadmap.md)).

A commercial CPT or similar may still serve as a benchmark or an optional learning resource. It is not a prerequisite. Never copy certification content or proprietary models.

## 2. Learning scope

Fit360 builds rigorous working knowledge of:

- **The body:** anatomy, physiology, energy systems, movement vocabulary, introductory biomechanics
- **Training:** exercise technique, resistance and cardio training, programming, progression, recovery, and the dos and don'ts with their reasons
- **Nutrition:** energy balance, macronutrients, fat loss and muscle gain, Indian diets and foods, and supplements (evidence strength, safety, regulation)
- **Body composition and metabolic health:** body fat distribution, visceral fat, Asian-Indian body composition, and lifestyle diseases (for example type 2 diabetes, hypertension, fatty liver) *as literacy topics*
- **Preventive-health literacy:** what common tests measure, what screening guidelines generally say, and how to prepare useful questions for a doctor
- **Ageing and longevity:** muscle and bone with age, and training and nutrition across the lifespan
- **Evidence literacy:** study types, reading a research summary, relative versus absolute risk, and spotting hype
- **Behaviour change and self-application:** habits, adherence, and bounded self-experiments

The curriculum's structure and order live in [`docs/curriculum/`](curriculum/README.md).

## 3. Safety and scope boundary

Fit360 provides **medical literacy, not medical practice**. Full rules, including what the in-app AI may and may not do, are in the [safety and AI policy](product/safety-and-ai-policy.md). In short, Fit360 must never:

- Diagnose, or interpret an individual's test results as a diagnosis or risk verdict
- Prescribe treatment, medication or a therapeutic diet
- Provide rehabilitation
- Give clinical recommendations through AI or any other means

It *may* explain general concepts and what tests measure, summarise published guidelines with sources, support low-risk general training for healthy adults, and help learners form questions for qualified clinicians.

## 4. Evidence policy

Use sources in this order of preference:

1. Primary sources and authoritative guidelines (including Indian bodies such as ICMR where relevant)
2. Systematic reviews and meta-analyses
3. Established textbooks
4. Professional organisations
5. Fit360's own explanations and interactive labs, clearly linked to their sources

AI is a teaching and design assistant, never the scientific authority. Where evidence is weak, mixed or drawn from non-Indian populations, say so.

## 5. Learning architecture

The hierarchy is **Program → Term → Module → Chapter → Lesson → Lab/Quiz/Practical**.

Every chapter begins with: why it matters, learning objectives, learner capabilities, prerequisites, keywords, a concept map, the safety and scope boundary, and a short diagnostic quiz.

Every lesson follows: **question → explanation → visual/lab → self-check → practical observation → recall cards → sources**.

Every lesson is designed to work in three places: the app (lesson player), YouTube (the video version) and the curriculum docs (the canonical text).

### Program map (proposed, pending curriculum review)

| Term | Title | Focus |
| --- | --- | --- |
| 1 | The Body | Anatomy, physiology, energy systems, movement vocabulary |
| 2 | Movement | Exercise technique, applied biomechanics, dos and don'ts with reasons |
| 3 | Adaptation | Training principles, programming, progression, recovery |
| 4 | Nutrition | Energy balance, macros, Indian diets, supplements |
| 5 | Evidence | Reading research as a layperson, judging claims |
| 6 | Health Literacy and Longevity | Body composition, visceral fat, lifestyle disease, preventive tests, ageing |

Term 1 is detailed in [Term 1 — The Body](curriculum/term-01-the-body.md). Terms 2–6 are outlines only until approved.

### First interactive lab

The **Lat Pulldown Lab** has start, pull and controlled-return states; front and posterior views; toggleable primary movers, contributors and stabilisers; explanations of joint actions and the movement path; a slider; source notes; and a quiz. It is an educational movement map, not an EMG display. Never invent activation percentages.

## 6. Product

### Surfaces

- **YouTube:** lessons as videos. This is the audience-building and validation channel.
- **Web app (first):** the lesson player, labs, evidence cards, and personal and family use.
- **Mobile app (later, paid):** training and logging on the go, lessons, and the assistant. The mobile technology choice is open (see [DECISIONS.md](DECISIONS.md)).

### Initial feature scope

- Personal dashboard
- Lesson player
- Workout planner and set-by-set log
- Exercise library
- Recovery check-in
- Evidence-card library
- Manual nutrition and meal logging
- Body measurements
- *Later:* a built-in assistant that answers from Fit360 content, within the safety policy

Workout recommendations start as transparent, editable rules, not open-ended AI. They always show their rationale and safety limits.

## 7. Business

Fit360 will charge for app access once the content and the free YouTube audience have shown what people value. Audience, pricing, payments and legal obligations are covered in the [business model](business/business-model.md).

## 8. Technical direction

- Next.js, React, TypeScript, Tailwind CSS and shadcn/ui for the web
- Supabase (PostgreSQL, Auth, Row-Level Security, Storage) as the initial backend
- YouTube for video hosting
- React Hook Form, Zod and Recharts
- Interactive SVG, Canvas or WebGL only where justified
- Mobile: to be decided. A shared TypeScript codebase is preferred.
- AI assistant: provider to be decided, with answers grounded in Fit360's own curriculum and sources

Use original or licensed visual assets. Do not treat AI calorie estimates as truth.

### Core data shape

- `profiles` (with a consent record)
- `courses`, `modules`, `chapters`, `lessons`, `sources`, `learner_progress`
- `exercises`, `programs`, `program_sessions`, `workout_logs`, `workout_sets`
- `daily_checkins`, `body_measurements`
- `foods`, `meals`, `meal_items`
- `evidence_cards`, `citations`
- *Later:* `subscriptions`, `assistant_conversations`

Each user's private records must be isolated from every other user's, and Supabase RLS tests must prove it. Health-related personal data is handled under the rules in the [business model](business/business-model.md#legal-and-data-obligations).

## 9. Engineering and delivery

The environments are local development and production. Pull-request previews may be added later, with synthetic data only. The workflow is Jira → branch → PR → review → squash merge, with TDD. Details are in the [delivery lifecycle](engineering/delivery-lifecycle.md).

## 10. Current priority

1. Approve the Term 1 curriculum and the first vertical lesson slice (one full lesson, plus the Lat Pulldown Lab, in the app and as a video).
2. Keep publishing lessons on YouTube to learn what the audience values.
3. Build the web app for personal and family use before any paid launch.

Do not build broad app features until the course architecture and the first vertical lesson slice are approved.
