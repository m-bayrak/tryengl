# Tryengl roadmap

## First-priority development work

Before redesigning the learner experience, create a structure that supports many lessons and lets development happen without losing the current worksheet as a reference.

1. Preserve the current passive-voice worksheet as the complete reference version in `legacy/`.
2. Create the application foundation: shared layout, navigation, lesson shell, styles and routes.
3. Create a learner-facing lesson library at `/library`.
4. Create a developer-only workspace at `/dev` with:
   - a lesson map showing every stage in a lesson;
   - an exercise gallery for each question type;
   - sample student states, feedback states and explanations;
   - animation previews and feature experiments.
5. Separate lesson content from interface code so new lessons are created from structured lesson data rather than copied HTML pages.

## Product direction

- Learners should see a focused, minimalist flow: one goal, one activity and one decision at a time.
- A lesson should progress through: Intro, Discover, Build, Practice, FCE Challenge and Review.
- `/library` is the catalogue visible to learners and teachers: modules, lessons, status and progress.
- `/dev` is not part of the normal learner navigation. It is the internal development area for building and testing components.
- Keep feedback short at first, with optional deeper grammar and vocabulary explanations.

## Suggested future project layout

```text
src/
  app/          routes, layouts and navigation
  components/   lesson, exercise, feedback and UI components
  lessons/      structured lesson content
  modes/        focus, library, review and exam modes
  dev/          component gallery, lesson map and playground
  styles/       shared design system
legacy/         complete worksheet reference
docs/           project documentation
```

## Development workflow

- Keep `main` stable and deployable.
- Build each feature in a dedicated branch, for example `codex/focus-mode` or `codex/lesson-library`.
- Use Netlify preview deployments to review a new feature before merging it into `main`.
