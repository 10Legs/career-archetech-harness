---
name: ats-optimization
description: ATS (Applicant Tracking System) optimization rules, formatting requirements, and keyword placement strategies. Invoke when building or reviewing any resume for ATS compliance.
allowed-tools: Read, Glob
---

# ATS Optimization Skill

## What is ATS and Why It Matters

Applicant Tracking Systems are software used by 98%+ of Fortune 500 companies and most mid-size companies to filter resumes before a human sees them. A resume that fails ATS parsing is rejected automatically, regardless of qualifications.

## ATS Anti-Patterns (Immediate Disqualifiers)

### Formatting That Breaks Parsing
- **Tables and columns**: ATS reads left-to-right and often merges columns into gibberish
- **Text boxes**: Content is often completely invisible to ATS
- **Headers and footers**: Contact info placed here gets skipped
- **Graphics, icons, logos**: Not parsed — just dead space
- **Fancy fonts**: Non-standard fonts may render as garbage characters
- **PDFs from design tools** (Canva, InDesign): Often corrupt ATS parsing — use Word-generated PDF
- **Infographic resumes**: Almost universally ATS failures

### Section Heading Mistakes
These headings confuse ATS parsers — use standard names instead:

| Non-Standard | Use Instead |
|-------------|-------------|
| "My Story" | Professional Summary |
| "Where I've Been" | Work Experience |
| "What I Know" | Skills |
| "Credentials" | Education |
| "Wins" | Achievements |

### Date Formatting Issues
- Must be consistent throughout
- Acceptable: "January 2020", "Jan 2020", "01/2020"
- Never: "2020-01", "Winter 2020", just "2020" (for ongoing roles, use "Present")

## ATS Best Practices

### File Format
- `.docx` is most universally parsed
- `.pdf` is acceptable if generated from Word (not design software)
- Never submit `.pages`, `.rtf`, or image-based PDFs

### Keyword Placement Priority
ATS systems weight keywords differently by location:
1. **Job Title field / Resume title** — Highest weight
2. **Professional Summary** — Very high weight
3. **Skills/Core Competencies section** — High weight
4. **Job titles within experience** — High weight
5. **Bullet points** — Standard weight
6. **Education section** — Lower weight for most roles

### Keyword Density Rules
- Include Tier 1 keywords **at least once verbatim** — exact match matters
- Acronyms: spell out AND abbreviate (e.g., "Search Engine Optimization (SEO)")
- Don't keyword-stuff — ATS systems now penalize unnatural density
- Synonyms: use both versions if space permits (e.g., "machine learning / ML")

### Job Title Alignment
- If your actual title was "Growth Hacker" but target is "Digital Marketing Manager", put your actual title but add clarifying context in bullets
- Some candidates legitimately add a hybrid: "Digital Marketing Manager (titled: Growth Hacker)"
- Never outright lie about titles — background checks exist

### Contact Information
- Must be in the main document body (not header/footer)
- Include: Full Name, City/State, Phone, Email, LinkedIn URL
- Optional: Portfolio, GitHub
- Exclude: Photo, full address, DOB, marital status

## ATS Compliance Checklist

Run this before finalizing any resume:

- [ ] File format is .docx or Word-generated .pdf
- [ ] No tables used for layout
- [ ] No text boxes
- [ ] Contact info in document body
- [ ] Standard section headings
- [ ] Dates formatted consistently as "Month Year"
- [ ] No graphics or icons
- [ ] All Tier 1 keywords appear at least once
- [ ] Acronyms spelled out on first use
- [ ] No columns (single-column layout throughout)
- [ ] Fonts are standard (Calibri, Arial, Georgia, Times New Roman)

## Modern ATS Nuances (2024–2025)

- Most modern ATS (Workday, Greenhouse, Lever, iCIMS) handle PDF well
- AI-screening layers (HireVue, etc.) now score semantic relevance, not just exact keyword match
- LinkedIn Easy Apply submits profile data, not resume file — optimize both
- Some ATS score based on skills taxonomy matching, not raw text
