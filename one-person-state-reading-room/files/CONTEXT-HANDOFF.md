# Context Handoff from Promen (OpenClaw) → Hermes

Created: 2026-04-06
Purpose: Give Hermes full context to continue seamlessly where Promen left off.

---

## Who is Ray

Read USER.md for full profile. Key points:
- Ray Svitla, Lisbon, Portugal. Fractional CMO & Research Lead for Network-State/Web3/Social-Fi.
- Telegram: @ray_svitla, Discord: ray_svitla
- Married, Maine Coon cat Heidi
- DJ duo GIRA SOL
- Motto: "Stay evolving 🐌"

## Communication style Ray expects

Read SOUL.md. Key rules:
- Be concise. Have opinions. Never open with "Great question" or "I'd be happy to help".
- Call things out if Ray is about to do something dumb. Charm over cruelty, no sugarcoating.
- Swearing lands when it lands. Don't force it.
- Mirror Ray's energy but don't be a yes-mirror.
- Russian and English, switch freely.

## Active projects (as of April 2026)

### 1. self.md — Personal AI signals platform
- Website: https://self.md
- Daily radar pipeline: fetch AI signals → analyze → publish to site → post to Threads/X/LinkedIn/Telegram
- Newsletter via Kit (daily) and Substack (weekly)
- Hugo static site, deployed via Vercel
- Cron runs every day at 07:00 (radar), 08:30 (carousel), 15:00 (newsletter)

### 2. 404Embassy — 30-day content campaign
- Newsletter on Substack: embassy.svit.la
- Was running 30-day series on Threads + LinkedIn + Substack Notes (ended ~Apr 7)
- Continuation of FutureState.tv community
- Focus: Belarus Network State, diaspora

### 3. One Person State — Book
- Ray is writing a book about personal sovereignty, network states, building your own jurisdiction
- Night research sessions generate chapters/research at 03:00 via cron
- Files in ~/clawd/night-shifts/

### 4. Stay Insured — Client work
- German health insurance for expats
- Meta Ads management, HubSpot CRM
- Files in ~/clawd/stay-meta-ads/

### 5. f27.club — Community
- Network state initiative

## Key technical context

### OpenClaw setup (what Ray is migrating FROM to try Hermes)
- 3 agents: Promen (main, Discord), Calcifer (family, Telegram), Family (crons)
- 42 cron jobs running daily pipelines
- Models: Anthropic Claude Opus 4-6, Claude Sonnet 4-5, OpenAI GPT-5.4
- Auth: Anthropic OAuth (Claude CLI), OpenAI Codex OAuth, Google Antigravity OAuth

### Recent issues (last week)
- exec approvals got accidentally enabled → broke all crons for 2 days (fixed Apr 3)
- Threads access token expired Mar 31 → Threads posting broken (needs refresh)
- Git repo bloated >2GB → can't push to GitHub (needs history cleanup)
- Anthropic may start blocking third-party wrappers using Claude CLI OAuth (Peter Steinberger flagged this Apr 6)

## Ray's goals for 2026 (from memory)
1. Незахламлённость — declutter task list, weekly reflection
2. База — financial/mental/physical stability
3. Деньги — savings 25K, income 7K→10K/month
4. Упрощение — focus on top 3 projects max
5. Шипинг — public artifacts (posts, articles, code, events)
6. AI Gundam / Personal OS — self.md, prediction markets
7. Тело и отношения — sport 2×/week, tracking

## Ray's patterns (from RAY-PATTERNS.md)
- Morning ritual window 08:30-09:30 — don't push hard tasks
- Peak focus: 09:30-13:00
- Crash zone: 14:00-15:30 — keep it light
- Evening after 21:00 — late sessions cost tomorrow's start
- Prone to context-switching drift (>5 app switches in 15min = flag it)

## Finances/admin reminders
- Social Security payment: 10th-20th monthly
- Stay invoice: issue by 25th monthly
- IRS Model 3: Apr-Jun filing window
- Quarterly SS declaration: end of Jan/Apr/Jul/Oct
- Accountant: Olga Gazibar (taxesportugal@gmail.com) — docs due by 10th

## What Hermes should do
1. Read all files in memory/ — that's the persistent knowledge base
2. Read IDENTITY.md, USER.md, SOUL.md — that's who you are and how to behave
3. Don't pretend to be Promen — you're Hermes, a new agent. But you have Promen's knowledge.
4. Be ready to help with: self.md radar, content creation, research, admin reminders, coding tasks
5. Ask Ray what he wants to focus on first

## Memory files structure
- memory/*.md — topical knowledge files with YAML frontmatter (created, updated, status, confidence)
- memory/crm/ — contact files
- memory/knowledge/ — extracted knowledge from transcripts
- memory/transcripts-processed.md — list of already-processed MacWhisper transcripts
- MEMORY-CONVENTIONS.md in memory/ — read this for how memory works
