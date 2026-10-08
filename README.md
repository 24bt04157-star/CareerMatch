# CareerMatch — React + Node.js/Express + PostgreSQL

This is the React/backend/database rebuild of the original CareerMatch HTML prototype. The UI direction and demo flow are preserved; the data layer is now API + PostgreSQL ready.

## Stack
- Frontend: React + Vite
- Backend: Node.js + Express
- Database: PostgreSQL
- Matching: transparent deterministic scoring (no AI dependency required for the MVP)

## Run locally
1. Install PostgreSQL and create a database named `careermatch`.
2. Run `database/schema.sql`, then `database/seed.sql`.
3. Copy `server/.env.example` to `server/.env` and update `DATABASE_URL`.
4. From this folder run `npm install`, `npm run install:all`, then `npm run dev`.
5. Open http://localhost:5173

Demo accounts are selected from the landing page; the hackathon prototype does not require passwords.

## Vercel / deployment
The frontend can be deployed to Vercel, but PostgreSQL must be hosted separately (for example a managed PostgreSQL provider). Set `VITE_API_URL` to the deployed API URL and configure `DATABASE_URL` on the backend host. Do not put database credentials in the frontend.

## PS2 alignment
The official PS2 MVS asks for profile creation, skills with proficiency, career selection, career-specific requirements, comparison, skill gaps and a readiness score. CareerMatch implements those core concepts and extends them with structured recruiter opportunity matching, location, mode, duration, availability and applications.
