# START Employability Score Platform

A career-readiness product for web and mobile. Learners take assessments for the job they want, get an Employability Score, and use AI career tools to close their gaps. Colleges and training providers get their own branded portal and an admin dashboard.

- Product pages: [Assessments and Employability Score](https://startnew.ca/platform/assessments-employability-score), [START Coach](https://startnew.ca/platform/start-coach), [For institutions](https://startnew.ca/institutions)
- Company: StartNew Technologies
- Source: private repository

All screens below come from the public product films and show a demo account.

## The problem

A learner preparing for a job rarely knows how far they are from being ready for it, or what to work on first. A college has the same question about a whole cohort. The platform answers both with one set of role-based assessments.

## My role

I lead the product: priorities, requirements, user journeys and UX for learners, institutions and administrators. I direct its development with AI coding agents across web, mobile and backend, review architecture and data-flow choices, and check the result against the acceptance criteria. The method is described in [how-i-work](https://github.com/gokselkacar/how-i-work).

I also directed the AI-assisted curation of the assessment content, more than 10,000 questions, including quality checks, cleaning and integration testing.

## Learner experience on the web

| Career dashboard | Career pulse | Practice question |
| --- | --- | --- |
| ![Career dashboard with role match and scores](../assets/screenshots/start-employability-score-application/01-web-career-dashboard.webp) | ![Career pulse for the best-matched role](../assets/screenshots/start-employability-score-application/02-web-career-pulse.webp) | ![A timed practice question](../assets/screenshots/start-employability-score-application/03-web-practice-question.webp) |

| Practice result | Weekly action board | Career tools |
| --- | --- | --- |
| ![Practice result with score and feedback](../assets/screenshots/start-employability-score-application/04-web-practice-result.webp) | ![Weekly action board with three tasks](../assets/screenshots/start-employability-score-application/05-web-weekly-action-board.webp) | ![Career tools menu](../assets/screenshots/start-employability-score-application/06-web-career-tools.webp) |

## START Coach, the AI career tools

| Coach chat | Interview Simulator |
| --- | --- |
| ![START Coach chat giving a four-week plan](../assets/screenshots/start-employability-score-application/07-web-coach-chat.webp) | ![Interview Simulator feedback on an answer](../assets/screenshots/start-employability-score-application/08-web-interview-simulator.webp) |

| Resume Optimizer | Role Matcher |
| --- | --- |
| ![Resume Optimizer with an ATS score and priority fixes](../assets/screenshots/start-employability-score-application/09-web-resume-optimizer.webp) | ![Role Matcher ranking best-fit roles](../assets/screenshots/start-employability-score-application/10-web-role-matcher.webp) |

## Institution portal

| Branded sign-in | Assessment analytics | Role readiness |
| --- | --- | --- |
| ![Sign-in page branded for a demo college](../assets/screenshots/start-employability-score-application/11-institution-portal.webp) | ![Admin view of scores and completions](../assets/screenshots/start-employability-score-application/12-institution-assessments.webp) | ![Admin view of role readiness and skill gaps](../assets/screenshots/start-employability-score-application/13-institution-readiness.webp) |

## Mobile app

| Home | Explore roles | Choose a level | Question | Result | Action board |
| --- | --- | --- | --- | --- | --- |
| <img src="../assets/screenshots/start-employability-score-application/14-mobile-home.webp" alt="Mobile home screen" width="150"> | <img src="../assets/screenshots/start-employability-score-application/15-mobile-explore-roles.webp" alt="Mobile role explorer" width="150"> | <img src="../assets/screenshots/start-employability-score-application/16-mobile-select-level.webp" alt="Mobile level picker" width="150"> | <img src="../assets/screenshots/start-employability-score-application/17-mobile-question.webp" alt="Mobile practice question" width="150"> | <img src="../assets/screenshots/start-employability-score-application/18-mobile-result.webp" alt="Mobile practice result" width="150"> | <img src="../assets/screenshots/start-employability-score-application/19-mobile-action-board.webp" alt="Mobile weekly action board" width="150"> |

## What it does

- **Role-based assessments.** A learner picks a job title, sees the skill areas it needs, and practises each one at junior, intermediate or expert level, or takes a level assessment.
- **Employability Score.** Results roll up into a score for the target role, with strengths, gaps and the next thing to practise.
- **START Coach.** Coach chat, Role Matcher, Resume Optimizer, Interview Simulator and a growth roadmap, all working from the learner's own results and profile.
- **Institution portal.** A college gets a sign-in page with its own name and look, and staff follow cohort progress, role readiness and skill gaps, and export reports.
- **Same product on both platforms.** The mobile app and the web app share the backend, the assessment content and the scoring.

## How it is built

React Native with Expo for mobile, Next.js for web, and a shared TypeScript monorepo. The backend is a GraphQL API on AWS with serverless functions and PostgreSQL, defined as infrastructure code.

```mermaid
flowchart TD
    U[Learners and institution staff] --> M[Mobile app]
    U --> W[Web app]
    M --> G[GraphQL API]
    W --> G
    G --> A[Authentication]
    G --> F[Serverless functions]
    F --> D[(PostgreSQL)]
    F --> S[File storage]
    F --> L[LLM services for coaching tools]
```

Mobile and web share one backend so an assessment behaves the same on both, and a learner can start on the phone and finish on the web.

## Repository note

The source code is in a private repository. This page is a public summary.
