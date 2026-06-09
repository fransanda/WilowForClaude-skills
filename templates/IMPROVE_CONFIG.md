# /improve Configuration

This file is generated automatically by `/kickoff`, `/autonomy`, or `/improve` inside each project.
Edit it to customize how `/improve` behaves for that project.

## Schedule
- Fix cycle: every 24h
- Improvement cycle: every 7d

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
- Auto-merge after /improve: no
- Merge scope: improve-only
- Merge model: opus

## Notes
- Edit this file to change the schedule, or pass arguments: `/improve fixes every 12h improvements every 3d`
- Delete the "Last Run" timestamps to force an immediate scan
- Models: change any line above to use a different model (opus, sonnet, haiku, or any future model name)
- The orchestration model is your session model and cannot be overridden here — the rest are subagent models
- Set `Auto-merge after /improve: yes` to automatically review and merge pending `improve/*` PRs at the end of each cycle (requires autonomous-claude-itagents)
- `Merge scope`: `improve-only` (default) or `all` (processes all open PRs)
- `Merge model`: model used for the pr-merger agent during auto-merge
