# Architecture Overview

This project is a full‑stack job application tracker built with Next.js. 
It allows users to auth., add/remove and track job applications, receive 
follow‑up reminders, store their CV for later use, and export or import their data. The application 
uses a SQL database for persistent storage and exposes API routes for 
CRUD operations.

## Tech Stack

- **Frontend:** Next.js (App Router), React, Tailwind CSS
- **Backend:** Next.js API Routes
- **Database:** PostgreSQL
- **ORM:** Prisma
- **Authentication:** NextAuth.js (OAuth)
- **Deployment:** Vercel (frontend + backend), Railway/Supabase (database)
- **Testing:** Jest or Vitest (unit tests), Playwright (integration tests)

## High-level architecture:

The application follows a modern full-stack architecture using Next.js:

- The **frontend** renders UI components using React and Tailwind CSS.
- The **backend** is implemented using Next.js API Routes, which handle 
  authentication, CRUD operations, and reminder logic.
- The **database** stores users and job applications using PostgreSQL.
- **Prisma** acts as the ORM layer between the backend and the database.
- **NextAuth** manages user sessions and authentication using OAuth providers (e.g., Google).
- The application is deployed on Vercel, with the database hosted on 
  Railway or Supabase (remains to be decided).

Data flows from the client to the API routes, which validate and process 
requests before interacting with the database. Responses are returned to 
the client to update the UI.

## Database tables:

### User
- id (PK)
- name - user's name
- email - email Adress
- emailVerified - timestamp for email verification
- image - profile picture URL
- createdAt - timestamp of user creation

### Account (NextAuth)
- id (PK)
- userId (FK -> User)
- provider - e.g. Google
- providerAccountId - ID from the provider
- access_token, refresh_token, expires_at, etc

### Session (NextAuth)
- id (PK)
- sessionToken
- userId (FK -> User)
- expires - session expiration timestamp

### Application
- id (PK)
- userId (FK -> User)
- company
- position
- status
- dateApplied
- lastUpdate
- notes
- createdAt
- updatedAt

## API Routes

The API routes will be defined once the CRUD structure is implemented.
Planned routes include:

- /api/applications (GET, POST)
- /api/applications/:id (GET, PUT, DELETE)
- /api/auth/[...nextauth] (NextAuth)
