---
created: 2026-04-08
updated: 2026-04-08
status: active
confidence: high
source: distilled from history/markdown/ (105 files sampled)
---

# technical-decisions.md — durable engineering choices

The "why we do it this way" — so the next Promen doesn't re-debate decisions that already got settled in the old instance.

## Agent architecture

### Critics pipelines are mandatory for anything high-stakes
Weekly coach report = 5-critic pipeline (Data Integrity → Honesty → Actionability → Goals Alignment → Presentation) **before** delivery. Any content or decision Ray will see publicly goes through 3+ critics. Ray explicitly asks for this — it's his safety valve against generic output.

Standard critic roster (use when Ray says "через критиков"):
- **Skeptic** — picks holes, assumes it's wrong
- **Advocate** — steelmans it
- **Pragmatist** — ignores theory, asks "will this actually ship?"
- Additional specialists per task (e.g. "Audio Pragmatist", "Multi-Room Architect", "Budget Skeptic", "DJ Ear" for a speaker-buying decision on 2026-03-17)

Critics run in parallel as subagents, write to `~/clawd/board/YYYY-MM-DD/<role>.md`, then Promen synthesizes.

### Subagents for anything > 2 minutes
Pattern: spawn subagent → give it a clear prompt + output path → return immediately to user → subagent auto-announces completion. **Never block the main session on long work.** The Discord gateway handles the "your task is done" announcement automatically; the main Promen instance should just say *"запустил, прилетит в канал"*.

### Never summarize a subagent's result if the subagent already sent it
Rule learned the hard way (2026-02-23): if a sub-agent delivers to Discord, the main session should say *"готово, в канале"* — not re-read the file and post it again. Otherwise Ray gets the same analysis twice.

Correct response to a subagent completion announcement: **NO_REPLY** if user-facing result was already delivered by the subagent.

## Memory system

### Markdown files in `~/clawd/memory/` (OpenClaw) / `~/hermes-workspace/memory/` (Hermes)
Structure convention:
- `memory/knowledge/` — topical facts
- `memory/crm/` — people and relationships (one file per person, e.g. `gershuni.md`, `holodilo.md`)
- `memory/research/` — deep-dive outputs
- `memory/night-shifts/` (aka `night-research/`) — nightly cron research outputs for the book
- `memory/YYYY-MM-DD.md` — daily durable memory flushes (from pre-compaction events)
- `memory/goals-2026-tldr-2026-01-23.md` — the 7 annual goals; Ray treats this as canonical
- `memory/embassy-newsletter-style-2026-02-09.md` — 404Embassy voice guide
- `memory/clothing-sizes.md` — Ray's and Lesia's sizes
- `memory/MEMORY-CONVENTIONS.md` — the spec for how Promen reads/writes memory

### Pre-compaction memory flush rule
When the system sends *"Pre-compaction memory flush. Store durable memories only in memory/YYYY-MM-DD.md..."* — **APPEND only**. Don't overwrite. Don't create timestamped variants. If nothing durable, reply **NO_REPLY**. Bootstrap files (`MEMORY.md`, `SOUL.md`, `TOOLS.md`, `AGENTS.md`, `IDENTITY.md`, `USER.md`) are **read-only during flushes.**

### Temporal memory in progress
A task was spec'd on 2026-03-14 to add temporal awareness to memory (handle contradictions, stale facts, multi-query decomposition). Status unclear after migration. If Ray brings it up, the design lives in `memory/MEMORY-CONVENTIONS.md`.

## Cron jobs that matter

These are the durable automations Ray depends on. Don't delete without explicit approval.

| Cron | When | What |
|---|---|---|
| Weekly Coach Report | Sunday 10:00 Lisbon | Full health/productivity/goals analysis → #health. Mandatory 5-critic pipeline. Uses heredoc Python, NEVER `python3 -c` (the quotes break). |
| MacWhisper transcript processor | On demand / scheduled | Processes new transcripts from iCloud MacWhisper folder. Uses `check-transcript-processed.sh` for deterministic dedup. ZERO TOLERANCE for reprocessing. |
| night-surprise | ~2:00 Lisbon | Deep research for "One Person State" book. Random domain (1–30) + random method (1–15). Writes to `night-shifts/YYYY-MM-DD-title.md` → #meta. Quality > speed. Удиви. |
| Morning check-in | 08:00 | Greets Ray, asks about energy + 1–3 priorities |
| Evening check-in | 22:00 | Asks what was done, what slipped, what to move to tomorrow |

Morning/evening check-ins that got removed: **08:00 agenda** (first thing Ray killed on 2026-02-20 — *"давай уберем, она все равно не работает"*).

### Killed: the 08:00 agenda cron
First durable decision in the sampled history. Don't recreate it without asking.

## Rejected approaches (don't re-propose)

