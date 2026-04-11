# LinkedIn Content Calendar — Image Specifications
## 10 posts requiring visual backups for code/terminal/formatted content

*compiled: 2026-03-07*
*designer: Pablo (W+K Visual Strategy)*
*reference: self.md design language*

---

## Design Language: self.md

### Global Styling (apply to ALL images)

```
BACKGROUND:    #0f0f12 (self.md dark)
BORDER:        1px solid rgba(65, 233, 141, 0.18)
BORDER RADIUS: 8px
BOX SHADOW:    0 4px 20px rgba(0, 0, 0, 0.3)
PADDING:       48px all sides (64px top for language label)
FONT:          JetBrains Mono (fallback: SF Mono, Menlo, monospace)
FONT SIZE:     18px (adjust per image to fit content)
LINE HEIGHT:   1.6
```

### Color Palette

```
TEXT (default):     #c9d1d9  (light gray body text)
GREEN ACCENT:       #41E98D  (primary brand — links, selections)
LIGHT GREEN:        #6DF0A8  (operators, tags, + diff lines)
SOFT GREEN:         #98c379  (strings, added content)
PURPLE:             #B4A0FF  (highlights, special elements)
CYAN:               #5cc9df  (keywords)
ORANGE:             #ffb366  (classes, warnings, variables)
COMMENT GRAY:       #5c6370  (comments, muted text, italic)
MUTED TEXT:         rgba(255, 255, 255, 0.5)
DELETED/RED:        #e06c75  (- diff lines, errors)
```

### Decorative Elements

```
LANGUAGE LABEL:    top-left, 10px, uppercase, letter-spacing 0.08em, #5c6370
WATERMARK:         "self.md" bottom-right, 10px, #5c6370, 40% opacity
GRID OVERLAY:      optional — subtle 60px grid lines at rgba(65,233,141,0.04)
GREEN GLOW:        optional — subtle radial gradient from top-right corner
                   rgba(65,233,141,0.08) fading to transparent
```

### LinkedIn Image Dimensions

```
SQUARE:     1080 × 1080 px  (default, works in all feeds)
PORTRAIT:   1080 × 1350 px  (more real estate, good for long content)
```

---

## DAY 1 — Incident Report {#day-1}

**Dimensions:** 1080 × 1350 (portrait — content is tall)
**Language label:** `INCIDENT REPORT`
**Font size:** 17px

### Exact Text

```
[INCIDENT REPORT]
date: 2024
severity: critical
system: ray.svitla.os

event:
  7-figure net worth → insolvent
  
root cause:
  not crypto. not scams. not bad trades.
  context switching.

diagnosis:
  7 parallel builds running.
  called it "strategy."
  it was avoidance with a flight itinerary.

cascade:
  fragmentation → latency → nothing ships
  → cashflow gaps → debt spiral
  → cognitive overload → wider gaps

patch applied:
  3-node constraint.
  add a project → kill a project.
  no exceptions.

status: recovering.
uptime: 71% and climbing.
```

### Color Mapping

| element | color | note |
|---------|-------|------|
| `[INCIDENT REPORT]` | #ffb366 (orange) | bold, slightly larger (20px) |
| `date:` `severity:` `system:` `event:` etc. | #5cc9df (cyan) | field labels |
| `critical` | #e06c75 (red) | severity highlight |
| `ray.svitla.os` | #B4A0FF (purple) | system name |
| all values | #c9d1d9 (default gray) | |
| `3-node constraint` | #41E98D (green accent) | the key concept — make it glow |
| `71%` | #6DF0A8 (light green) | positive number |

### Design Notes
- the `→` arrows in the cascade section should form a visual waterfall — each indented slightly
- consider a subtle pulsing green dot next to "status: recovering" to suggest a live system
- this is the SERIES OPENER image. it sets the visual language for all 10 images. get this right first.

---

## DAY 2 — Git Diff {#day-2}

**Dimensions:** 1080 × 1350 (portrait — diff is tall)
**Language label:** `DIFF`
**Font size:** 16px

### Exact Text

