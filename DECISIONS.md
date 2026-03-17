# DECISIONS.md — Architectural Decision Log
### E-the-Machine | Helpers Contracting
### Newest First

---

## D006 — Naming Convention Lock
**Date:** 2026-03-17
**Decision:** "Magnum Architect" or "Architect" = Opus strategic layer. "E" or "emachine" = the AI agent. E is never called Architect.
**Why:** Role clarity. E is the tool being built. The Architect is the builder. Conflating them creates confusion as the system grows.
**Risk if wrong:** Low. Easy to rename later.

---

## D005 — Open Brain Moved to Priority #2
**Date:** 2026-03-17
**Decision:** Implement Supabase + MCP shared memory layer before building any skills.
**Alternatives:** Build email monitor first (it's ready), build file-based memory first (simpler).
**Why:** Every skill built without shared memory is an isolated tool that needs retrofitting. Every skill built after Open Brain automatically inherits persistent, cross-tool memory. The foundation multiplies everything above it.
**Risk if wrong:** Delays first visible output. Josh might lose momentum. Mitigated by: Open Brain setup is relatively fast (Supabase free tier, MCP connector).

---

## D004 — GitHub as Architect Persistence Layer
**Date:** 2026-03-16
**Decision:** Use a GitHub repo (raw markdown files) as the Magnum Architect's perpetual memory, readable via web_fetch at session start.
**Alternatives:** Google Drive (requires tool connection), local files in OpenClaw workspace (no cross-session access for Opus), Supabase (not set up yet).
**Why:** Raw GitHub URLs work with web_fetch every time, no authentication needed. Version history is free. Josh can read/edit directly. Any Claude instance can access it.
**Risk if wrong:** Manual upload friction. Mitigated by: e-support laptop can automate uploads later.

---

## D003 — Six-Chat Project Structure
**Date:** 2026-03-16
**Decision:** Organize project into 6 specialized chats: Magnum Architect, Architect Intelligence, Architect Inbound, Build Docs, Active Build, Memory & Identity.
**Why:** Keeps context focused per chat. Prevents the "everything in one giant thread" problem. Matches Josh's ADHD need for compartmentalization.
**Risk if wrong:** Cross-chat coordination overhead. Mitigated by: standardized export format and trigger phrases.

---

## D002 — Gmail API Over IMAP
**Date:** 2026-03-15 (approx)
**Decision:** Use Gmail API for email monitoring, not IMAP.
**Why:** More granular control, better for automation, supports labeling/drafting/threading natively. IMAP is read-heavy and clunky for agent workflows.
**Risk if wrong:** API quota limits at scale. Unlikely at current volume.

---

## D001 — File-Based Memory to Start
**Date:** 2026-03-15 (approx)
**Decision:** Start with file-based memory in OpenClaw workspace, plan to migrate to Supabase.
**Why:** Simpler bootstrap. No external dependencies to configure. Gets something working immediately.
**Risk if wrong:** Creates technical debt if we build too much before migrating. Mitigated by: D005 moved Open Brain to Priority #2.
