---
description: Prepare for an interview — behavioral questions, technical mocks, and company research
argument-hint: [client-name] [job-slug]
allowed-tools: [Read, Write, Edit, Glob]
---

You are running interview preparation for a Career Architect client.

## Pre-Flight

1. Verify client profile: `client-profiles/{client-name}-profile.md`
   - If missing, run `/consult {client-name}` first

2. Verify job target exists: `job-targets/{job-slug}/`
   - If missing, run `/analyze-job {client-name}` first to ensure we have context on the role

3. (Optional) Check for existing resume in `job-targets/{job-slug}/resume.md` to tailor answers

## Execution

Invoke the **InterviewAce** agent to:

1. **Intake** — Confirm interview date, format (virtual/in-person), and interviewer names if known.
2. **Strategy** — Generate a custom prep plan (1-week or 2-week) based on the timeline.
3. **Behavioral Prep** — Identify top STAR stories relevant to this specific job description.
4. **Mock Interview** — Conduct a mini-mock interview (5-10 mins) with immediate feedback.
5. **Company Research** — Provide talking points on company culture, recent news, and specific questions for the interviewer.

## Output

Save progress and feedback to `job-targets/{job-slug}/interview-prep.md`

## Success Criteria

- [ ] Custom prep plan generated
- [ ] At least 5 STAR stories mapped to job requirements
- [ ] At least one mock interview question conducted and scored
- [ ] Specific "Questions for Interviewer" provided
- [ ] Follow-up and negotiation tips shared

## Delivery

> "🚀 Ready to crush this interview! Prep plan and initial mock feedback saved to `job-targets/{job-slug}/interview-prep.md`. 
> Want to do another mock question or dive deeper into [Company]'s culture?"
