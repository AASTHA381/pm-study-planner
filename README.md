# 🎯 PM Study Planner

A daily task tracker built to support my journey into Product Management — no frameworks, no backend, no dependencies. Just pure HTML, CSS, and JavaScript, installable as a PWA on your phone.

---

## 📱 Live Demo

> Deploy your own in minutes — see [Deployment](#-deployment) below.

Both PWA and offline mode are fully supported once installed.

---

## ✨ Features

- **Daily Task Tracking** — Check off PM learning tasks each day
- **Smart Carry-Over** — Missed tasks automatically shift to the next day
- **Manage Tasks** — Add custom tasks or delete existing ones directly from the UI — no code editing needed
- **4 Tabs:**
  - 📋 **Today** — Daily tasks, carried-over items, personal tasks
  - 📈 **Progress** — Track courses, videos, and days completed across all resources
  - 📅 **History** — 14-day completion cards + monthly heatmap
  - 🔗 **Resources** — Quick access links to all study materials
- **Streak Tracking** — Separate PM streak and personal streak counters
- **Personal Tasks** — Mandatory daily items (college articles, novel chapter) that never carry over
- **PWA** — Install on iPhone or Android, works fully offline

---

## 📚 Resources Tracked

| Resource | Details |
|----------|---------|
| 🤖 Learn Prompting | 16 courses on AI & prompt engineering |
| 🏗️ The Noob PM | 45-day structured PM curriculum |
| 🎥 HelloPM Channel | 60 YouTube videos |
| 📖 Cohere Docs | AI/LLM documentation study |
| 💡 Case Study Questions | Daily PM case practice |
| 🛠️ App Building | Build one small app per day |
| ▶️ PM YouTube Videos | Curated one-time watch list |

---

## 🗂️ File Structure

```
├── pm-tracker.html          # Main app (single-file, self-contained)
├── manifest.json            # PWA manifest (for installability)
├── sw.js                    # Service Worker (offline support)
├── icon-192.png             # PWA icon 192×192
├── icon-512.png             # PWA icon 512×512
└── apple-touch-icon.png     # iOS home screen icon 180×180
```

---

## 🚀 How to Use Locally

No installation or build step required.

```bash
# Clone the repo
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# Open the app in your browser
open pm-tracker.html
```

Or just double-click `pm-tracker.html` — it opens straight in your browser.

> **Note:** The PWA service worker requires the file to be served over HTTP/HTTPS, not the `file://` protocol. For full PWA + offline features, deploy it (see below).

---

## 📲 Install as iPhone / Android App (PWA)

Both apps are Progressive Web Apps — you can install them on your phone's home screen and use them offline.

**On iPhone (Safari only):**
1. Open the deployed URL in **Safari**
2. Tap the **Share** button (box with arrow)
3. Tap **"Add to Home Screen"**
4. Tap **"Add"**

**On Android (Chrome):**
1. Open the deployed URL in Chrome
2. Tap the **three-dot menu → "Add to Home screen"**

Once installed, the app works **fully offline** — your progress is saved in the device's `localStorage`.

---

## 🌐 Deployment

### Option 1 — Netlify Drop (easiest, no account needed)
1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag the `pwa-deploy.zip` onto the page
3. Get an instant public URL (sign up with Google to make it permanent)

### Option 2 — GitHub Pages
1. Push this repo to GitHub
2. Go to **Settings → Pages → Source: main branch / root**
3. Your app will be live at `https://your-username.github.io/your-repo-name/pm-tracker.html`

### Option 3 — Any static host
Upload the files to Vercel, Cloudflare Pages, Render, or any static hosting service.

---

## 💾 Data & Privacy

- All data is stored **locally in your browser** using `localStorage`
- Nothing is sent to any server — no analytics, no tracking
- Data is **per device** — progress on your laptop won't sync to your phone
- Clearing browser data / app storage will reset progress

---

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| Language | Vanilla HTML, CSS, JavaScript |
| Storage | Browser `localStorage` |
| Offline | Service Worker (Cache API) |
| Installable | Web App Manifest (PWA) |
| Hosting | Static file — works anywhere |
| Dependencies | **None** |

---

## 🎨 Design

- Dark navy theme (`#0b0f2a` background)
- Indigo / cyan accent colors
- Mobile-first, fully responsive
- Smooth animations and toast notifications

---

## 📌 Customizing Tasks

You can add or delete tasks directly from the UI — no code editing needed:

1. Open the **Today** tab in the PM Planner
2. Click **⚙️ Manage Tasks** button (top-right of the PM tasks section)
3. Click **✕** on any task to delete it
4. Click **➕ Add New Task** to create a custom task with your own name, icon, description, and link

Changes are saved permanently to your browser.

---

## 📄 License

MIT — feel free to fork, modify, and use for your own study tracking.

---

*Built with ❤️ to stay consistent on the PM learning journey.*
