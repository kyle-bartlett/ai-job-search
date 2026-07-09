# Search Queries for Job Scraper

<!-- Kyle Bartlett — US, remote-only, AI-leadership search.
     NOTE: the repo's built-in scraper CLI tools target Danish portals (jobindex.dk etc.),
     which do not apply here. Use LinkedIn + Google site-searches + US boards below. -->

## Search Sites

Primary (US / remote):
- **linkedin.com/jobs** — filter: Remote, United States
- **wellfound.com** (AngelList Talent) — startups / founding-AI roles
- **google.com search** — `site:` filters + "remote" for company career pages
- **ycombinator.com/jobs** (Work at a Startup) — seed–Series B AI roles
- **indeed.com** — broad US coverage, filter Remote

Secondary:
- Direct Google `site:boards.greenhouse.io` / `site:jobs.lever.co` / `site:job-boards.ashbyhq.com` searches for AI-forward companies.

## Query Categories

Every query is **remote-first**. Pair titles with: `remote`, `AI strategy`, `adoption`, `enablement`, `change management`, `automation`, `agentic`, `LLM`.

### Priority 1: AI Enablement & Adoption Leadership (exact wheelhouse)

```
site:linkedin.com/jobs "AI Enablement Lead" remote
site:linkedin.com/jobs "Director of AI Adoption" remote
site:linkedin.com/jobs ("AI Enablement" OR "AI Adoption") (Lead OR Director OR Manager) remote
site:boards.greenhouse.io "AI enablement" remote
"AI adoption lead" OR "AI enablement manager" remote change management -senior director
```

### Priority 2: Head of AI / AI Lead / AI Program (own the function)

```
site:linkedin.com/jobs "Head of AI" remote (startup OR "Series A" OR "Series B")
site:linkedin.com/jobs "AI Lead" remote
site:linkedin.com/jobs ("AI Program Manager" OR "AI Platform Manager") remote
site:jobs.lever.co ("Head of AI" OR "Founding AI") remote
"first AI hire" OR "founding AI" OR "build the AI function" remote
```

### Priority 3: Applied / Agentic AI Build + Strategy (hands-on lead)

```
site:linkedin.com/jobs "Applied AI Lead" remote
site:linkedin.com/jobs ("Agentic" OR "LLM" OR "multi-agent") (Lead OR Architect OR "Solutions") remote
site:linkedin.com/jobs "AI Solutions Lead" remote consulting
site:job-boards.ashbyhq.com ("Applied AI" OR agentic) remote
```

### Priority 4: Adjacent — Automation / Innovation / Emerging Tech (wider net)

```
site:linkedin.com/jobs "Director of Automation" remote
site:linkedin.com/jobs ("Emerging Technology Lead" OR "Innovation Manager") AI remote
site:linkedin.com/jobs "AI Transformation" (Lead OR Director OR Consultant) remote
site:linkedin.com/jobs "AI Product Manager" remote
```

## Location Filter

- **Remote (US) — required.** This is a hard filter, not a preference.
- Reject: on-site, hybrid, or "remote but must be in [city] X days/week."
- Reject: roles requiring relocation.
- International-remote is fine only if fully remote and US-timezone-friendly.

## Compensation Filter

- Target $250k+ total comp ($275-350k preferred). Flag anything materially below as low-priority.
- If comp isn't listed, include but note "comp unknown — verify before applying."

## Seniority Filter

- **Green:** "lead / build / grow a small team," "player-coach," "first AI hire," no hard "X years managing PMs/managers."
- **Reach (flag):** "8-10 years formally managing managers/PMs," "manager of managers," VP/Senior Director requiring long management tenure.

## Date Filter

Only include jobs posted within the last 14 days, or with an open application deadline. If a posting date can't be determined, include it but flag "date unknown".

## Adapting Queries

If Kyle specifies a focus (e.g. "/scrape enablement" or "/scrape founding"), pull that category's queries plus 2-3 custom queries for the focus.
