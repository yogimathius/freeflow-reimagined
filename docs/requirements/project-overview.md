# Freeflow Reimagined — Project Overview

A social platform for professionals to connect, share skills, and collaborate, built with a Next.js 15 frontend and a NestJS GraphQL backend using Prisma/PostgreSQL.

## High-level Architecture
- Frontend: Next.js (App Router), Tailwind, shadcn/ui, Apollo Client, NextAuth
- Backend: NestJS (GraphQL Apollo), Prisma, JWT auth
- DB: PostgreSQL via Prisma schema

## Core Domains
- Users, Auth, Profiles
- Posts, Comments, Likes, PostSkills
- Skills, SkillCategories, UserSkills, Endorsements
- Experiences (requests between users) with XP award flow
- Messaging (DMs)
- Achievements (unlockable, with engine service)
- Progress/XP (UserProgress, UserSkillProgress)

## Primary User Journeys
- Register/Login
- View feed, open post, comment/like, tag skills
- Manage skills, view other users, request experiences
- Message other users
- View profile with achievements and experience timeline

