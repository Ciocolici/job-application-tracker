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
- **Authentication:** NextAuth.js
- **Deployment:** Vercel (frontend + backend), Railway/Supabase (database)
- **Testing:** Jest or Vitest (unit tests), Playwright (integration tests)

## High-level architecture:

The application follows a modern full-stack architecture using Next.js:

- The **frontend** renders UI components using React and Tailwind CSS.
- The **backend** is implemented using Next.js API Routes, which handle 
  authentication, CRUD operations, and reminder logic.
- The **database** stores users and job applications using PostgreSQL.
- **Prisma** acts as the ORM layer between the backend and the database.
- **NextAuth** manages user sessions and authentication.
- The application is deployed on Vercel, with the database hosted on 
  Railway or Supabase (remains to be decided).

Data flows from the client to the API routes, which validate and process 
requests before interacting with the database. Responses are returned to 
the client to update the UI.

## Database tables:






API Routes: