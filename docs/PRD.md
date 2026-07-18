# PM Study Planner — Product Requirements Document & Case Study

> **Study PM your way, and actually stick to it.** A personal daily planner with a flexible task system, progress grids, streaks and history — installable as an app.

| | |
|---|---|
| **Live app** | https://aastha381.github.io/pm-study-planner/ |
| **Repository** | https://github.com/AASTHA381/pm-study-planner |
| **Author** | Aastha Saini |
| **Status** | Shipped (PWA) |
| **Type** | 0→1 consumer productivity (habit / learning) |
| **Doc version** | 1.0 |

---

## 1. TL;DR (Loom-style walkthrough script)

> *This is the PM Study Planner — I built it for myself while learning product management, but it generalises to any self-directed study.*
>
> *The problem with self-study is consistency: courses are scattered across YouTube, Cohere, HelloPM, Learn Prompting, and you never know if you're actually making progress. This planner lets me pick only the tasks I have time for today from a library, tracks long-term progress across each course with grids, builds daily streaks for study and personal habits, and shows a 14-day history and monthly heatmap. It even carries over tasks I missed. No login, no server — it just works offline and installs to my phone. It turned "I should study PM" into a visible, daily, gamified habit.*

**Elevator pitch:** *A flexible, gamified daily planner that turns scattered self-study into a streak you keep.*

---

## 2. Problem Statement

Self-directed learning fails on **consistency and visibility** — content is scattered, progress is invisible, and motivation fades without feedback.

**The core problem:**
> Self-learners can't easily plan a realistic daily study set, see long-term progress across sources, or stay motivated — so they start strong and drift.

**Signals:**
- Learning material spread across many platforms.
- No single view of "am I making progress?".
- Motivation drops without streaks/feedback.
- Rigid planners don't fit variable daily time.

**Hypothesis:**
> If learners pick only what fits today, see progress grids + streaks, and get carry-over nudges, they'll study more consistently.

---

## 3. Research

### 3.1 Insights
| # | Insight | Implication |
|---|---------|-------------|
| 1 | Fixed daily plans break on busy days. | **Pick-what-you-can** flexible task list. |
| 2 | Progress across sources is invisible. | **Per-course progress grids**. |
| 3 | Motivation needs feedback loops. | **Streaks** for study + personal. |
| 4 | Missed tasks silently disappear. | **Carry-over reminders**. |
| 5 | Reflection helps. | **14-day history + monthly heatmap**. |
| 6 | Friction kills habits. | **No login, offline, installable**. |

### 3.2 Competitive landscape
| Alternative | Reality | Gap this fills |
|---|---|---|
| Generic to-do apps | No study progress or streaks | Learning-specific grids + streaks |
| Course platforms | Siloed per course | Cross-source daily plan |
| Habit trackers | Not task-aware | Combines tasks + habit streaks |

---

## 4. User Personas

### Primary — "Self-learner Sana" 🎯
| Attribute | Detail |
|---|---|
| Who | Aspiring PM studying across free resources |
| Pain | Inconsistent; can't see progress; loses motivation |
| Goal | A daily, flexible, visibly-tracked study habit |
| Wins | Streaks + grids + carry-overs keep her going |

### Anti-persona
Learners in a single structured bootcamp with built-in tracking.

---

## 5. Goals & Success Metrics

### North Star Metric
> **Active study days** (days a user completes ≥1 planned task).

### Supporting metrics (proposed)
| Category | Metric | Target |
|---|---|---|
| Activation | % who plan + complete a task day 1 | ≥ 70% |
| Habit | Current/longest streak length | trending up |
| Retention | 14-day retention | ≥ 30% |
| Completion | % planned tasks completed | ≥ 60% |
| Recovery | % carried-over tasks later done | ≥ 40% |

### Guardrails
- Data never lost (local); offline reliability; no demotivating friction.

---

## 6. Solution & MVP Scope

