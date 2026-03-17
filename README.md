# AI Analytics Platform

Full-stack SaaS app for uploading, managing, and visualizing CSV/JSON datasets with interactive charts.

## Prerequisites

- Node.js 18+
- PostgreSQL 14+

## Database setup

1. Create database:

```bash
createdb analytics_db
```

2. Run schema:

```bash
psql -d analytics_db -f backend/schema.sql
```

## Backend setup

```bash
cd backend
npm install
cp .env.example .env
```

Edit `backend/.env`:

- `DATABASE_URL=postgresql://user:password@localhost:5432/analytics_db`
- `JWT_SECRET=your_secret_key`

Start backend:

```bash
node src/app.js
```

Backend runs on `http://localhost:5000`.

## Frontend setup

```bash
cd frontend
npm install
cp .env.local.example .env.local
```

Ensure `frontend/.env.local` contains:

```
NEXT_PUBLIC_API_URL=http://localhost:5000
```

Start frontend:

```bash
npm run dev
```

Frontend runs on `http://localhost:3000`.

