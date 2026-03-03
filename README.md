# Senior Software Engineer — Recruiter Screening Guide

---

## How to Use This Guide

```
STEP 1 → Run Pre-Screen Checklist (2 min)   — hard eliminators, ask before anything else
STEP 2 → Ask Knockout Questions Q1–Q3       — any ❌ = end screen + do not advance
STEP 3 → Ask Core Questions Q4–Q10          — score each, note gaps for technical panel
STEP 4 → Ask Closing Questions Q11–Q12      — assess mindset and fit
STEP 5 → Fill Scorecard + make decision
```

**Score key:** 

✅ Strong — candidate gave a specific, confident answer with real examples

⚠️ Partial — answered but was vague, generic, or hedged too much

❌ Weak — could not answer, gave a textbook definition only, or showed a red flag

---

## STEP 1 — Pre-Screen Checklist (ask these first, ~2 min)

> These are binary gates. If any answer is **No**, politely end the screen — do not proceed.

| Gate | Question to Ask | Pass | Fail |
|------|-----------------|------|------|
| **Years of experience** | "This role requires 5+ years of commercial software development. Can you confirm your total years of paid professional experience building production software?" | Confirms 5+ years | < 5 years or only freelance/side projects |
| **PHP production experience** | "This is primarily a PHP/Laravel role — roughly 80% of the codebase. Have you worked with PHP and Laravel in a commercial production environment?" | Yes, with specifics | No PHP experience or only personal projects |
| **Right to work / location** | *(insert your org's standard eligibility check)* | Eligible | Not eligible |

---

## STEP 2 — Knockout Questions (Any ❌ = Do Not Advance)

> These three questions are your strongest filters. A weak answer here means the candidate does not meet the seniority bar — do not be tempted to advance anyway.

---

### Q1 — Real PHP/Laravel Production Experience
**Time budget: ~5 min**

**Ask:** *"Tell me about a PHP or Laravel application you've personally owned or had significant responsibility for. How large was the codebase, how many users did it serve, and what was your specific role?"*

**Why this matters:** Filters out candidates who have used Laravel only on tutorials, side projects, or in a very junior/supporting capacity. Seniority requires ownership at real scale.

| What you're listening for | What should concern you |
|---------------------------|------------------------|
| Names a real company/product (doesn't have to be public) | Only mentions personal/hobby projects |
| Gives concrete scale signals — user numbers, traffic, team size | Says "we" for everything, can't describe their own contribution |
| Describes evolution of the system over time, not just initial build | Claims 5+ years but only describes one small feature |
| Shows they understand the business impact of what they built | Gets defensive or vague when asked follow-up questions |

**Follow-up if vague:** *"What was the single hardest technical decision you made on that project — and what would you do differently now?"*

---

### Q2 — Production Incident, Debugging & Performance Under Pressure
**Time budget: ~5 min**

**Ask:** *"Tell me about the worst production incident you've been directly involved in on a PHP or Laravel application. Walk me through how you detected it, how you diagnosed the root cause, and what you did to resolve it and prevent recurrence."*

**Why this matters:** Seniority is proven under fire, not in ideal conditions. This question simultaneously tests debugging skills, methodical thinking, tooling knowledge, performance awareness, and ownership. A candidate who has never owned a production problem is not a senior engineer.

| What you're listening for | What should concern you |
|---------------------------|------------------------|
| Describes a **structured triage process**: alerts/logs → hypothesis → isolation → fix — not random changes | Stumbles to recall any production incident they were personally involved in |
| Names **specific tooling** used to investigate: Laravel Telescope, Xdebug, Blackfire, Sentry, Datadog, New Relic, MySQL slow query log | "I just checked the code and found it" — no systematic approach, no tooling |
| Can identify the **root cause category**: N+1 query, memory leak, race condition, cache stampede, deadlock, queue backup, misconfigured index | Describes a very minor bug (typo, wrong variable) as their "worst incident" |
| Describes a **performance angle** — e.g. a query that worked fine at low volume and only broke at scale | Only fixed the symptom; no follow-up to prevent recurrence |
| Mentions **post-incident actions**: added monitoring/alerting, wrote a runbook, added a regression test, held a blameless post-mortem | Shows panic or blame rather than structured, calm problem-solving |
| Gives **before/after metrics** if performance-related — query time, response time, error rate, queue depth | Cannot quantify the impact of the incident or the fix |

**Follow-up if vague:** *"What specific tool or log entry gave you the first clue about what was going wrong?"*

**Follow-up if no performance angle mentioned:** *"Has there been a time where performance degraded gradually under load rather than a sudden failure? How did you catch it?"*

---

### Q3 — Tech Stack Adaptability (Attitude Filter)
**Time budget: ~4 min**

**Ask:** *"This role is 80% PHP/Laravel in a mature, established codebase — not a greenfield rewrite. How do you feel about that, and what's your experience working in existing codebases rather than starting fresh?"*

**Why this matters:** The single most common failure mode for this hire is an engineer who privately considers PHP beneath them and will chafe against the codebase from day one. This question surfaces that attitude before it becomes a retention issue.

| What you're listening for | What should concern you |
|---------------------------|------------------------|
| Expresses genuine comfort or interest in established codebases | Says "I prefer greenfield" without any caveat |
| Talks about the *value* of understanding an existing system before changing it | Makes comments like "PHP is outdated" or "I'd want to rewrite everything" |
| Has a real example of improving or navigating a legacy codebase | Shows impatience or dismissiveness when you describe the stack |
| Mentions the 20% Node.js as a plus, not as the only reason they applied | Only excited about the Node.js portion; treats PHP as a burden to endure |

**Follow-up if attitude seems off:** *"If the role ended up being 90% PHP and only 10% Node.js, would that change your interest?"*

> **Hard rule:** A dismissive or negative attitude toward PHP/Laravel here = **automatic Do Not Advance**, regardless of how strong they are technically. We cannot train someone out of that mindset.

---

## STEP 3 — Core Questions (Score Each, Flag Gaps)

> Score each question. Partial answers (⚠️) are acceptable here — flag them for the technical panel to probe deeper.

---

### Q4 — System Design & Architecture Judgment
**Time budget: ~4 min**

**Ask:** *"Tell me about a significant architecture or system design decision you personally made on a PHP/Laravel project — one that had lasting impact on the codebase or team. What options did you consider, and why did you land where you did?"*

**Why this matters:** Seniority means owning decisions, not just implementing them. This question reveals whether the candidate can reason about trade-offs, communicate choices, and learn from outcomes — all critical for someone who will influence a mature, high-traffic codebase.

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Describes trade-offs explicitly (performance vs. maintainability, speed vs. correctness, flexibility vs. simplicity) | Can describe a design decision but only from a single angle | "Someone else made that call" — cannot name a decision they personally owned |
| Considered non-technical factors: team capability, time constraints, future extensibility | Has strong opinions but has never had to defend or document them to others | Has only ever implemented decisions handed down by others |
| Shows honest awareness of the risks or downsides of their choice | Treats their chosen solution as objectively correct with no acknowledged trade-offs | Cannot articulate a concrete alternative they evaluated and rejected |

**Follow-up:** *"Looking back, was it the right call? What would you do differently now?"*

---

### Q5 — Performance & Scalability
**Time budget: ~4 min**

**Ask:** *"Walk me through a time you identified and fixed a performance problem in a PHP application or database query. What was the impact before and after?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| **Starts with measurement** — they profiled or queried logs before fixing | Jumps straight to "I added caching" with no explanation of how they found the problem | Cannot describe a single performance fix |
| Names specific techniques: eager loading, indexing, caching, queue offloading | Answer is very high-level / theoretical with no concrete numbers | Has never worked on a performance issue |
| Gives before/after numbers (query time, page load, throughput) | Can describe the fix but not the root cause | Confuses performance with just "making code cleaner" |

**Follow-up:** *"How did you confirm the fix actually worked and didn't introduce a regression?"*

---

### Q6 — Testing Practices
**Time budget: ~3 min**

**Ask:** *"What does your testing setup look like in a typical PHP/Laravel project? What types of tests do you write, and how are they hooked into your CI pipeline?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Distinguishes unit tests, feature/integration tests, and E2E | Only mentions unit tests or only mentions manual QA | Has never written automated tests |
| Names PHPUnit or Pest; mentions Laravel's HTTP testing | Knows the concepts but hasn't set up a pipeline themselves | Testing is treated as optional or someone else's job |
| Describes CI gates — tests must pass before merging | Has written tests but they're not run automatically | "QA handles that" with no personal involvement |

**Follow-up:** *"What's a type of code that's notoriously hard to test, and how do you handle it?"*

---

### Q7 — Database Design & Migrations
**Time budget: ~3 min**

**Ask:** *"Tell me about a complex database schema you've designed. How did you handle schema migrations on a live, running system without downtime?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Mentions backward-compatible migrations (add column before removing old one) | Has run migrations but never on a live system under traffic | Has only ever run migrations in development |
| Aware of risks: locking, long-running queries, foreign key constraints | Knows the theory but no real production migration story | Claims senior experience but has never thought about zero-downtime deploys |
| Understands indexing trade-offs (read vs. write performance) | Treats all migrations as the same regardless of risk | |

**Follow-up:** *"What would you do differently if a migration needed to change a column that had millions of rows?"*

---

### Q8 — Code Quality & Git Workflow
**Time budget: ~3 min**

**Ask:** *"Walk me through how your last team handled code reviews and branching. What made a PR get rejected?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Describes a real review culture — not just rubber-stamping | Reviews happened but were mostly style/nitpick focused | "We pushed directly to main" or no PR culture |
| Can give a specific example of a PR they rejected or that was rejected and why | Has done reviews but never enforced a standard | Review was a formality with no real gate |
| Mentions CI checks, static analysis (PHPStan, Psalm, Laravel Pint) | Relies only on human review, no automated checks | |

---

### Q9 — Node.js, TypeScript & React Honesty Check
**Time budget: ~3 min**

**Ask:** *"About 20% of this role involves Node.js, TypeScript, and React. On a scale of 1–10, how would you honestly rate yourself in each, and what's the most complex work you've done commercially in that part of the stack?"*

> **Recruiter note:** You are NOT testing for expertise here. You are testing for **honesty and growth mindset**. A candidate who says "Node 6, TypeScript 5, React 4 — here's what I've done and here's how I'd close the gap" is far more valuable than one who claims across-the-board 9s and then stumbles on a follow-up.

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Honest, differentiated self-ratings with concrete reasoning for each area | Claims high proficiency across the board but can only describe basic CRUD APIs or tutorial-level React | Dismisses the Node.js/TypeScript/React work as irrelevant or refuses to engage with learning it |
| Describes real async patterns in Node.js: promises, async/await, event-driven code | Equates "I've used npm" or "I've written a few React components" with meaningful proficiency | Claims expert level but cannot describe what the event loop does or what TypeScript generics are for when probed |
| For TypeScript: distinguishes between using types for basic annotations vs. leveraging the type system (generics, utility types, discriminated unions) | Self-ratings with no supporting evidence either way | |
| Shows a concrete plan or genuine enthusiasm for closing any gap | | |

**Follow-up if they claim high Node.js proficiency:** *"What's the difference between Node.js's concurrency model and PHP's, and when would you choose one over the other?"* *(You don't need to know the answer — you're listening for confidence and depth.)*

**Follow-up if they claim strong TypeScript:** *"How do you handle typing third-party libraries that ship without type definitions?"* *(Again, listen for specificity, not a perfect answer.)*

---

### Q10 — Security Awareness
**Time budget: ~3 min**

**Ask:** *"What are the top security risks you actively guard against when building PHP APIs, and can you give me a real example of catching or fixing a vulnerability?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Names specific vulnerabilities: SQL injection, XSS, CSRF, mass assignment, IDOR (Insecure Direct Object Reference), broken authentication | Gives only generic "security is important" statements | Has never thought about security at code level |
| Knows Laravel's built-in protections AND their limits (e.g. Eloquent doesn't make you immune to mass assignment if `$guarded` is misused; CSRF middleware doesn't cover stateless APIs) | Relies entirely on "Laravel handles it automatically" | Cannot name a single vulnerability type |
| For APIs specifically: mentions authentication token hygiene, rate limiting, input validation at the boundary, and avoiding over-exposing data in responses | Theoretical knowledge only, no real example | |
| Has a real story — something caught in a review, audit, or pen test | | |

---

## STEP 4 — Closing Questions (Mindset & Fit)

---

### Q11 — Handling a Brownfield Codebase
**Time budget: ~3 min**

**Ask:** *"Imagine you join and the first thing you're asked to do is add a feature to a part of the codebase you find messy or poorly structured. What's your approach?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Talks about understanding the code's intent before judging it | Immediately talks about rewriting it | "I'd refuse to touch it until it was cleaned up" |
| Balances delivering the feature with incremental improvement (boy scout rule) | Would deliver the feature but ignore any improvement opportunity | Shows contempt for existing code or past engineers |
| Raises the trade-off conversation with the team/product owner | Would spend weeks refactoring without aligning with stakeholders | |

---

### Q12 — Motivation & Long-Term Fit
**Time budget: ~3 min**

**Ask:** *"Why does this specific role appeal to you — not just the company, but the nature of the work: a mature PHP product, gradual modernisation, high-traffic scale?"*

| ✅ Listen for | ⚠️ Flag if | ❌ Stop if |
|--------------|-----------|-----------|
| Articulates genuine interest in ownership, scale, or impact | Generic answer about "exciting technology" or "career growth" | Only interested because of the Node.js/TypeScript 20% |
| Has done research on the product or company | Has not looked at what the product does | Sees the role as a stepping stone to something "better" |
| Can describe what they'd contribute, not just what they'd get | Focuses entirely on what they want to learn | Treats PHP at this scale as beneath their ambitions |

---

## STEP 5 — Scorecard

> Complete this immediately after the call while memory is fresh.

**Candidate name:** _________________________ &nbsp;&nbsp; **Date:** _______________ &nbsp;&nbsp; **Interviewer:** ___________________

### Pre-Screen Gates
| Gate | Pass ✅ | Fail ❌ |
|------|--------|--------|
| 5+ years commercial experience | | |
| PHP/Laravel production experience | | |
| Right to work / eligibility | | |
| Notice period acceptable | | |

> **If any gate = ❌, do not proceed. Mark as "Screen Fail – Eligibility."**

---

### Knockout Questions
| # | Question | Score | Key evidence heard |
|---|----------|-------|--------------------|
| Q1 | PHP/Laravel production ownership | ✅ / ⚠️ / ❌ | |
| Q2 | Production incident, debugging & performance | ✅ / ⚠️ / ❌ | |
| Q3 | Tech stack adaptability & attitude | ✅ / ⚠️ / ❌ | |

> **If any Knockout = ❌, mark as "Screen Fail – Seniority/Fit." Do not advance.**

---

### Core Questions
| # | Question | Score | Gaps to flag for technical panel |
|---|----------|-------|----------------------------------|
| Q4 | System design & architecture | ✅ / ⚠️ / ❌ | |
| Q5 | Performance & scalability | ✅ / ⚠️ / ❌ | |
| Q6 | Testing practices | ✅ / ⚠️ / ❌ | |
| Q7 | Database design & migrations | ✅ / ⚠️ / ❌ | |
| Q8 | Code quality & Git | ✅ / ⚠️ / ❌ | |
| Q9 | Node.js, TypeScript & React honesty | ✅ / ⚠️ / ❌ | |
| Q10 | Security awareness | ✅ / ⚠️ / ❌ | |

**Core score:** ___ ✅ out of 7

---

### Closing Questions
| # | Question | Score | Notes |
|---|----------|-------|-------|
| Q11 | Brownfield codebase approach | ✅ / ⚠️ / ❌ | |
| Q12 | Motivation & long-term fit | ✅ / ⚠️ / ❌ | |

---

## Decision Framework

```
All 4 Pre-Screen gates = Pass?          → NO  = Screen Fail – Eligibility
Any Knockout (Q1–Q3) = ❌?             → YES = Screen Fail – Seniority/Fit
Q3 attitude = ❌ (dismissive of PHP)?  → YES = Screen Fail – Culture Fit (hard rule)

Core score 6–7 ✅ + Closing ✅✅       → STRONG ADVANCE — fast-track technical round
Core score 4–5 ✅ + Closing ✅         → CONDITIONAL ADVANCE — share flagged gaps with technical panel
Core score 3 ✅ or fewer               → HOLD — discuss with hiring manager before advancing
```

| Decision | Next action |
|----------|-------------|
| **Strong Advance** | Book technical round; no special notes needed |
| **Conditional Advance** | Book technical round; send "areas to probe" note to technical interviewer |
| **Hold** | Discuss with hiring manager — may suit a different level or team |
| **Screen Fail** | Send rejection; log reason for pipeline reporting |

---

## Quick Reference — Recruiter Cheat Sheet

> Print or keep open during the call.

| # | Topic | One thing that guarantees ✅ | One thing that guarantees ❌ |
|---|-------|-----------------------------|-----------------------------|
| Q1 | PHP ownership | Describes a real product at real scale with their name on it | Only side projects or "I was part of the team" |
| Q2 | Production incident | Structured triage story + names a specific tool that cracked it | Cannot recall a real incident; no tooling; "I just tried things" |
| Q3 | Stack attitude | Expresses genuine comfort with PHP/Laravel | Any dismissiveness toward PHP |
| Q4 | System design | Describes a real decision with explicit trade-offs they personally owned | "Someone else decided that" or solution presented as obviously correct with no alternatives |
| Q5 | Performance | Started with measurement before fixing | Immediately jumped to "add caching" |
| Q6 | Testing | At least unit + feature tests running in CI | No automated tests or "QA handles it" |
| Q7 | Database | Knows migrations can be risky on live systems | Has only ever run migrations in dev |
| Q8 | Git/code quality | Can describe a PR that was actually rejected | "We pushed to main" |
| Q9 | Node.js / TS / React | Honest, differentiated ratings per technology + concrete example or clear plan to grow | Claims expert across the board but stumbles on async patterns, TS type system, or React specifics |
| Q10 | Security | Names at least 2 specific vulnerability types (bonus: mentions IDOR or API-specific risks) | "Laravel handles security for me" |
| Q11 | Brownfield | Deliver first, improve incrementally | "I'd want to rewrite this" |
| Q12 | Motivation | Excited about ownership at scale in PHP | Only here for the Node.js work |

---

*Role: Senior Software Engineer · Stack: PHP/Laravel (80%) + Node.js/TypeScript (20%) · Last updated: March 2026*