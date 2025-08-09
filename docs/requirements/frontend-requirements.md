# Frontend Requirements (Observed)

## Tech/Infra
- Next.js 15 (App Router), React 19, Tailwind, shadcn/ui
- Apollo Client for GraphQL
- NextAuth Credentials provider (calls backend GraphQL login)
- Auth-aware middleware gating protected routes

## Implemented Pages
- `/` feed with posts list and detail at `/feed/[postId]`
- `/login`, `/register` (NextAuth integrated)
- `/skills` manage user skills (optimistic UI, uses GraphQL queries)
- `/messages` conversational UI (GraphQL-backed)
- `/inbox` + `/inbox/experiences` summary and management of experiences
- `/connect` browse users, filter by skill category, request experiences
- `/profile` profile view with achievements section and experience timeline (some mock data placeholders)
- `/users` simple users list page

## Key Components/Hooks
- Experience flow (request/confirm) components and hooks
- Post detail interactions (like, comment, post skills chips)
- Apollo client with multi-source token strategy, error link handling
- Middleware to enforce auth on selected routes

## Missing/To Verify
- Unified error/loading states across pages
- Real-time updates (messages, inbox badges)
- Full profile edit form
- Achievement rendering fed entirely by backend (currently partly mocked)
- Create post UX (button exists; mutation wired but UI incomplete)
- Search and filtering across feed/users/skills
- Pagination/infinite scroll patterns beyond basic slicing

