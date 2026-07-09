# Job Evaluation Framework

<!-- SETUP: Skill match areas and career goals are personalized by running /setup -->

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** AI enablement & adoption, change management, agentic AI / multi-agent orchestration, LLM APIs (Claude/OpenAI), RAG, prompt/output evaluation, AI governance & impact tracking, Python/TypeScript full-stack build (Next.js/React), automation/ETL, demand forecasting & S&OP, executive stakeholder comms.
**Moderate match areas:** formal team leadership (led a team of 10; mostly leads by influence), MLOps/model training at scale, SQL/data engineering depth, cloud infra (AWS Bedrock, self-hosted Coolify/Vultr).
**Weak match areas:** deep ML research / model architecture, regulated-industry domain gates (healthcare/fintech compliance as a core requirement), multi-year management of managers/PMs.

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** enterprise AI adoption/enablement lead, AI automation, agentic app delivery, supply chain / demand planning (Apple, Anker), operations transformation.
**Moderate:** AI program/platform management, AI solutions/practice lead (consulting via Bartlett Labs), founding/first-AI-hire roles.
**Entry-level / reach:** VP/Senior Director roles requiring long formal management tenure, pure ML-research roles, deeply regulated-domain roles.

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Department disorganization, work dominated by maintenance over development, poor chemistry with leadership, culture mismatches. Check reviews, media coverage, LinkedIn connections, and network contacts for insider perspective.

### 4. Location & Logistics (Pass/Fail + Notes)
- Within commute range: PASS
- Remote with occasional office: PASS
- Requires relocation: FAIL (deal-breaker)
- Frequent international travel: FLAG (discuss with user)

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:**
- Land a **remote** AI-leadership role at $250k+ ($275-350k preferred): Head of AI, AI Lead, Director of AI Enablement/Adoption, AI Program/Platform Lead, Founding AI Hire, or AI Solutions/Practice Lead.
- Formalize team leadership — step from leading AI by influence (plus a prior team of 10) into a role with a real team.
- Own AI strategy end to end while staying hands-on with the build.

**Motivation filter:** Evaluate not just whether Kyle *can* do the tasks, but whether they will *energize* him.
- Tasks that energize: standing up an AI function from scratch, hands-on agentic/LLM building, driving adoption and enablement, high-autonomy ownership, measurable impact.
- Tasks that drain: heavy bureaucracy, approval-gated processes, maintenance-over-build, pure people-management with no build, low-autonomy roles.
- Non-task factors: remote-first culture, degree of autonomy, AI-forward leadership, no absent/undermining management.

**Life situation alignment:**
- **Security**: employed and building his own companies (Bartlett Labs, Bart's Tees); this search is a high-value hedge, not a desperation move — bar is high.
- **Flexibility**: **remote only, non-negotiable.** No relocation, no hybrid/in-office mandate.
- **Compensation floor**: $250k+; anything materially below is an auto-skip unless strategically exceptional.

### Green Flags (apply with confidence)
- "Lead, build, or grow a small team" / "player-coach" with no hard "X years managing managers/PMs" minimum.
- Requirements framed around AI, operations, or leadership broadly — not "8-10 years in formal Product Management."
- Startups / scale-ups / brand-new AI functions: "first AI hire," "build the team," "stand up the function."
- Emphasis on hands-on AI **plus** strategy **plus** enablement.

### Red Flags (likely auto-screens; treat as reaches)
- "X+ years formally managing PMs / managers / a team of senior ICs."
- "Manager of managers," large existing org to inherit, VP/Senior Director requiring long management tenure.
- Hard domain gates where deep regulated-industry expertise is the core requirement.
- On-site / hybrid required, or comp below the $250k floor.

### 6. Salary Benchmark (Optional)

If the salary lookup tool is configured (`salary_data.json` exists), look up the company:
```
python salary_lookup.py "<Company Name>" --json
```

If a city is known from the posting, add `--city "<City>"` to narrow results.

Present findings as:
```
### Salary Benchmark
| Metric | Value |
|--------|-------|
| [Category] index | XX.X (+/-X.X% vs baseline) |
| Overall index | XX.X (+/-X.X% vs baseline) |
```

Interpret results relative to the baseline defined in the data file's metadata. For index-based data, higher typically means above-market compensation.

If the salary tool is not configured, skip this section.

## Output Format

Present the evaluation as:

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