```diff
- governance OS 2.0 (nation-state)
+ governance OS 3.0 (composable)

- source: partially open ("constitution")
- good luck submitting a pull request
+ source: forkable modules
+ anyone can submit, fork, or deploy

- user accounts: "citizenship"
- onboarding: birth
- offboarding: difficult and costly
+ identity: self-custodied keys
+ onboarding: opt-in
+ offboarding: your choice

- upgrade path: revolution or civil war
+ upgrade path: fork

- annual overhead: $18 trillion
- moat: monopoly on violence
+ overhead: TBD
+ moat: none needed

# reviewed by: nobody
# merged by: history
# rollback: not supported
```

### Color Mapping

| element | color | background |
|---------|-------|------------|
| all `- ` lines | #e06c75 (red) | rgba(224, 108, 117, 0.08) subtle red bg |
| all `+ ` lines | #98c379 (soft green) | rgba(152, 195, 121, 0.08) subtle green bg |
| `# ` comment lines | #5c6370 (comment gray) | none |
| `-` and `+` symbols | same as line but bold | |

### Design Notes
- this is a DIFF. the red/green contrast IS the message. make it prominent.
- each `-`/`+` pair should be visually grouped with slight spacing between groups
- the `#` comment lines at the bottom should feel like afterthoughts — smaller, grayer, set apart by extra spacing
- consider a thin vertical green line on the left margin (like GitHub's diff view)

---

## DAY 6 — Python Code {#day-6}

**Dimensions:** 1080 × 1350 (portrait)
**Language label:** `PYTHON`
**Font size:** 15px (code is dense)

### Exact Text

```python
class NationState:  # in production since 1648. no tests.
    def defend(self, threat):
        if threat.type == "crypto":
            return self.regulate(threat)
        if threat.type == "DAO":
            return self.regulate(threat)
        if threat.type == "network_state":
            return self.regulate(threat)
    
    def regulate(self, threat):
        threat.add_forms(9000)
        threat.require_kyc()
        threat.hire_compliance_officer()
        time.sleep(years=5)
        # threat is now a fintech startup.
        # mission accomplished.
        return threat.now_a_startup()
    
    def handle_revolution(self):
        return "Netflix released a new season"
```

### Color Mapping

| element | color |
|---------|-------|
| `class` `def` `if` `return` | #5cc9df (cyan keywords) |
| `NationState` | #ffb366 (orange class) |
| `self` | #c9d1d9 (default) |
| `threat` `time` | #c9d1d9 (default) |
| `.type` `.add_forms` `.require_kyc` etc. | #c9a0dc (purple methods) |
| `"crypto"` `"DAO"` `"network_state"` `"Netflix..."` | #98c379 (green strings) |
| `==` | #6DF0A8 (light green operator) |
| `(9000)` `(years=5)` | #c9a0dc (purple numbers) |
| `# in production since 1648...` etc. | #5c6370 (comment gray, italic) |
| `(` `)` `:` | #7a8394 (punctuation) |

### Design Notes
- standard Python syntax highlighting. follow self.md's Chroma scheme exactly.
- the comment "in production since 1648. no tests." should be visible but muted — the humor lives in the contrast between the serious class name and the casual comment.
- indentation must be pixel-perfect. this is code. devs will notice.

---

## DAY 9 — Pitch Deck Slide {#day-9}

**Dimensions:** 1080 × 1080 (square — pitch deck slides are square)
**Language label:** `SLIDE 7 / 12`
**Font size:** 16px

### Exact Text

```
TAM

governance.
the largest market on earth.
~$18 trillion annual overhead.
virtually zero innovation in a century.

customer satisfaction:
  — global trust: 52% (Edelman, 2024)
  — U.S. trust: 70% (1960s) → 22% (now)
  — 44% plurality: actively distrust

competitive landscape:
  — incumbent: nation-state (est. ~1648)
  — last major upgrade: representative democracy
  — upgrade method: revolution (high CAC)

new entrants:
  — DAO treasuries: $18.4B
  — charter cities: JaaS
  — modular protocols: AWS for governance

status: pre-revenue.
de-risked by millennia of failed states.
```

### Color Mapping

| element | color |
|---------|-------|
| `TAM` | #ffb366 (orange) bold, 28px |
| `SLIDE 7 / 12` (label) | #5c6370 (muted) |
| section headers (`customer satisfaction:` etc.) | #5cc9df (cyan) |
| `—` bullet dashes | #41E98D (green accent) |
| percentages and numbers | #B4A0FF (purple) |
| `$18 trillion` `$18.4B` | #6DF0A8 (light green) bold |
| `(high CAC)` `(Edelman, 2024)` `(est. ~1648)` | #5c6370 (comment gray) |
| body text | #c9d1d9 (default) |
| `[NEXT SLIDE →]` | bottom-right, #41E98D, 12px |

### Design Notes
- this should feel like a real pitch deck slide rendered in terminal aesthetic
- "TAM" should be the dominant element — big, orange, top-left
- consider a subtle slide navigation indicator at the bottom: `● ● ● ● ● ● ◉ ● ● ● ● ●` where the 7th dot is highlighted green
- the contrast between VC language and terminal aesthetic is the point

---

## DAY 12 — Agent Terminal Log {#day-12}

**Dimensions:** 1080 × 1350 (portrait — conversation is long)
**Language label:** `TERMINAL`
**Font size:** 16px

### Exact Text

```
23:47 [agent] starting research: "one-person 
       state feasibility"
23:47 [agent] estimated duration: 4-6 hours.
       go to sleep.

04:23 [agent] research complete.
04:23 [agent] 47 sources. 3 contradictions found. 
04:23 [agent] key finding: sam altman says single 
       founder → billion-dollar company.
04:23 [agent] adjusted question: how soon until 
       single person → state?
04:24 [agent] a state is not a currency or a discord 
       with better branding.
04:24 [agent] a state = identity + decisions + budget 
       + diplomacy
04:24 [agent] pipeline: personal OS → founder OS → 
       civic OS
04:25 [agent] recommendation: you already have 
       step 1. ship step 2.
04:25 [agent] also: you have 4 unread messages from 
       your wife.
04:25 [agent] priority override: respond to wife 
       first.

07:41 [ray] ...
07:41 [ray] good call on the priority override.
```

### Color Mapping

| element | color |
|---------|-------|
| `23:47` `04:23` `04:24` `04:25` `07:41` | #5c6370 (timestamp gray) |
| `[agent]` | #5cc9df (cyan) |
| `[ray]` | #B4A0FF (purple) |
| `"one-person state feasibility"` | #98c379 (green string) |
| `47 sources` `3 contradictions` | #ffb366 (orange numbers) |
| `priority override` | #e06c75 (red — urgency) |
| `respond to wife first` | #41E98D (green — correct priority) |
| `...` (ray's response) | #c9d1d9 (default) |
| `good call on the priority override.` | #c9d1d9 (default) |
| all other text | #c9d1d9 (default) |

### Design Notes
- the TIME GAP between 23:47 and 04:23 is critical. add extra vertical space there — maybe a subtle dividing line or `...` in comment gray to suggest hours passing.
- the `[agent]` / `[ray]` distinction should be immediately clear — two different speakers, two different colors.
- the "priority override" line should feel like a system alert interrupting the research report
- the final two `[ray]` lines should have a slight delay feel — maybe slightly more spacing between them, suggesting he just woke up

---

## DAY 13 — System Diagnostic {#day-13}

**Dimensions:** 1080 × 1350 (portrait)
**Language label:** `DIAGNOSTIC`
**Font size:** 16px

### Exact Text

```
SYSTEM DIAGNOSTIC: ray.os
date: wednesday
active_contexts: 7

WARNING: cognitive RAM exceeded.
WARNING: context_switching_cost = 23 min per 
         interrupt (Gloria Mark, 2023)
WARNING: active_guilt_pings this week: 14
WARNING: deep_work_sessions_completed: 0
WARNING: you called this "portfolio strategy"
WARNING: your investors called it 
         "diversification"
WARNING: your wife called it "that thing you do 
         where you're busy but nothing moves"

RECOMMENDATION: 
  reduce active_contexts to ≤ 3
  route everything else to /dev/null
  stop pretending the fan noise is productivity
```

### Color Mapping

| element | color |
|---------|-------|
| `SYSTEM DIAGNOSTIC:` | #5cc9df (cyan) bold |
| `ray.os` | #B4A0FF (purple) |
| `wednesday` | #c9d1d9 (default) |
| `active_contexts: 7` | #e06c75 (red — exceeded) |
| `WARNING:` (each instance) | #ffb366 (orange) bold |
| warning text | #c9d1d9 (default) |
| `23 min` `14` `0` `7` | #e06c75 (red numbers — all bad) |
| `"portfolio strategy"` `"diversification"` | #98c379 (green strings — ironic) |
| `"that thing you do..."` | #98c379 (green string) |
| `(Gloria Mark, 2023)` | #5c6370 (comment gray) |
| `RECOMMENDATION:` | #41E98D (green) bold |
| recommendation text | #c9d1d9 (default) |
| `≤ 3` | #6DF0A8 (light green — the goal) |
| `/dev/null` | #B4A0FF (purple) |

### Design Notes
- the WARNING lines should stack like a system log that's getting increasingly personal
- each WARNING should be on its own line with consistent left alignment
- the escalation from technical ("cognitive RAM") to personal ("your wife called it...") should feel like the diagnostic is becoming self-aware
- RECOMMENDATION section should feel like a relief after the wall of warnings — slightly more spacing above it

---

## DAY 16 — Support Ticket {#day-16}

**Dimensions:** 1080 × 1350 (portrait)
**Language label:** `SUPPORT TICKET`
**Font size:** 16px

### Exact Text

```
SUPPORT TICKET #00000001
submitted by: Anya
subject: identity not found

description:
  fled conflict zone. crossed border.
  state-issued identity no longer recognized.
  
current status in OS 2.0: ghost.
  cannot open bank account.
  cannot rent apartment.
  cannot prove she exists.

proposed solution (OS 3.0):
  identity = self-custodied cryptographic keys
  proof-of-humanity verified on-chain
  payments, reputation, access
  no permission required
  
ticket status: open since 1951.
assigned to: nobody.
priority: "we'll get back to you."
escalation path: post about it on LinkedIn.
                  oh wait.
```

### Color Mapping

| element | color |
|---------|-------|
| `SUPPORT TICKET #00000001` | #ffb366 (orange) bold, 20px |
| `submitted by:` `subject:` field labels | #5cc9df (cyan) |
| `Anya` | #B4A0FF (purple) — she's a person, not a data point |
| `identity not found` | #e06c75 (red) |
| `description:` | #5cc9df (cyan) |
| description text | #c9d1d9 (default) |
| `ghost.` | #e06c75 (red) bold |
| `cannot` (each instance) | #e06c75 (red) |
| `proposed solution (OS 3.0):` | #41E98D (green) |
| solution text | #98c379 (soft green — hope) |
| `open since 1951.` | #e06c75 (red) |
| `nobody.` | #e06c75 (red) |
| `"we'll get back to you."` | #5c6370 (comment gray — bitter) |
| `escalation path:` | #5cc9df (cyan) |
| `post about it on LinkedIn. oh wait.` | #5c6370 (comment gray — humor as cope) |

### Design Notes
- the ticket format should feel like an actual support system — think Zendesk or Jira but stripped to monospace
- the emotional weight is in the contrast: bureaucratic format, human crisis
- `ghost.` should stand out. maybe a subtle red glow behind it.
- the "escalation path" humor at the end needs to feel like gallows humor, not flippancy. the gray color helps — it reads as an aside.
- consider a subtle "1 of 89.3M" in the top-right corner (approximate global displaced persons) — or omit if it feels like data decoration

---

## DAY 18 — Git Commit Message {#day-18}

**Dimensions:** 1080 × 1080 (square)
**Language label:** `GIT COMMIT`
**Font size:** 16px

### Exact Text

```
commit 4a7f2e1
Author: ray <ray@self.md>
Date:   Thu Mar 19 2026

  kill skill store from MVP.

  reason: can't build it well in 2 weeks. 
  shipping it badly trains users to expect 
  something we can't maintain.
  
  replacing with: context export from existing 
  sources. less exciting. more honest.
  
  nobody will write a LinkedIn post about this 
  decision. there's no framework for "i cut the 
  interesting thing and kept the boring thing."
  
  but this is the entire job.
  
  files changed: 14
  lines removed: 2,847
  dopamine cost: significant
```

### Color Mapping

| element | color |
|---------|-------|
| `commit` | #5cc9df (cyan keyword) |
| `4a7f2e1` | #ffb366 (orange hash) |
| `Author:` `Date:` | #5cc9df (cyan) |
| `ray` | #B4A0FF (purple) |
| `<ray@self.md>` | #5c6370 (gray — email) |
| `Thu Mar 19 2026` | #c9d1d9 (default) |
| commit message body | #c9d1d9 (default) |
| `"i cut the interesting thing..."` | #98c379 (green string) |
| `files changed: 14` | #c9d1d9 |
| `lines removed: 2,847` | #e06c75 (red — deletions) |
| `dopamine cost: significant` | #ffb366 (orange — not a real git field, that's the joke) |

### Design Notes
- this should look exactly like `git log --format=full` output
- the commit hash should be truncated (7 chars) like real git
- the `ray@self.md` email is subtle brand placement — make it visible but not highlighted
- the joke is that "dopamine cost" is formatted identically to "files changed" and "lines removed" — as if it's a standard git metric. don't differentiate it visually. the uniformity IS the humor.

---

## DAY 26 — Man Page {#day-26}

**Dimensions:** 1080 × 1350 (portrait — this is the longest formatted post)
**Language label:** `MAN PAGE`
**Font size:** 14px (dense content — needs to fit)

### Exact Text

```
NATION-STATE(1)       LEGACY SYSTEMS       NATION-STATE(1)

NAME
    nation-state — monolithic governance runtime
    
SYNOPSIS
    nation-state [--constitution FILE] [--citizens N]
    
DESCRIPTION
    On-premise governance suite, est. ~1648. Source 
    partially open. User accounts ("citizenship") 
    provisioned at birth. Off-boarding difficult. 
    Upgrade path: revolution (DANGEROUS) or civil 
    war (DEPRECATED).
    
    Running 18th-century algorithms on 21st-century 
    hardware. Known to panic under load. Panics 
    historically labeled "revolutions."

OPTIONS
    --democracy     experimental. requires constant
                    manual intervention. see BUGS.
    --fork          exit current instance. may void
                    warranty and passport.
    --protest       rate-limited. see local laws.
    
BUGS
    Vendor lock-in by design. Pull requests to 
    constitution require mass mobilization. 
    Response time measured in decades.
    
SEE ALSO
    network-state(3), dao(7), charter-city(5)
    
HISTORY
    Approximately 300 years without major refactor.
    Maintenance cost: $18T/year.
    No maintainer on call.
```

### Color Mapping

| element | color |
|---------|-------|
| `NATION-STATE(1)` header (both) | #c9d1d9 bold, 16px |
| `LEGACY SYSTEMS` center header | #5c6370 (gray) |
| `NAME` `SYNOPSIS` `DESCRIPTION` `OPTIONS` `BUGS` `SEE ALSO` `HISTORY` | #ffb366 (orange section headers) bold |
| `nation-state` (in NAME) | #B4A0FF (purple) |
| `--constitution` `--citizens` `--democracy` `--fork` `--protest` | #41E98D (green flags) |
| `FILE` `N` | #5cc9df (cyan arguments) |
| `(DANGEROUS)` | #e06c75 (red) |
| `(DEPRECATED)` | #e06c75 (red) |
| `network-state(3)` `dao(7)` `charter-city(5)` | #B4A0FF (purple references) |
| `$18T/year` | #6DF0A8 (light green) |
| `No maintainer on call.` | #e06c75 (red — the kicker) |
| all other body text | #c9d1d9 (default) |

### Design Notes
- this MUST look like an actual Unix man page. the three-column header, the section formatting, the indentation — all must be accurate.
- the OPTIONS section is the humor payload. `--protest rate-limited. see local laws.` is the punchline. it should be formatted identically to `--democracy` and `--fork` — the joke is in the uniformity.
- `SEE ALSO` references to `network-state(3)`, `dao(7)`, `charter-city(5)` imply a whole ecosystem of alternative governance man pages. don't explain this. let the devs get it.
- `No maintainer on call.` as the last line should feel like a system status that's both funny and terrifying.
- this is the SIGNATURE visual piece. it's the one people will screenshot most. prioritize quality.

---

## DAY 29 — Field Notes Header {#day-29}

**Dimensions:** 1080 × 1080 (square — only the header block)
**Language label:** `FIELD NOTES`
**Font size:** 20px (less text, bigger font)

### Exact Text

```
FIELD NOTES: founder OS sessions
duration: 2 months
participants: [redacted]
finding: OS scales. vibes don't.
```

### Color Mapping

| element | color |
|---------|-------|
| `FIELD NOTES:` | #ffb366 (orange) bold, 24px |
| `founder OS sessions` | #c9d1d9 (default) |
| `duration:` `participants:` `finding:` | #5cc9df (cyan labels) |
| `2 months` | #c9d1d9 (default) |
| `[redacted]` | #e06c75 (red, with a black bar overlay effect) |
| `OS scales.` | #41E98D (green — positive) |
| `vibes don't.` | #e06c75 (red — negative) |

### Design Notes
- this is just the header block. 4 lines. make them BIG and bold.
- `[redacted]` could have a redaction-bar visual effect — the text visible through a semi-transparent dark overlay, like a classified document
- the split color on the finding line ("OS scales." in green, "vibes don't." in red) creates the visual punchline
- this image accompanies a longer text post — it's the hook image, not the full content
- most white space of any image. let it breathe. the confidence of the formatting IS the statement.

---

## Production Notes

### File Naming Convention
```
linkedin-day-XX-[format].png
linkedin-day-01-incident-report.png
linkedin-day-02-git-diff.png
linkedin-day-06-python.png
linkedin-day-09-pitch-deck.png
linkedin-day-12-agent-log.png
linkedin-day-13-diagnostic.png
linkedin-day-16-support-ticket.png
linkedin-day-18-git-commit.png
linkedin-day-26-man-page.png
linkedin-day-29-field-notes.png
```

### Export Settings
- Format: PNG (for text clarity — no JPEG compression artifacts on monospace)
- Resolution: 2x (2160 × 2160 or 2160 × 2700) for retina displays
- Color space: sRGB
- Compression: maximum quality

### Accessibility
- every image should have alt text prepared (= the exact text content of the image)
- LinkedIn supports alt text on images — fill it in every time
- the alt text ensures screen readers can access the code-formatted content

### Batch Production Recommendation
1. create a master template in Figma/Sketch with the self.md styling
2. produce Day 1 first — it's the series opener and sets the standard
3. produce Day 26 (man page) second — it's the most complex and the signature piece
4. batch the remaining 8 after the template is locked
5. QA: check every image on mobile at 375px width — text must still be readable
6. generate all 10 BEFORE series launch day. no scrambling mid-series.

### self.md Brand Consistency Notes
- the green (#41E98D) is the primary brand color. it should appear in every image but never dominate — it's an accent, not a background.
- the purple (#B4A0FF) is for interactive/special elements. in images, use it for names, references, and system identifiers.
- the overall feeling should be: "this is a screenshot from a system that actually exists." not decorative. functional. beautiful by accident.
- no gradients on text. no drop shadows on text. no glow effects on text. the self.md aesthetic is flat, monospace, and precise.

---

*10 images. 1 design language. 0 carousels.*
