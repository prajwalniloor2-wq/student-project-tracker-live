# Student Project Tracker — Cloud Variant

A hands-on web app development project using Vercel for hosting and Supabase PostgreSQL for data storage. The browser sends requests to an Express API, which reads and changes project records.

## Run locally

Use Node.js 22.x. In PowerShell, from this folder, run:

```powershell
npm.cmd ci
```

Copy `.env.example` to `.env` and put your own Supabase Transaction pooler connection string in `DATABASE_URL`. Keep `.env` private and never commit it.

Run `schema.sql` in the Supabase SQL Editor to create the projects table. Then start the app:

```powershell
npm.cmd start
```

Open http://localhost:3000.

## Data and configuration

`DATABASE_URL` is server-only configuration. Each person running or deploying this app must provide their own database connection string.

This demo has no sign-in; visitors share its project records. Use synthetic data. Local SQLite records are not migrated to Supabase.

## Deployment

Production URL: https://student-project-tracker-live-sooty.vercel.app/

## Verification

- The Supabase schema was created successfully.
- The production homepage and `/api/health` returned successfully.
- Hosted API create, list, update, and delete were verified; the temporary verification record was removed.
- The learner confirmed the hosted UI workflow and access from a phone.
- Vercel deployments run from the connected GitHub repository; Supabase stores hosted records separately from source.
