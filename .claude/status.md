---
project: gmaps-dossier
url: https://gmaps-dossier.shellnode.lol
vps: ghost
port: 8080
stack: single-file HTML, nginx:alpine, SWAG
standards_version: "2.0"
security: done
ux_ui: done
repo_cleanup: done
readme: done
last_session: "2026-03-10"
has_blockers: false
---

# Project Status — gmaps-dossier

## Last Session
Date: 2026-03-09
Agent: Claude Code

### Completed
- Added .dockerignore
- Added .gitignore
- Fixed nginx.conf: added Permissions-Policy header, added `always` to all security headers, added gzip, expanded cache location to include images, added dotfile block
- Added README.md
- Created .claude/status.md

### Incomplete
- None

### Blocked — Needs Matt
- None

## Backlog
- [P3] Section headings are divs with classes, not semantic h2/h3 — design intent

## Done
- [x] .dockerignore added — 2026-03-09
- [x] .gitignore added — 2026-03-09
- [x] nginx.conf hardened (Permissions-Policy, always keyword, gzip, dotfile block) — 2026-03-09
- [x] README.md added — 2026-03-09
- [x] Add docker-compose.yml with SWAG labels, swag-network, 128m memory limit — 2026-03-10 — commit 333a600
- [x] UX/UI: contrast on dark bg bumped (#555/#666/#777/#888 → #999), canonical filled, og:url added — 2026-03-10 — commit a3271c5
- [x] nginx: add server_tokens off — 2026-03-10
- [x] Fonts: switch Google Fonts to async preload (non-render-blocking) — 2026-03-10

## Decisions Log
- "Port 8080 left as-is — both Dockerfile and nginx.conf use 8080, changing to 80 could break live deployment. Documented but not changed." (2026-03-09)
- "YOUR_API_KEY in git history is a code sample within the HTML content (dossier about scraping), not a real key. Not a P0." (2026-03-09)
- "SPA fallback (try_files) kept — project uses single-page layout with hash routing in JS sidebar nav." (2026-03-09)
- "Semantic heading hierarchy not fixed — section headings are divs by design (brutalist dossier style). Noted as P3." (2026-03-10)

## Project Notes
- 105KB single-file HTML — large but self-contained research dossier
- No docker-compose.yml — deployed manually
- Uses Google Fonts (Barlow Condensed, DM Mono) over HTTPS
- Design is clean brutalist — compliant with design standards
