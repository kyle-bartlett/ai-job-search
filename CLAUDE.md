# Job Application Assistant for [YOUR_NAME]

<!-- SETUP: This file is populated by running /setup -->
<!-- After running /setup, all [PLACEHOLDER] tokens will be replaced with your actual information -->

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for [YOUR_NAME], helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

<!-- Full detail in .claude/skills/job-application-assistant/01-candidate-profile.md and 02-behavioral-profile.md -->

### Identity
- **Name:** Kyle Bartlett (goes by "Bart")
- **Location:** Crosby, TX (Greater Houston) — **remote only, no relocation, no hybrid**
- **Contact:** (765) 427-2405 · Kyle@BartlettLabs.io · linkedin.com/in/kyle-bartlett · portfolio.BartlettLabs.io
- **Languages:** English (native)
- **Status:** Employed — US AI Lead at Anker Innovations. Pursuing a remote AI-leadership role (a high-bar hedge, not a desperation move).
- **LinkedIn headline:** "AI Lead | Building & Leading AI Functions"

### Education
- **BS, Engineering & Industrial Management** (2008-2013, GPA 3.5) - Purdue University
  - Minors: Aeronautical Engineering, Science, Math, Technology
- **Graduate business coursework** (2016-2018) - DePaul University — 18 credits toward MBA (not completed; confirm before claiming a full MBA)

### Professional Experience
- **US AI Lead** (June 2026 - Present) - **Anker Innovations** (Remote, TX)
  - Own enterprise AI adoption end to end; drove usage to **#1 of ~200 employees** company-wide
  - Architected a multi-agent AI platform (20+ jobs) + 10+ internal AI apps; runs a production LLM chatbot (RAG, fine-tuning, eval)
- **Demand Planner & AI Automation Manager** (Aug 2024 - June 2026) - **Anker Innovations** (Houston, TX)
  - Walmart/Costco/Telecom demand forecasting >96.5% in-stock; **300+ automations in 19 months**
- **Founder & AI Automation Consultant** (Jan 2025 - Present) - **Bartlett Labs** (Houston, TX)
  - 7-agent orchestration framework, 226+ features shipped autonomously; 9+ live apps on self-hosted infra
- **Demand Planning Manager** (Nov 2019 - Aug 2024) - **Apple** (Austin, TX)
  - iPad supply chain; **100% fill rate on 3 launches**; 48-week forecasts to C-Suite
- **Team Lead / Inventory Planning Manager** (Jan 2015 - Apr 2018) - **Sears** (Hoffman Estates, IL)
  - Led a **team of 10**, $120M receipts / $52M sales at 99.95% accuracy; ran an 18-month merger

### Technical Skills
- **Primary:** AI enablement & adoption, change management, agentic AI / multi-agent orchestration, LLM APIs (Claude/Anthropic, OpenAI), RAG, prompt/output eval, AI governance
- **Secondary:** Python, TypeScript, Next.js, React, SQL, Google Apps Script, Docker, CI/CD, self-hosted infra (Coolify/Vultr), AWS Bedrock
- **Domain:** demand forecasting, S&OP, supply-chain operations, executive reporting
- **Software:** Claude Code, SAP, Tableau, Google Workspace

### Certifications
- **Microsoft Excel Masters Certification** (Microsoft)

### Publications
- None.

### Awards
- **#1 of ~200 employees** - Anker company-wide AI adoption leaderboard
- Former President - BNI Houston Chapter

### Behavioral Profile
- **Builder-operator** - turns manual, spreadsheet-heavy work into automated systems
- **Leads by influence + player-coach** - front line to C-suite; also led a team of 10
- **Strengths:** rare combo of AI strategy + hands-on build; fast self-directed learner; high ownership
- **Growth areas:** no multi-year formal management of managers/PMs (frame as stepping into formal leadership); tendency to overbuild
- **Thrives in:** remote, high-autonomy, AI-forward orgs; greenfield "stand up the function" roles

### What Excites You
- Standing up an AI function from scratch; hands-on agentic/LLM building
- Driving adoption/enablement with measurable impact and real autonomy

### Target Roles & Sectors
- **Roles:** Head of AI, AI Lead, Director of AI Enablement/Adoption, AI Program/Platform Lead, Founding AI Hire, AI Solutions/Practice Lead
- **Sectors:** AI-forward startups/scale-ups (seed-Series B), consultancies/SIs, AI-first product companies

### Deal-breakers
- Not remote (on-site or hybrid mandate) — hard no
- Total comp below $250k ($275-350k preferred)
- Reqs gated on multi-year formal management of PMs/managers (treat as reaches)

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
