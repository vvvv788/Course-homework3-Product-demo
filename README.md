# 🎯 REPS · Clickable Prototype

**Turn every rep into a comparable one.**

A practice tool for interview-prep students — one rubric, week over week.

🔗 **Live demo:** https://vvv788.github.io/Course-homework3-Product-demo/

👩💻 Coursework: **vivi (Lin Ziwei) · HW03**

---

## 💡 What it is

REPS is a clickable prototype of a practice tool for people preparing for job interviews.

It does **not** teach you how to answer. It does one thing: **score every answer against the same rubric**, so that *"did I actually get stronger this week?"* becomes a visible signal instead of a feeling.

---

## 📐 The one thing it tries to prove

**Three things must stay unchanged:**

1. 🎯 **Role** unchanged
2. 📊 **Rubric** unchanged — 4 dimensions × 25 pts
3. 📝 **Question type** unchanged — behavioral

Only when all three hold are this week's 78 and last week's 66 comparable at all.

This is labeled explicitly on both the Score and the Progress screen. When the conditions aren't met, the prototype **says so instead of drawing a fake upward line**.

---

## 🤔 Why not just practice randomly

**Without it** — you practice for weeks and still can't tell whether you improved. Every session uses a different standard, so scores don't line up.

**With REPS** — same role, same rubric, so each new score subtracts from the previous one. Progress is visible, and so are the weak spots.

---

## 🚀 Run it locally

Just double-click `index.html`. It is a single file with zero dependencies and zero external requests — it works offline.

Or serve it:

```
python -m http.server 8000
```

Then open 👉 `http://localhost:8000`

---

## 🔄 The six-step loop

**Home → ① Diagnose gap → ② Generate question → ③ Answer → ④ Score → ⑤ Progress signal → ⑥ Exit mechanism**

- **① Diagnose gap** 🔍 — Three inputs: target role, background, and your gut feel on where you lose points. The diagnosis decides which dimension today's question stresses.
- **② Generate question** ⚙️ — Same role draws from the same bank, so sessions stay comparable. Staged 4-phase progress text, not just a spinner.
- **③ Answer** ✍️ — Char count and timer are visible. Voice answer and sample answer shortcuts available.
- **④ Score** 📊 — 4 dimensions × 25 pts = 100. Shows each dimension's delta vs. last time, plus the two things to fix next.
- **⑤ Progress signal** 📈 — With fewer than two records, it draws **no line** — explanation and guidance instead.
- **⑥ Exit mechanism** 🚪 — Pass line fixed at 80. After 2 consecutive passes it tells you to drop to weekly and go interview.

**Scoring rubric:** 🏗️ Structure · 📌 Evidence · 🎯 Role relevance · 💬 Clarity — 25 points each.

---

## ✨ Features

- 🌏 **Bilingual 中文 / English** — the top-right toggle switches everything at once: UI copy, questions, role names, scoring reasons. Your choice persists in `localStorage["reps-lang"]`.
- 🔐 **Log in / Sign up** (top-right) — a UI demo with validation. **No backend, no real account, nothing uploaded.**
- 🧩 **Full state coverage** — loading, failure (retry in place, content kept), empty (no fake chart line), boundary (empty submit hint, over-long answer warning).
- ♿ **Accessibility** — fully keyboard reachable, `aria-live` announcements on screen change, respects reduced-motion.
- ↩️ **Reversibility** — clear answer, swap question, start a new cycle, jump back to any completed step.
- 📝 **Design notes drawer** — the reasoning behind each screen, plus the demo switches below.

---

## 🎬 Demo shortcuts (for presenting in class)

- 📦 **Load demo data** — 3 weeks of fictional history + this rep, so you get a full curve immediately.
- ⌨️ **Fill sample answer** — submits a well-structured but evidence-light answer → **81** total, with **Evidence 13/25** as the obvious weak spot.
- 💥 **Simulate generation failure** — forces the failure state so you can demo the retry path.

---

## 🛠️ Tech notes

- Single HTML file, ~160 KB. **No build step, no frameworks, no CDN requests, works offline.**
- Plain CSS custom properties, glass-effect sticky topbar, aurora gradient background.
- i18n via four data attributes — `data-i18n`, `data-i18n-html`, `data-i18n-ph`, `data-i18n-aria` — plus zh/en dictionaries and instant re-render on switch.
- All state stays in the browser: language, mock login, practice history. **Nothing leaves the device.**
- ⚠️ **Scoring uses local keyword and structure rules, not a real model.** When a model gets attached, the rubric and dimensions stay exactly the same — only the judge changes.

---

## ⚠️ Disclaimer

This is a **product-design prototype**. Questions, scores and history are all demonstration content, and the score is produced by local rules — it is not an assessment of anyone's ability. The login flow creates no real account.

---

*Made for an easy-vibe course assignment · HW03 · 2026*