**Solution:** A single-file PWA that turns a task library into a flexible daily plan with streaks, progress grids, history and carry-overs.

### MVP (shipped)
| Capability | Description |
|---|---|
| 📋 **Flexible daily plan** | Add only the tasks you have time for from a library |
| ➕ **Custom tasks** | Add your own with name, icon, link |
| 📈 **Progress grids** | Long-term progress across Cohere, HelloPM, Learn Prompting, The Noob PM |
| 🔥 **Streaks** | Daily streaks for PM study *and* personal tasks |
| 🗓️ **History** | 14-day card view + monthly heatmap |
| ↪️ **Carry-over** | Reminders for missed tasks |
| 📲 **Offline PWA** | No login/server; installable |

### Out of scope
- Accounts/sync, social/leaderboards, content hosting.

---

## 7. User Flow (Flowchart)

```mermaid
flowchart TD
    A([Open planner - Today]) --> B[Pick tasks from library for today]
    B --> C[Work through today's tasks]
    C --> D{Task done?}
    D -- Yes --> E[Mark complete → streak + grid update]
    D -- Not today --> F[Carry over to tomorrow]
    E --> G[History: 14-day cards + heatmap]
    F --> A
    G --> H[See progress across courses]
```

---

## 8. System Architecture

```mermaid
flowchart LR
    subgraph Client["Browser PWA (single file)"]
      UI[Today / Progress / History tabs]
      LOGIC[Streaks + carry-over + grids]
      LS[(localStorage)]
      SW[Service worker - offline]
    end
    UI --> LOGIC --> LS
    UI -.offline-first.- SW
```

**Key decisions**
- **Local-only, no account** — zero friction, private, offline.
- **Flexible over rigid** — pick-what-fits beats fixed schedules for real adherence.
- **Gamification (streaks/grids/heatmap)** as the retention engine.

---

## 9. Wireframe (low-fidelity)

```
┌───────────────────────────┐
│ 🎯 PM Study Planner        │
│ 📋 Today  📈 Progress  🗓️ │
├───────────────────────────┤
│ All tasks → [+ Add]        │
│ Today's tasks:             │
│  ☐ 💡 Case study question  │
│  ☑ 🎥 HelloPM video 🔥3    │
├───────────────────────────┤
│ Streak: 🔥 3 days          │
│ Heatmap ▓▓░▓▓░░            │
└───────────────────────────┘
```

Shipped UI in **Section 11**.

---

## 10. Roadmap

```mermaid
timeline
    title PM Study Planner Roadmap
    Phase 0 — Core : Task library : Flexible daily plan : localStorage
    Phase 1 — Motivation : Streaks : Progress grids : Custom tasks
    Phase 2 — Reflection : 14-day history : Monthly heatmap : Carry-over reminders
    Next : Reminders/notifications : Cloud sync (opt-in) : Shareable progress
```

---

## 11. Screenshots

### Today — plan & track your study day
![PM Study Planner](screenshots/01-today.png)

---

## 12. Key Decisions & Trade-offs

| Decision | Options | Choice & why |
|---|---|---|
| **Rigid vs flexible plan** | Fixed schedule vs pick-what-fits | **Flexible** — survives busy days, better adherence. |
| **Motivation** | None vs streaks/grids | **Streaks + grids + heatmap** — visible momentum. |
| **Storage** | Cloud vs local | **Local** — private, offline, zero setup. |
| **Missed tasks** | Drop vs carry-over | **Carry-over** — reduces guilt, keeps momentum. |

---

## 13. What I'd do next
1. **Reminders / notifications** to prompt daily planning. *(habit)*
2. **Opt-in cloud sync** for multi-device. *(reach)*
3. **Shareable progress cards** for accountability. *(virality)*

---

## 14. Appendix — Tech
- Single-file vanilla JS PWA, localStorage, offline service worker, GitHub Pages.
