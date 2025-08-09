# Backend Requirements (Observed)

## Tech/Infra
- NestJS 11 with Apollo GraphQL, schema-first via code-first (autoSchemaFile)
- Prisma with PostgreSQL; seeds for users, posts, skill categories, skills
- JWT-based auth; `AuthModule`, `JwtStrategy`, guards
- CORS configured in `main.ts` for local dev

## Modules (from `AppModule`)
- `Users`, `Auth`, `Posts`, `Comments`, `Likes`, `Messages`
- `Skills`, `SkillCategories`, `UserSkills`, `PostSkills`
- `Experiences`
- `Achievements` (+ `AchievementsEngineService`)
- `UserProgress` (XP/levels, plus per-skill progress)
- `Common` (plugins, logging, http logger middleware)
- `Prisma`

## GraphQL Surface (from `src/schema.gql`)
- Queries: users, me, posts, postSkill(s), skills, categories, likes, comments, experiences, achievements, various user-centric queries (my*, byUser, byPost)
- Mutations: register/login, CRUD for post/comment/skill/category/user skills, like toggle, messaging (send/mark read), experiences (create/update/confirm), achievements unlock, post-skill add/remove

## Data Model (from `prisma/schema.prisma`)
- Users with relations to posts/comments/likes/messages/skills/achievements/progress
- Posts with comments/likes/postSkills
- Skills with categories, userSkills, postSkills, experiences
- Experiences with requester/responder, type, confirmations, xp flags
- Messages with isRead
- Achievements and UserAchievement (unique per user/achievement)
- Progress: `UserProgress` and `UserSkillProgress`

## Implemented Services/Resolvers (glance)
- Services/resolvers exist for all listed modules above; tests exist per service
- `AchievementsEngineService` implemented and exported

## Missing/To Verify
- WebSocket/subscriptions for real-time (messages, notifications)
- Rate limiting, input validation depth, error normalization
- Admin roles/guards for admin-only mutations
- Search endpoints (users/posts/skills)
- Pagination patterns on list queries
- File upload handling beyond avatarUrl (none visible)
- Notifications model/resolvers (not present)

