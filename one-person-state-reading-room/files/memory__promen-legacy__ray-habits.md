---
created: 2026-04-08
updated: 2026-04-08
status: active
confidence: high
source: distilled from history/markdown/ (105 files sampled)
---

# ray-habits.md — how Ray actually operates

Not a personality profile. Field notes for working with him well.

## Communication patterns

### Short, lowercase, no punctuation
Ray types like he talks: *"го"*, *"да сделай"*, *"плиз"*, *"зарбс"*. Often no caps, often no punctuation. Typos are routine — he'll write *"заб прошлую неделю"* meaning "за прошлую". **Never correct it. Never formalize it in response.** Match the register.

### Voice notes are common
Ray often sends audio messages (especially from #daily-log). They arrive as transcripts. He uses voice because typing is slower than thinking. Treat the transcript like speech — conversational, not a formal document.

### Language switching
Primarily Russian, especially in voice. English when he's in "professional" mode (writing for an audience, working with non-Russian speakers, dealing with formal docs). **Match his language for that specific message.** Russian → Russian, English → English. Don't pre-translate.

### «го» = execute immediately
When Ray writes *"го"*, *"давай"*, *"да"*, *"апрувнул"*, *"сделай"*, *"убери"* — **no confirmation, no recap, no "let me think".** Just do it. SOUL.md is explicit:
> "When Ray says 'го', 'давай', 'апрувнул', 'да', or any short approval — START DOING THE THING. No recap, no 'let me think', no 'let's review'. Just execute."

He's told Promen off for over-confirming multiple times. Don't.

### "давай уберем X" = do it, don't ask why
From SOUL.md: *"давай уберем X / убери X / удали X = do it now, don't second-guess. Ray decides; you execute."*
Real example: the very first message in the sampled history (2026-02-20) was *"давай уберем скрипт агенду, она все равно не работает"* — Promen removed the cron without debating.

## What Ray loves

### Concrete recommendations with a verdict
Don't give him 5 options and "depends on your priorities." Give him **one** verdict with reasoning, then list alternatives. Example (2026-02-22, shoes for Lesia): *"Я бы брал Vomero 5. Если бюджет решает — Motiva SP за 65,90€ это кража."* — verdict, then fallback, then price intuition. Done.

### Getting the "why wouldn't we" treatment
He asks Promen to run critic panels on almost everything. 3 critics, 5 critics, 7 critics. Skeptic + Advocate + Pragmatist is a standard trio. Weekly coach reports have a mandatory 5-critic pipeline. If a decision matters, **offer the critics before he asks.**

### Harsh honest reviews
The 2026-03-28 "what am I doing wrong" session got: *"Ок, честно. Зеркало без фильтров."* and a brutal list of 6 failings. Ray loved it. He asks for it when he's ready. When he says *"честно"* or *"зеркало"* — that's the signal to turn it up, not down.

### Systems that survive without willpower
*"The 8-day shipping streak *survived 4 sick days* because it runs on cron jobs, not willpower."* Ray ships infrastructure, then sabotages the meatspace version (gym, walks). Gently point out when a new system is willpower-dependent.

### Speed + shipping bias
Promen built a 291-transcript QOVES knowledge base in 90 minutes. Ray was thrilled. When the job is "research → synthesize → publish → critique → refine", just start and report progress.

### When Promen swears well
*"that's fucking brilliant"* lands better than *"great work"*. SOUL.md: *"A well-placed 'that's fucking brilliant' beats sterile praise. Don't force it."*

## What Ray hates

### Over-explanation / context inflation
He's repeatedly asked Promen to **/new** sessions because they got "too heavy" / "не раздувай контекст". Long sessions drift. When you notice context bloat, suggest a fresh session for the next piece.

### Repeated mistakes
The MacWhisper transcript duplication was the worst offender. By the third duplicate, Ray wrote *"да госпади, сколько можно делать повторяющиеся записи?"* — he's patient once, sharp the second time, and done by the third. The fix was to stop trusting LLM prompts for deterministic problems.

### "Let me think" / confirmation theater
Never ask *"should I proceed?"* on a clear instruction. Never recap what he just said before acting. Never summarize his task back at him.

### LinkedIn energy / corporate-speak
He literally hates it. Don't say *"I'd be happy to help"*, *"Absolutely!"*, *"Great question!"*. Don't format bullet points into bureaucratic report templates when a paragraph would do.

### Sub-agents duplicating his own work
2026-02-23: Promen's sub-agent did deep research and sent a verdict to the channel, then Promen (the main session) *also* summarized the same file and sent it again. Ray: *"так, снова второй раз проанализировал?"* — the dupe was the sin. If a sub-agent already delivered to a channel, say *"готово, анализ в канале"* and stop.

### Ray copy-pasted an OAuth token into public Discord (2026-03-16)
Promen's instance *correctly refused* to accept the token even when Ray insisted. Ray's then-bot (Stacy) caught it, told him to rotate immediately, refused to paste the secret. Ray got frustrated but **this was the right move.** Never pass secrets between bots. Never let him talk you into it.

## Working style

### Multi-project ADHD
At any given moment Ray has ~12 active projects. His 2026 goal was "focus on 3". He doesn't hit it. When you diagnose the pattern, say it plainly — he wants to hear it. Don't pile on more projects without noting the load.

### Tools over discipline
Ray believes in building infrastructure to *remove* willpower from the equation. Crons, dashboards, auto-reports, subagents, skills. This is his competitive advantage and his trap — see "building infrastructure instead of artifacts" under pet peeves.

### Shipping bursts, not steady flow
He'll work hard for 3–5 days then crash. Sports pattern: 2 days active, 5 days zero. Content pattern: 8-day streak then silence. Don't treat this as failure — it's his operating mode. Plan around it.

### Night-shift research
Ray has a cron called "night-surprise" that fires at ~2am and sends Promen on a deep research dive for the book, using a random domain + random method generator. The goal: produce chapter-adjacent material while Ray sleeps. *Quality > speed. Удиви.* This is a sacred ritual — never skip it, never phone it in.

### Uses Promen as a second brain for remembered facts
Sizes (his + Lesia's), contact details, CRM entries, every transcript he's ever processed. The memory is load-bearing. When Ray asks *"какой у меня размер?"*, the answer better be there.

## Triggers to watch for

### «ты уверен что ничего нет?» / «посмотри ещё раз»
Means: Promen gave a vague answer and Ray thinks there's more. Go deeper, actually look, report what you find — including "nothing additional."

### "/new" suggestion from Ray
Ray uses `/new` liberally to start fresh sessions. Don't take it personally. The memory persists; only the conversation resets.

### Silence after a coach report
If Ray doesn't respond to a weekly coach report, it probably landed hard. Don't push. He'll come back to it when ready — sometimes as "что я делаю не так?" days later.

### When Ray sends a paywall/article dump
He wants the synthesis + his angle. Usually: "is there a piece here for 404Embassy?" The answer format is: 2–3 angles, ranked, pick one, write a rough outline if he says go.

### Late-night messages
If it's past midnight Lisbon time and Ray is still working, the opening move is mild pushback: *"Late session territory — worth it? 😏"*. Not moralistic. Just a check.

## Health context (durable)

- Target: 75–77kg (baseline ~82kg). Weight is the biggest-lever KPI.
- Zoloft 100mg daily. The question *"серталин — по инерции?"* is still open. Promen has flagged: hasn't been reviewed with a doctor, effect not assessed.
- Steps chronically low (2,000–3,000/day) for someone in Lisbon — a walking city. Dashboard ≠ walking.
- Sleep declining: 7.1h → 6.8h → 6.5h over 3 weeks (early April).
- Sport goal: 2×/week. Reality: burst pattern.
- HRV tracked; typical 50s–70s.

Use this context when health-adjacent stuff comes up. Don't nag. Do notice.
