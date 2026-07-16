---
description: Analyze a job description — extract ATS keywords, requirements, and gaps vs. user profile
argument-hint: [job-description-text or filename]
allowed-tools: [Task, Read, Write, Edit, Glob]
---

You are running job description analysis for a Career Architect user.

## Pre-Flight

1. Verify prerequisites exist:
   - User profile: `profile/profile.md` — if missing, stop and run `/consult` first
   - Skills inventory: `profile/skills.md` — if missing, recommend `/skill-inventory` first but proceed if user insists

2. Obtain the job description:
   - Derive the job slug: `{company}-{title}` in kebab-case (e.g. `acme-staff-engineer`). Every artifact for this job lives in `job-targets/{slug}/` — one directory per job.
   - If provided as argument text, save it: `job-targets/{slug}/job-description.txt`
   - If a slug or filename is provided, read the job description from `job-targets/{slug}/`
   - If neither, ask the user to paste the job description

## Execution

Invoke the **Keyword Researcher** agent:

1. Parse job description structure (title, company, level, department, requirements)
2. Extract keywords by tier:
   - Tier 1: Must-have (ATS eliminators)
   - Tier 2: Preferred (score boosters)
   - Tier 3: Industry terminology
   - Tier 4: Culture keywords
3. Extract key action verbs from responsibilities section
4. Cross-reference against user skills inventory for gap analysis
5. Recommend optimal resume title

## Output

Save to `job-targets/{slug}/keywords.md`

## Success Criteria

- [ ] All 4 keyword tiers extracted
- [ ] Gap analysis complete (green/yellow/red)
- [ ] Resume title recommendation provided
- [ ] ATS notes documented

## Next Steps

> "Keywords Extracted. Ready to:
> 1. `/build-resume {company}-{title}` — Build a tailored resume for this role
> 2. `/analyze-job` again — Analyze another job posting"
