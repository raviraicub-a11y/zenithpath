# Zenithpath CRM — GitHub + Vercel deployment

### A. Create database
Create a managed PostgreSQL database and copy its connection string.

### B. Push to GitHub
```bash
git init
git add .
git commit -m "Zenithpath CRM v1"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/zenithpath-crm.git
git push -u origin main
```

### C. Deploy Vercel
Import the repository at Vercel. Add:
- `DATABASE_URL`
- `NEXT_PUBLIC_APP_NAME=Zenithpath CRM`
- `NEXT_PUBLIC_APP_URL=https://your-domain.vercel.app`

Build command: `npm run build`

### D. Initialize database
From a machine with the production DATABASE_URL:
```bash
npx prisma db push
npm run db:seed
```

### E. Custom domain
After deployment, attach your Zenithpath subdomain/domain from Vercel Project → Domains.

### Production security
Before sharing the public URL, add login + role-based access (Admin / Manager / Sales), audit permissions, rate limiting, and a backup policy.
