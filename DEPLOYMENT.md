# Deployment notes

## Frontend (Vercel)
- Import the `client` folder as the Vercel project root.
- Build command: `npm run build`
- Output directory: `dist`
- Add `VITE_API_URL=https://YOUR-BACKEND-DOMAIN`.

## Backend (Node/Express)
Deploy the `server` folder to a Node host such as Render, Railway, Fly.io or another Express-compatible service.
Set `PORT` and `DATABASE_URL` there.

## PostgreSQL
Use a managed PostgreSQL instance. Run `database/schema.sql` followed by `database/seed.sql` once.

## Important
Never put `DATABASE_URL` in Vercel/frontend environment variables. Only the backend should receive database credentials.
