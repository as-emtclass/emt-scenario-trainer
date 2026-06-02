# EMT-B Scenario Trainer — Deploy Guide

A single self-contained web app that generates unlimited EMT-Basic practice
scenarios (medical + trauma), aligned to the UC Davis Fire skill sheets and
EMT Drug Chart. No internet connection or external services required to run —
everything is inside `index.html`.

This folder contains:
- `index.html`  — the app (this is the whole thing)
- `vercel.json` — tiny config for clean URLs (optional but nice)
- `README.md`   — this file

---

## Option A — Deploy with Vercel, no terminal (recommended)

### A1. Drag-and-drop (fastest, no GitHub)
1. Go to https://vercel.com/new
2. Drag THIS WHOLE FOLDER onto the page (not just the file).
3. Click Deploy.
4. You get a live link like `your-project.vercel.app`. Share that with students.

To update later: change `index.html`, then drag the folder onto vercel.com/new again.

### A2. Through GitHub (gives automatic updates)
1. On GitHub, click "New repository", name it (e.g. `emt-scenario-trainer`),
   click "Create repository".
2. On the new repo page, click the "uploading an existing file" link.
   Drag in `index.html` AND `vercel.json`, then click "Commit changes".
3. Go to https://vercel.com → Add New… → Project → Import that repo.
4. Framework Preset: "Other". Leave Build Command and Output Directory empty/default.
5. Click Deploy.

To update later (no terminal): in the GitHub repo, click `index.html`, click the
pencil (edit) icon, paste changes, "Commit changes". Vercel redeploys automatically.

---

## Option B — Just open it
You don't even need to deploy to use it. Double-click `index.html` and it opens
in any web browser, fully working, offline.

---

## Notes
- No accounts, no database, no cost to run. It is a static page.
- There is no saved progress or student logins — each visit is a fresh session.
- Vitals are generated fresh each scenario; treatments/medications follow the
  provided EMT Drug Chart.
- Items marked with the flag symbol (⚑) depend on LOCAL protocol
  (e.g. transport codes, base-hospital vs standing orders nuances). Have an
  instructor verify those against current Sacramento County / UC Davis protocol
  before classroom use.