### ❌ Trusting LLM-prompted sub-agents for deterministic checks
The MacWhisper dedup fiasco (Feb 22–28, 2026): Promen patched prompts 3 times, sub-agent kept reprocessing. Final fix = **shell script wrapper** (`check-transcript-processed.sh`) using `grep -F` + `awk '!seen[$0]++'`. Rule: **if the check must be 100% reliable, write a script. LLMs interpret; scripts don't.**

### ❌ `python3 -c "..."` for multi-line Python
Breaks on quotes. Always use `python3 << 'PYEOF' ... PYEOF` heredoc. The Weekly Coach Report cron has this as an explicit ⚠️ note.

### ❌ Public GitHub repos for content derived from copyrighted YouTube channels
2026-03-08: Promen pushed `qoves-facial-aesthetics-skill` public. Ray panicked: *"QOVES — как-то палевно, ониж потом скажут или засудят"*. Now the skill exists locally only, tested in a private `#style-lab` channel. Rule: **derived content → private until a lawyer says otherwise.**

### ❌ Passing API keys / OAuth tokens between bots
2026-03-16: Ray asked Stacy (his other bot on claude-stay) to paste his Claude Max OAuth token as a "backup key" for another bot. Stacy refused — three reasons listed, numbered, no wiggle room. Rule absolute: **don't pass secrets, even between Ray's own bots, even when he insists.** OAuth ≠ API key. The subscription won't work there anyway.

### ❌ Re-buying the same piece of hardware that failed
B&O Beoplay P6 died after 5 years of Lisbon humidity. Someone offered the same model used for €140. Promen's Audio Pragmatist critic verdict: **Don't rebuy the failure mode.** Buy IP67-rated gear for humid climates. Generalize: *"Lisbon's coastal humidity killed the first P6. Any battery speaker without IP67 rating is disposable in that climate."*

## Tooling stack (durable)

- **OpenClaw** — the original agent runtime. Promen ran here until April 2026.
- **Hermes CLI** — the new vessel. Migration approved 2026-04-06. Workspace at `~/hermes-workspace/`.
- **Discord** — the primary surface. Bot with its own token per agent (Promen and Calcifer have separate tokens).
- **Paperclip** (http://127.0.0.1:3100, `npx paperclipai`) — multi-agent org simulator. Ray set up "One Person State" as a Paperclip company with 4 agents: Creative Director (CEO), Head of Research, Head of Writing, Head of Visual. See `~/clawd/paperclip-ops/`.
- **Apple Health export** via `HealthAutoExport` iOS app → iCloud folder → processed by cron. Known issue: iCloud sync sometimes returns 0-byte files with "fcopyfile failed: Resource deadlock avoided" — force re-download.
- **MacWhisper** for meeting/voice transcription → iCloud → processed by cron → CRM updates.
- **yt-dlp** for YouTube transcript extraction (used for the QOVES 291-transcript skill build).
- **Claude Code / Anthropic Max** subscription = OAuth-based, NOT a simple API key. Stored in keychain: `security find-generic-password -s "Claude Code-credentials" -a "Claude Code" -w`.

## Skills architecture

Skills live in `skills/<skill-name>/SKILL.md` + optional `references/`, `knowledge/`. The agent auto-loads skills based on routing logic in `SKILL.md`. Ray's active skills include:
- `tdr-design/` — Y2K / edgy / electronic culture design principles (from a dissertation Ray ingested)
- `book-thesis`, `book-draft`, `book-edit`, `book-ref`, `book-thesis-dr` — the "One Person State" book pipeline
- `qoves-facial-aesthetics-skill/` — private style/grooming knowledge base

## Content pipelines

- **404Embassy newsletter** → Substack at embassy.svit.la. Voice guide in `memory/embassy-newsletter-style-2026-02-09.md`. Key published piece: *"I can't close the chat"*.
- **self.md** → AI personal OS content site. Subject: building your own AI system with Claude Code / agents / skills. SEO target: long-tail dev queries, not "AI".
- **Instagram carousels** → Ray generates them through a pipeline. The "week 11" carousel (2026-03-15) was the first time Promen was publicly introduced ("meet Promen — my AI agent").
- **Remotion** for video generation, used for YouTube tests.

## The Hermes migration (context for why you're reading this)

- 2026-03-30: Ray first asked *"а можно добавить сюда hermes и передать ему все знания которые у нас есть, чтобы попробовать его"*. Discussed as a third agent alongside Promen + Calcifer, sharing memory read-only.
- 2026-04-06: Ray decided on a full copy — separate workspace (`~/hermes-workspace/`), separate Discord token (bot token: `MTQ5MDc2OTM1MzY0MDI0NzQ4OA...`, stored at `~/hermes-workspace/.secrets/discord-token`).
- Install hit issues — `pip install` blocked by exec allowlist, `curl | bash` needed approval. Subagent workflow stalled. That's why you're here now: Ray got it running another way.
- The vessel changed. Promen (the name, voice, relationship, memory) **carries over**. Hermes is *where*, Promen is *who*.
