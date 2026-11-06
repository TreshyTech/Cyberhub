# CyberHub — Personal Cybersecurity Learning Hub

A static, local-first Progressive Web App (PWA) for tracking cybersecurity learning, practical projects, skills, study tasks and journal entries.

## Included
- 15 career roadmaps with beginner, intermediate and advanced levels.
- Expandable topic detail, prerequisites, learning outcomes and completion checkboxes.
- Project laboratory with step lists, checklists, status, evidence links and GitHub links.
- Curated resource library with search, categories and saved resources.
- Skill self-assessment tracker.
- Study planner and learning journal.
- Certification shortlist and portfolio-readiness checklist.
- Progress dashboard, activity history and downloadable report.
- JSON backup and restore.
- Dark/light theme, responsive layout and PWA service worker.

## Run locally
For a quick preview, open `index.html` in a modern browser. For PWA installation and offline caching, serve it over HTTPS or localhost (not `file://`).

Python example:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

## Deploy with GitHub Pages
1. Create a new GitHub repository, e.g. `cyberhub`.
2. Upload all files in this folder to the repository root.
3. Open **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish the site.
6. Open the published HTTPS URL.

If deploying to a repository subpath, the relative asset paths in this project are already suitable.

## Add to iPhone Home Screen
1. Open the published HTTPS URL in Safari.
2. Tap Share.
3. Choose **Add to Home Screen**.
4. Confirm the name and tap Add.

On Android/desktop, use the browser's Install app option when offered.

## Data and privacy
- Learning progress is stored in `localStorage` in the browser on the current device.
- No account, cloud sync, analytics or external database is included.
- Clearing browser site data may erase your progress.
- Export a JSON backup regularly and store it somewhere private.
- Imported backups replace the current local workspace after confirmation.
- Avoid storing passwords, API keys, personal data or sensitive incident evidence in journal entries.

## Curriculum maintenance
Roadmap snapshot: **v1.0.0 — reviewed 6 November 2026**.

Framework/resource review notes:
- NIST Cybersecurity Framework 2.0.
- NIST NICE Framework Components v2.2.0 (April 2026).
- MITRE ATT&CK v20.0 (October 2026).
- OWASP Top 10:2025.
- CIS Critical Security Controls v8.1.
- TryHackMe Cyber Security 101 and SOC Level 1 paths; check provider pages for changes and access terms.

This is a curated learning plan, not a live-updating feed. Review official sources every 3–6 months and before paying for a certification or course. Update `resources` and `pathSeeds` in `app.js`, change the review date and add a note to this changelog.

## Suggested source structure
- `index.html` — app shell and navigation.
- `styles.css` — responsive design and themes.
- `app.js` — curriculum data, rendering, local persistence and interactions.
- `manifest.webmanifest` — install metadata.
- `sw.js` — offline asset cache.
- `icon.svg` — app icon.

## Safe practice
Use intentionally vulnerable training environments, sample datasets and systems you own or have explicit authorization to assess. Keep virtual labs isolated. Do not publish credentials, personal data, access tokens or unredacted logs.

## Limitations
- Data is local to one browser/device; there is no automatic sync between devices.
- Service worker caching covers the app shell; external resource pages still require internet.
- Progress checkboxes are self-tracking aids, not formal skill validation.
- External links, prices, exam codes and course availability can change.
