# SkillProbe — Assessment Platform

A complete MCQ-based assessment platform for 7 technical domains with Admin Dashboard.

## 📁 Project Structure

```
skillprobe/
├── index.html          ← Main HTML file (open this in browser)
├── css/
│   └── style.css       ← All styles
└── js/
    ├── questions.js    ← Question bank (350 questions, 50 per domain)
    └── app.js          ← Platform logic (quiz engine, admin, timer)
```

## 🚀 How to Run Locally

Just open `index.html` in any modern browser — no server needed!

## 🔐 Login Credentials

| Role    | Username | Password   |
|---------|----------|------------|
| Admin   | admin    | admin123   |
| Trainee | (any)    | (any name + domain + ID) |

## 🌐 FREE Hosting Options

### Option 1: GitHub Pages (Recommended — Easiest)
1. Create a free account at https://github.com
2. Click "New Repository" → name it `skillprobe` → set to **Public**
3. Upload all files maintaining the folder structure:
   - `index.html` at root
   - `css/style.css`
   - `js/questions.js`
   - `js/app.js`
4. Go to **Settings → Pages → Source** → select `main` branch → Save
5. Your site will be live at: `https://YOUR-USERNAME.github.io/skillprobe`

### Option 2: Netlify (Drag & Drop — 30 seconds)
1. Go to https://netlify.com → Sign up free
2. On dashboard, drag and drop the entire `skillprobe/` folder
3. Netlify auto-deploys instantly
4. You get a URL like: `https://amazing-name-123.netlify.app`
5. Optional: Go to **Site Settings → Domain** to set a custom name

### Option 3: Vercel
1. Go to https://vercel.com → Sign up with GitHub
2. Import your GitHub repository (from Option 1)
3. Click Deploy — done!
4. URL: `https://skillprobe.vercel.app`

### Option 4: Cloudflare Pages (Best Performance)
1. Go to https://pages.cloudflare.com
2. Connect GitHub repo
3. Build command: (leave empty)
4. Output directory: `/`
5. Deploy!

## 📊 Features

- **7 Domains**: Data Engineering, QA, BA, DevOps, MERN, PHP, Python
- **350 Questions**: 50 per domain, all difficult/tricky
- **30-minute timer** with auto-submit
- **Question Navigator** panel — jump to any question
- **Mark for Review** — flag questions to revisit
- **Keyboard shortcuts**: Arrow keys to navigate, 1/2/3/4 or A/B/C/D to answer, M to mark
- **Admin Dashboard**: Live stats, all results, domain analytics
- **Search & Filter**: Filter results by domain, name, pass/fail
- **Persistent Storage**: Results saved in browser localStorage

## ⚠️ Note on Data Persistence

Results are stored in browser `localStorage`. This means:
- Admin on the same browser/device sees all results
- Data clears if browser cache is cleared
- For production use with a backend DB, integrate Firebase or Supabase (both free tiers available)

## 🔧 Customization

**Change admin password**: Edit `app.js` line with `u === 'admin' && p === 'admin123'`

**Add questions**: Edit `js/questions.js` and add to the appropriate domain array

**Change timer**: Edit `state.timeLeft = 1800` in `app.js` (value is in seconds)

**Change question count**: Edit `.slice(0, 50)` in `startQuiz()` in `app.js`
