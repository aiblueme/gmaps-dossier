---
project: gmaps-dossier
url: https://gmaps-dossier.shellnode.lol
vps: ghost
port: 8080
stack: single-file HTML, nginx:alpine, SWAG
standards_version: "2.0"
security: done
ux_ui: not_started
repo_cleanup: done
readme: done
last_session: "2026-03-09"
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
- UX/UI audit not started — project is large (105KB HTML), skipped for this session to stay within scope

### Blocked — Needs Matt
- None

## Backlog
- [P2] UX/UI audit — check responsiveness, page weight, console errors, broken links
- [P3] docker-compose.yml with SWAG labels and memory limit
- [P3] `server_tokens off` (may already be handled at SWAG level)

## Done
- [x] .dockerignore added — 2026-03-09
- [x] .gitignore added — 2026-03-09
- [x] nginx.conf hardened (Permissions-Policy, always keyword, gzip, dotfile block) — 2026-03-09
- [x] README.md added — 2026-03-09

## Decisions Log
- "Port 8080 left as-is — both Dockerfile and nginx.conf use 8080, changing to 80 could break live deployment. Documented but not changed." (2026-03-09)
- "YOUR_API_KEY in git history is a code sample within the HTML content (dossier about scraping), not a real key. Not a P0." (2026-03-09)
- "SPA fallback (try_files) kept — project uses single-page layout with hash routing in JS sidebar nav." (2026-03-09)

## Project Notes
- 105KB single-file HTML — large but self-contained research dossier
- No docker-compose.yml — deployed manually
- Uses Google Fonts (Barlow Condensed, DM Mono) over HTTPS
- Design is clean brutalist — compliant with design standards
