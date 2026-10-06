# Tryengl project context

Read this file before making architectural, content, deployment or product decisions for Tryengl.

## What this project is

Tryengl is an interactive English-learning site focused on FCE preparation. The current lesson teaches paraphrasing, passive voice and Reading and Use of English practice.

## Live links

- GitHub repository: <https://github.com/m-bayrak/tryengl>
- GitHub Pages: <https://m-bayrak.github.io/tryengl/>
- Netlify: <https://tryengl.netlify.app/>

## Current implementation

- The site is a static interactive worksheet.
- Exercises include at least ten items where applicable.
- Passive-voice activities are clickable and give feedback.
- Incorrect answers can offer grammar or vocabulary explanations.
- Passive formulas cover the main required forms, including future passive and past perfect passive.
- The existing worksheet is the reference for future redesign work; preserve it while creating new learner experiences.

## Product decisions

- The learner experience should become focused and minimalist: one goal, activity and decision at a time rather than a long page of text.
- Future lessons should support modes or stages such as Intro, Discover, Build, Practice, FCE Challenge and Review.
- A learner-facing lesson catalogue will live at `/library`.
- A developer-only component and lesson workspace will live at `/dev` and must not be in normal learner navigation.
- New lesson content should eventually be separate structured data, not copied HTML pages.

## Development and deployment

- Keep `main` stable and deployable.
- Use a dedicated feature branch for substantial work, then merge only after review.
- GitHub Pages and Netlify both deploy the current public site.
- Do not commit secrets, access tokens or local machine files.

## Working in a new Cloud chat

1. Choose the `m-bayrak/tryengl` environment.
2. Read this file and `docs/ROADMAP.md` before changing structure or UX.
3. Inspect the existing implementation before replacing it.
4. Summarize material decisions here after they are committed.

## Next priorities

See [ROADMAP.md](ROADMAP.md) for the agreed implementation order.
