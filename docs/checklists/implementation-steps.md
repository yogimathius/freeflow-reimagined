# Implementation Steps (Prioritized)

1) Data/API enhancements
- [ ] Add pagination and simple search filters to GraphQL queries (args + prisma)
- [ ] Wire `AchievementsEngineService` into Posts, Messages, Experiences services
- [ ] Ensure XP increments on experience confirmation and other triggers
- [ ] Optional: add Notifications model + queries (achievement unlocked, message received)

2) Frontend UX completeness
- [ ] Feed: implement Create Post form (modal) using `CREATE_POST`
- [ ] Profile: replace mocks by querying achievements (`userAchievements`) and experiences (`userExperienceHistory`)
- [ ] Skills: ensure add-user-skill uses real skill IDs; add endorsement action
- [ ] Messages: mark-as-read on view; add basic polling or subscription
- [ ] Connect: batch load user skills to reduce N+1, or expose composite query
- [ ] Achievement popups triggered after successful mutations

3) Search & filtering
- [ ] Add search inputs on feed/users; call new backend filters
- [ ] Filter posts by postSkills

4) Reliability and polish
- [ ] Standardize error toasts + empty states
- [ ] Token propagation: confirm Apollo header always has token; remove redundant localStorage usage if possible
- [ ] CI: lint/build/test; ensure seed script runs in CI (backend)
- [ ] Docs: env examples, setup, run, seed, codegen

