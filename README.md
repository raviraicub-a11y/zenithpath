# Zenithpath CRM

Premium light-theme lead CRM built for Zenithpath.

## What is included

- Lead command center dashboard
- Add / edit lead
- Soft delete to Trash + Restore
- Call and WhatsApp quick actions
- Activity timeline for calls, WhatsApp, notes and status changes
- Follow-up manager
- Overdue + next-24-hour notifications
- Search and pipeline filters
- Priority and status tracking
- Lead assignment
- Qualification + document fields
- CSV export
- PostgreSQL + Prisma backend
- Vercel-friendly Next.js App Router

## 1. Local setup

```bash
npm install
cp .env.example .env
# Put your PostgreSQL DATABASE_URL in .env
npx prisma db push
npm run db:seed
npm run dev
```

Open http://localhost:3000.

## 2. GitHub

```bash
git init
git add .
git commit -m "Build Zenithpath CRM"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/zenithpath-crm.git
git push -u origin main
```

## 3. Vercel

1. Import the GitHub repository into Vercel.
2. Add `DATABASE_URL` in Vercel Project Settings → Environment Variables.
3. Deploy.
4. Redeploy after changing environment variables.

## Database

This project uses PostgreSQL through Prisma. You can use a managed PostgreSQL provider and put its connection string into `DATABASE_URL`.

## Important

The supplied HTML was used as the starting data model: it contained 27 example leads and fields such as Facebook/Instagram source, campaign, phone/WhatsApp, location, documents, call status, feedback, budget, occupation, house/roof type, follow-up and assignee. The new schema expands those concepts and moves the data into PostgreSQL.

For a real production launch, add authentication/role permissions before exposing the CRM publicly.
