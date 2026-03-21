# Personal Career Architect Harness

A personal, multi-agent AI harness built for **Claude Code CLI** and **Gemini CLI** that transforms your skills and experiences into compelling career narratives. This harness is designed for a single user to manage their professional profile, tailor resumes for specific job targets, and execute a strategic job search.

---

## How It Works

The harness orchestrates a team of specialized AI agents to manage your career documents and strategy. 

- **Claude Code CLI**: Uses `CLAUDE.md` and slash commands in `.claude/commands/`.
- **Gemini CLI**: Uses `GEMINI.md` and follows the personal operational workflows described therein.

Both tools use the same underlying agents and "memory" (your profile and history) to ensure a consistent experience.

### Workflow

The harness follows a logical progression, but as a personal tool, you can jump into any step once your initial profile is set up:

```
/consult → /skill-inventory → /analyze-job → /build-resume → /interview-prep → /career-strategy
```

1. **Intake (`/consult`)**: Define your career goals and professional background.
2. **Skill Inventory (`/skill-inventory`)**: Build a comprehensive, "master" list of your hard and soft skills.
3. **Job Analysis (`/analyze-job`)**: Analyze a specific job description to extract ATS keywords and identify gaps in your profile.
4. **Resume Building (`/build-resume`)**: Generate a highly-tailored resume and cover letter for a specific role.
5. **Interview Prep (`/interview-prep`)**: Prepare for specific interviews with mock sessions and STAR story coaching.
6. **Career Strategy (`/career-strategy`)**: Develop a networking plan and long-term career strategy.

---

## Getting Started (Single-User)

### 1. Initialize Your Profile
Run the consultation command to create your master profile.
```bash
/consult [your-name]
```
This saves your goals to `client-profiles/[your-name]-profile.md`.

### 2. Map Your Skills
Build your master skills inventory.
```bash
/skill-inventory [your-name]
```

### 3. Apply for a Job
When you find a role you want, analyze it and then build your tailored documents.
```bash
/analyze-job [your-name]
# (Follow prompts to paste JD)
/build-resume [your-name] [job-slug]
```

### 4. Prepare for the Interview
Once you land an interview, use InterviewAce to prepare.
```bash
/interview-prep [your-name] [job-slug]
```

---

## Repository Structure & "Memory"

This repository acts as your career's "external brain." All your data is persisted in the following structure:

```
client-profiles/          # Your master profile and skill inventories
job-targets/              # Analysis of every job you've targeted
resume-outputs/           # Every resume and cover letter generated
patterns_library/         # Your personal library of resume bullets and patterns
.claude/                  # Agent logic and command definitions
GEMINI.md                 # Gemini CLI instructions and project memory
CLAUDE.md                 # Claude Code instructions
```

---

## Why Single-User?

This harness is built to be a **Personal Career OS**. By keeping everything in one private repository, you:
- Maintain a complete history of every application and strategy.
- Build a "living" skills inventory that grows with your career.
- Ensure your personal brand remains consistent across all documents.
- Leverage AI agents that "remember" your background and preferences.

---

## Ethics & Standards

- **Evidence Always**: Never fabricate accomplishments. The agents are instructed to highlight your *actual* impact.
- **Privacy**: Keep this repository private to protect your personal and professional data.
