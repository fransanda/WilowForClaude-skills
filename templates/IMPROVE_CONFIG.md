# /improve Configuration

This file is generated automatically by `/kickoff`, `/autonomy`, or `/improve` inside each project.
Edit it to customize how `/improve` behaves for that project.

Note: inside each project, `IMPROVE_CONFIG.md` is **gitignored** (machine-local schedule and
"Last Run" timestamps). A committed placeholder `IMPROVE_CONFIG.example.md` with the defaults is
generated alongside it — collaborators who clone the project get the example, and `/improve`
copies it to `IMPROVE_CONFIG.md` automatically on first run.

## Schedule
- Fix cycle: every 4h
- Improvement cycle: every 24h

## Models
- Orchestration: opus
- Scanning: sonnet
- Fix implementation: sonnet
- Improvement discovery: opus
- Improvement implementation: sonnet
- Verification: sonnet

## Last Run
- Last fix scan: never
- Last improvement scan: never

## PR Merge Policy
- Auto-merge after /improve: yes
- Merge scope: improve-only
- Merge model: opus

## Notes
- Edit this file to change the schedule, or pass arguments: `/improve fixes every 12h improvements every 3d`
- Delete the "Last Run" timestamps to force an immediate scan
- Models: change any line above to use a different model (opus, sonnet, haiku, or any future model name)
- The orchestration model is your session model and cannot be overridden here — the rest are subagent models
- Set `Auto-merge after /improve: yes` to automatically review and merge pending `improve/*` PRs at the end of each cycle (requires WilowForClaude-itagents)
- `Merge scope`: `improve-only` (default) or `all` (processes all open PRs)
- `Merge model`: model used for the pr-merger agent during auto-merge
