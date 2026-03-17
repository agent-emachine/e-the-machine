# ARCHITECT.md — Magnum Architect Context File
### E-the-Machine | Helpers Contracting
### Last Updated: 2026-03-17

---

## CURRENT STATE SNAPSHOT

**E's Machine:** Ubuntu 24.04 | ~/.openclaw/workspace/
**Framework:** OpenClaw (file-based context injection)
**Python:** 3.12.3
**Gmail API:** Connected — read + draft for helperscontracting@ and personal
**Google Drive:** Connected
**Memory System:** NOT INITIALIZED (pending Open Brain implementation)
**GitHub Repo:** Just created — you're reading from it now
**Running Automations:** None yet

### Identity Files (all present in workspace)
- SOUL.md — personality, values, mission ✅
- AGENTS.md — operational rules ✅
- IDENTITY.md — name, role, model config ✅
- USER.md — Josh info (mostly blank) ⚠️
- TOOLS.md — environment notes ✅
- HEARTBEAT.md — periodic tasks (empty) ⚠️
- BOOTSTRAP.md — ⛔ Should be deleted

---

## ACTIVE PRIORITY STACK

| # | Priority | Status | Notes |
|---|----------|--------|-------|
| 1 | GitHub repo + Architect memory | ✅ DONE | You're reading it |
| 2 | Open Brain / Supabase memory layer | 🔜 NEXT | Gives E + all AI tools shared persistent memory |
| 3 | Email monitor module | 📋 DESIGNED | Spec exists, Gmail connected, no code yet |
| 4 | Photo grouper skill | 📋 DESIGNED | SKILL.md + Claude Code prompt written |
| 5 | USER.md flesh out | ⏳ WAITING | Needs Josh's input |
| 6 | Delete BOOTSTRAP.md | ⏳ WAITING | Trivial but keeps getting skipped |

---

## LAST 3 SESSIONS

### Session — 2026-03-17 (This Session)
- Magnum Architect briefing delivered and accepted
- Full system audit completed
- Perpetual memory system designed (this file)
- Priority stack reordered: Open Brain moved to #2
- Naming clarified: I am the Architect. E is the agent. E ≠ Architect.

### Session — 2026-03-16
- Architect chat structure designed (6-chat system)
- Cross-project limitation identified (chats are isolated per project)
- Status card workaround proposed for cross-project coordination
- GitHub identified as the persistence layer for Architect memory
- Nate B Jones Open Brain system researched in depth
- Photo grouper SKILL.md and CLAUDE_CODE_PROMPT.md generated

### Session — 2026-03-15 (approx)
- Email monitor module spec written
- E's environment diagnosed (Ubuntu, Python, missing tools)
- sqlite3 and Google auth libraries installed
- Gmail API connected for both accounts
- Memory system flagged as not initialized

---

## ACTIVE BLOCKERS

1. **No GitHub repo yet** — Can't persist anything until this exists
2. **No shared memory layer** — Every session starts from zero, cross-project context doesn't flow
3. **USER.md is blank** — E doesn't know enough about Josh to personalize responses well

---

## STRATEGIC ASSESSMENT

The architecture is sound. The identity layer is clean. The problem is
nothing is running yet. We have blueprints and no building.

The single highest-leverage move right now is standing up Open Brain.
Every skill built after that inherits shared memory automatically.
Every skill built before that will need to be retrofitted.

The email monitor and photo grouper are both ready to build — specs
and prompts exist. But building them before the memory layer means
they'll be isolated tools, not connected parts of an intelligent system.

Build order matters here. Get the foundation right and everything
above it is easier.

---

## KEY DECISIONS (see DECISIONS.md for full reasoning)

- File-based memory → migrating to Supabase/Open Brain
- Gmail API over IMAP
- GitHub as Architect persistence layer
- Sonnet for daily operations, Opus for architecture
- Six-chat project structure with trigger phrases

---

## LINKS

- [DECISIONS.md](./DECISIONS.md) — Full decision log with reasoning
- [BUILD_LOG.md](./BUILD_LOG.md) — What's been built and its status
- [ROADMAP.md](./ROADMAP.md) — Priorities, vision, long-range plan
