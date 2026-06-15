# CV Repository

Personal CV/Resume repository for Danilo C. Dutra using LaTeX.

## Overview

This repository uses the [Awesome-CV](https://github.com/posquit0/Awesome-CV) LaTeX template to generate professional CVs and resumes.

## Structure

```
latex/
├── resume.tex          # Main resume document (actively used)
├── cv.tex              # Full CV document (template example)
├── coverletter.tex     # Cover letter template
├── resume/             # Resume section files
│   ├── summary.tex
│   ├── experience.tex
│   ├── education.tex
│   ├── languages.tex
│   ├── skills.tex      # Technical skills for ATS
│   └── ...
└── cv/                 # CV section files (template examples)
    └── ...
```

## Key Files

- **`latex/resume.tex`** - The main resume file to edit. Includes personal info and imports section files.
- **`latex/resume/skills.tex`** - Technical skills section (ATS-optimized keywords).
- **`latex/resume/experience.tex`** - Work experience entries.

## Building

- Requires XeLaTeX for compilation (`%!TEX TS-program = xelatex`)
- Docker Compose available for building (`docker compose`)

## LaTeX Conventions

### Adding a skill category
```latex
\cvskill
  {Category Name} % Category
  {Skill1, Skill2, Skill3} % Skills
```

### Adding an experience entry
```latex
\cventry
  {Job Title} % Job title
  {Company} % Organization
  {Location} % Location
  {Date Range} % Date(s)
  {
    \begin{cvitems}
      \item {Description of achievement or responsibility}
    \end{cvitems}
  }
```

### Adding a section
1. Create a new `.tex` file in `latex/resume/`
2. Add `\input{resume/filename.tex}` to `latex/resume.tex`

## ATS Optimization Guidelines

- Use full technology names (e.g., "PostgreSQL" not "Postgres", "Power BI" not "PowerBI")
- Expand abbreviations on first use: "Infrastructure as Code (Terraform)", "Change Data Capture (CDC)"
- Use separate `\item` entries instead of `\\` line breaks within bullets
- Include keywords from Skills section naturally within Experience descriptions
- Add quantifiable metrics where possible (cost savings, percentages, team sizes)
- Ensure technologies mentioned in Skills appear in Experience context
- Use standard date format: "Mon. YYYY" (e.g., "Oct. 2014" not "Out. 2014")

## Notes

- The `cvskills` environment produces clean text that ATS systems can parse
- Section highlight color is set to orange (`#D35400`)
