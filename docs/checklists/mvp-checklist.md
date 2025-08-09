# MVP Delivery Checklist

## Product Readiness
- [ ] Define MVP scope and success metrics
- [ ] Provision environments: dev, staging (optional), prod
- [ ] Create .env templates for frontend/backend

## Backend (GraphQL API)
- [ ] Verify auth guards on sensitive mutations (posts/comments/messages/experiences)
- [ ] Add pagination to list queries: `posts`, `users`, `messages`, `experiences`
- [ ] Add basic search filters (users by name, posts by title/body, skills by name)
- [ ] Finish achievements wiring: invoke `AchievementsEngineService` on:
  - [ ] post create (FIRST_POST_CREATED)
  - [ ] message create (FIRST_MESSAGE_SENT)
  - [ ] experience create/confirm (FIRST_EXPERIENCE_ADDED)
  - [ ] milestones (counts) for comments/likes/posts/skills
- [ ] Ensure XP awarding toggles `xpAwarded` and increments `UserProgress`
- [ ] Add notifications model + resolvers for achievements/level-up (optional for MVP)
- [ ] Add rate limiting (e.g., per-IP for auth and posts) (optional)
- [ ] Add consistent error shapes and input validation coverage (class-validator)
- [ ] Seed data completeness (skills, categories, demo users/posts)
- [ ] Unit tests green (services/resolvers), run coverage

## Frontend (App)
- [ ] Global auth state reliability (NextAuth session <-> Apollo header)
- [ ] Feed: create post UI (modal/form) with mutation + optimistic update
- [ ] Post detail: comment composer + live refresh after submit
- [ ] Skills: replace placeholders; ensure add skill path uses real IDs
- [ ] Profile: remove mock data, render from GraphQL (skills, achievements, experiences)
- [ ] Connect: ensure skills-by-user loads in batch or via query composition; empty states
- [ ] Inbox/Experiences: confirm flows work and badge counts update after actions
- [ ] Messages: mark-as-read on view; scroll-to-bottom; empty and loading states
- [ ] Achievement popups: trigger from mutations (post/comment/experience/message)
- [ ] Error boundaries and toasts standardized
- [ ] Basic search UI (users/posts/skills) calling new backend filters
- [ ] Pagination or infinite scroll on feed and conversations

## DevEx/Quality
- [ ] ESLint/Prettier pass in frontend and backend
- [ ] Type generation up-to-date: `npm run codegen` (frontend)
- [ ] Environment variables documented
- [ ] README updates (run, test, seed, env)
- [ ] Basic CI: lint + build + test on push (optional)

## Deployment
- [ ] Backend deployed (Docker or Node), DB provisioned (Postgres)
- [ ] Frontend deployed (Vercel or Node)
- [ ] CORS and URLs configured (`NEXT_PUBLIC_GRAPHQL_URI`, backend CORS)
- [ ] Health checks and basic logs

