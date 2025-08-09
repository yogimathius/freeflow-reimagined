# Feature Parity Checklist (Code vs Intended)

## Auth
- [x] Register and login (NextAuth + GraphQL)
- [ ] Forgot/reset password flow
- [x] Route protection via middleware

## Users & Profiles
- [x] User list page
- [ ] Profile edit form (name/bio/avatar)
- [ ] Achievements fully rendered from API (no mocks)
- [ ] Progress (XP/level) shown on profile

## Posts
- [x] Posts list (feed)
- [x] Post detail page with comments and likes
- [ ] Create post UI wired to mutation
- [ ] Tag skills on create/edit; list filtering by skills
- [ ] Search posts

## Skills
- [x] View/Add user skills (basic)
- [ ] Endorse skill interaction
- [ ] Filter skills by category in UI comprehensively

## Experiences
- [x] Request experience modal and flows
- [x] Inbox with incoming/outgoing and confirm flow
- [ ] Real-time or polling refresh upon confirm
- [ ] XP award visualization on completion

## Messages
- [x] Conversations list and thread view
- [ ] Mark-as-read on scroll/visibility
- [ ] Real-time updates (subscriptions/websocket) or polling
- [ ] Unread counts in header/badges

## Achievements & Progress
- [x] Engine service exists on backend
- [ ] Hooked into mutations/events (post, message, experience, milestones)
- [ ] Toast/inline popups when unlocked
- [ ] Profile/dashboard surfaces progress and badges

## Search & Discovery
- [ ] Users: by name and skill category
- [ ] Posts: by text and skills
- [ ] Skills: by name

## Quality
- [ ] Pagination everywhere lists can grow large
- [ ] Error handling unified
- [ ] Loading states consistent
- [ ] Tests: unit + e2e basics pass
