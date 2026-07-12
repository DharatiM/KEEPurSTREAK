
# 🔥 Keep the Streak

A quiet, honest daily habit tracker built with React — no sign-up, no clutter, just you and your streak.

Every day you show up, you're asked to be honest: what actually **has** to happen *now*, what can wait until later *today*, how many hours you actually put into the things that matter, and how much time slipped into social media. Over a rolling 30-day window, all of that turns into a heatmap, a streak counter, and a set of progress charts — so patterns become visible instead of invisible.

---

## ✨ Features

### 🎯 Two kinds of tasks — Now vs Today
Every task you add is tagged as one of two priorities:
- **Now** — can't wait. Rendered at the top of the list with a warm amber glow and a subtle pulsing animation so it visually demands attention.
- **Today** — needs to happen before the day ends, but isn't urgent. Rendered calmly below, in sage green.

### 🟩 Per-task heatmap (30 days)
Every task gets its own GitHub-contributions-style heatmap. Each day you complete it, the cell fills in green — and the shade gets darker the more hours you log, so a light green square and a glowing dark green square tell two different stories at a glance.

### ⏱️ Hours-based monthly progress chart
Log how many hours you spent on a task each day (e.g. "Studied 2 hrs today, 1 hr tomorrow"). At any point, an area chart shows your total hours per day across the month, plus a breakdown line per individual task — so you can see effort trends building or fading over time.

### 🔥 Streak tracker
Counts consecutive days you've opened and used the app. Miss a day, and it resets — a simple, honest incentive to keep showing up, displayed as a glowing flame with the day count front and center.

### 📱 Screen-time honesty check
A separate, deliberately simple tracker: log how many minutes you spent on social media today. A line chart plots it over the month against your own rolling average, with a "trending up" or "trending down" indicator — the goal is awareness, not shame. Lower over time is the win condition.

### 💬 Daily purpose heading
The very first time you open the app, you're asked one question: *why are you here?* Whatever you answer becomes the heading shown every single day, front and center — a constant, quiet reminder of the reason you started.

### 🔒 Private by design
No login, no server, no tracking. All data lives in your browser's `localStorage`. Every friend you share the link with gets their own separate 30-day history on their own device — nothing is shared or visible to anyone else.

---

## 🛠️ Tech stack

| Layer          | Choice                                  |
|----------------|------------------------------------------|
| Framework      | React 19 + Vite                          |
| Styling        | Tailwind CSS v4                          |
| Charts         | Recharts (area & line charts)            |
| Icons          | lucide-react                             |
| Fonts          | Fraunces (display), Inter (body), JetBrains Mono (data/labels) |
| Persistence    | Browser `localStorage` (no backend, no database) |
| Hosting        | Static — deployable to Netlify, Vercel, or GitHub Pages |

## Live Link:
https://6a53d084d971062aaba272a1--gregarious-platypus-5b799a.netlify.app/

---

## 📂 Project structure
habit-tracker/
├── src/
│   ├── components/
│   │   ├── Onboarding.jsx        # First-run: name + purpose
│   │   ├── Header.jsx            # Daily purpose heading + streak counter
│   │   ├── TaskInput.jsx         # Add a task, choose Now / Today
│   │   ├── TaskCard.jsx          # Task row: complete toggle, hours input, heatmap
│   │   ├── Heatmap.jsx           # 30-day intensity grid for one task
│   │   ├── HoursChart.jsx        # Monthly area chart of hours logged
│   │   ├── ScreenTimeTracker.jsx # Social media minutes input + trend chart
│   │   └── MonthSummary.jsx      # Stat cards + HoursChart
│   ├── utils/
│   │   ├── dates.js              # Date key helpers, last-30-days generation
│   │   └── storage.js            # localStorage read/write, streak logic, trimming
│   ├── App.jsx                   # Top-level state + layout
│   ├── main.jsx                  # React entry point
│   └── index.css                 # Design tokens, gradients, animations
├── index.html
├── vite.config.js
└── package.json

