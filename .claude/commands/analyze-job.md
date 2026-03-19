---
description: Analyze a job description — extract ATS keywords, requirements, and gaps vs. client profile
argument-hint: [client-name] [job-description-text or filename]
allowed-tools: [Read, Write, Edit, Glob]
---

You are running job description analysis for a Career Architect client.

## Pre-Flight

1. Verify prerequisites exist:
   - Client profile: `client-profiles/{client-name}-profile.md` — if missing, stop and run `/consult` first
   - Skills inventory: `client-profiles/{client-name}-skills.md` — if missing, recommend `/skill-inventory` first but proceed if client insists

2. Obtain the job description and initialize directory:
   - Define a slug for the job: `{YYYY-MM-DD}-{company}-{title}` (use current date if not provided)
   - Create a dedicated directory: `job-targets/{slug}/`
   - If provided as argument text, save it: `job-targets/{slug}/job-description.txt`
   - If a filename is provided, copy it to the new directory as `job-description.txt`
   - If neither, ask the client to paste the job description

## Execution

Invoke the **Keyword Researcher** agent:

1. Parse job description structure (title, company, level, department, requirements)
2. Extract keywords by tier:
   - Tier 1: Must-have (ATS eliminators)
   - Tier 2: Preferred (score boosters)
   - Tier 3: Industry terminology
   - Tier 4: Culture keywords
3. Extract key action verbs from responsibilities section
4. Cross-reference against client skills inventory for gap analysis
5. Recommend optimal resume title

## Output

Save to `job-targets/{slug}/keywords.md`

## Success Criteria

- [ ] Dedicated job directory created
- [ ] Job description saved as `job-description.txt`
- [ ] All 4 keyword tiers extracted and saved to `keywords.md`
- [ ] Gap analysis complete (green/yellow/red)
- [ ] Resume title recommendation provided
- [ ] ATS notes documented

## Next Steps

> "Keywords Extracted. Ready to:
> 1. `/build-resume {client-name} {slug}` — Build a tailored resume for this role
> 2. `/analyze-job {client-name}` again — Analyze another job posting"
