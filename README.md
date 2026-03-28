# EMB Global · PMS FY 2025-26

Performance Management System — static single-page app deployed on Vercel.

## 🚀 Deploy to Vercel

### Option A — Vercel Dashboard (easiest)
1. Push this folder to a GitHub repo
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your GitHub repo
4. Framework Preset: **Other**
5. Click **Deploy** — done ✅

### Option B — Vercel CLI
```bash
npm i -g vercel
vercel login
vercel --prod
```

## 🗂 Project Structure
```
├── index.html     # Full PMS application (self-contained)
├── data.json      # Seed data: employees, KRA templates, ratings
├── vercel.json    # Vercel routing & cache config
├── package.json   # Project metadata
└── .gitignore
```

## 💻 Run Locally
```bash
npx serve . -p 3000
# Open http://localhost:3000
```

## 🔐 Roles
| Role       | Access                                              |
|------------|-----------------------------------------------------|
| Employee   | Fill KRAs, self-rate, submit for manager review     |
| HRBP       | Full edit — review all KRAs, set targets, lock, analytics |
| Management | Read-only executive view — stats, dept drill-down, leaderboard |

## 📌 Notes
- All performance data is stored in the **browser's localStorage** — no backend required.
- Use the **↓ Export** button in the app to download a JSON snapshot of all data at any time.
- To reset data, clear localStorage for the site (`localStorage.clear()` in browser console).
