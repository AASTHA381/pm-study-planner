# 🎯 PM Study Planner

A personal daily planner built to track PM (Product Manager) study progress — with a flexible task system, progress grids, streaks, history, and installable as an app on iPhone/Android.

---

## 📱 What It Does

This is a **single-file web app** (no login, no server, no account needed) that helps you:

- Plan your daily PM study tasks **your way** — pick only what you have time for
- Track long-term progress across Cohere, HelloPM, Learn Prompting, and The Noob PM
- Build daily streaks for both PM study and personal tasks
- Review your history with a 14-day card view and monthly heatmap
- Get carry-over reminders for tasks you missed

All data is saved locally in your browser — works offline, no account needed.

---

## 📋 Tabs Overview

### 📋 Today

The main daily planning tab. Divided into 3 sections:

#### 📦 All Tasks — Pick What to Do Today
A full list of available tasks you can add to today's plan:

| Task | Description |
|------|-------------|
| 💡 Case Study Question | Solve 1 PM case study question |
| 📖 Cohere Docs | Study a section of Cohere documentation |
| 🛠️ Build a Simple App | Build something using Cohere API |
| 🎥 HelloPM Video | Watch a video from the HelloPM YouTube channel |
| 🤖 Learn Prompting | Complete a session of Learn Prompting courses |
| 🏗️ The Noob PM | Complete a day of The Noob PM 45-day program |
| ▶️ PM YouTube Video 1/2/3 | Watch specific PM YouTube videos |

- Tap **＋ Add** to add any task to today's plan
- Once added, the button turns green **✓ Added** and the task appears in Today's Tasks below
- Tap **✕** on a task in Today's Tasks to remove it from today
- Use **✏️ Edit** to permanently remove a task from the library
- Use **➕ Add a Custom Task** to add your own task with a custom name, icon, and link

#### 🔴 Today's Tasks
Shows only the tasks you've added from the list above. Tap any task to check it off. Tasks with carry enabled that you miss will automatically re-appear the next day.

#### 🎓 Personal
Always-present mandatory tasks:

- 🎓 **College Case Article** — Mandatory daily
- 📚 **Novel Chapter** — Mandatory daily
- 📘 **Had 2 lectures today?** — Toggle to add a 2nd College Article for days when you have 2 lectures

---

### 📈 Progress

Long-term progress tracking across three resources:

- **🎥 HelloPM** — 60 videos (clickable grid, mark each video watched)
- **🤖 Learn Prompting** — 16 AI courses (list with direct links to each course)
- **🏗️ The Noob PM** — 45-day build program (clickable grid with day links)

Each has a progress bar and counter.

---

### 📅 History

- **14-day card view** — colour-coded cards for the last 2 weeks (green = all done, yellow = partial, red = barely started)
- **Monthly heatmap** — GitHub-style calendar showing completion intensity for the current and previous month

---

### 🔗 Resources

Quick-access links to all study resources:
- Learn Prompting course library
- The Noob PM 45-day program
- Cohere documentation
- HelloPM YouTube channel
- PM YouTube videos

---

## ✨ Features

- **Flexible daily planning** — add only the tasks you have time for each day
- **Carry-over system** — missed tasks (with carry enabled) auto-appear the next day
- **PM Streak & Personal Streak** — tracks consecutive days of study
- **Custom tasks** — add your own task with a custom icon, name, link, and carry setting
- **2nd College Article toggle** — optional extra task for days with 2 lectures
- **Toast notifications** — quick confirmation when you tick or untick a task
- **Responsive design** — works on mobile, tablet, and desktop
- **PWA installable** — add to home screen on iPhone or Android (works offline)

---

## 📲 Install as an App (PWA)

### iPhone (Safari)
1. Open the site in **Safari**
2. Tap the **Share** button (box with arrow at the bottom)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add** — it now appears as an app icon on your home screen

### Android (Chrome)
1. Open the site in **Chrome**
2. Tap the **three-dot menu** → **Add to Home Screen**
3. Tap **Add**

---

## 🗂️ File Structure

```
pm-tracker.html       ← Main app (everything in one file)
manifest.json         ← PWA manifest for installability
sw.js                 ← Service worker for offline support
icon-192.png          ← App icon (192×192)
icon-512.png          ← App icon (512×512)
apple-touch-icon.png  ← iPhone home screen icon
```

---

## 🚀 How to Use Locally

1. Download or clone this repo
2. Open `pm-tracker.html` in any browser
3. No build step, no dependencies, no install needed

---

## 🔒 Privacy

- **All data stays in your browser** (`localStorage`)
- Nothing is sent to any server
- Clearing browser data / site data will reset the app

---

## 🛠️ Tech Stack

- Pure HTML + CSS + JavaScript (no frameworks)
- Browser `localStorage` for persistence
- PWA: Web App Manifest + Service Worker
- No build tools, no npm, no dependencies

---

## 📚 Study Resources Tracked

| Resource | What It Is | Progress |
|----------|-----------|----------|
| [HelloPM](https://www.youtube.com/@hellopm) | PM YouTube channel — watch oldest first | 60 videos |
| [Learn Prompting](https://learnprompting.thinkific.com/collections) | AI & Prompt Engineering course library | 16 courses |
| [The Noob PM](https://www.thenoobpm.com/#/dashboard) | 45-day PM build program | 45 days |
| [Cohere Docs](https://docs.cohere.com/docs/build-things-with-cohere) | Build things with Cohere AI | Daily reading |

---

*Built for personal use — no auth, no backend, just consistency.*
