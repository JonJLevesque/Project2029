# CLAUDE.md — Project 2029

## Project Overview

**Project 2029: A Mandate for Restorative + Transformative Democratic Renewal** is a comprehensive progressive policy framework and counter-document to the Heritage Foundation's "Project 2025." It is a 210,000+ word blueprint for a future Democratic presidential administration covering all major federal agencies and proposing sweeping structural reforms.

- **Published at:** GitHub Pages via Docsify (`index.html` + `.nojekyll`)
- **Repository:** `github.com/JonJLevesque/Project2029`
- **Branch strategy:** Work on `main` directly; use feature branches for major chapter development
- **Last major development:** December 2025

---

## Repository Structure

```
Project2029/
├── CLAUDE.md                          ← You are here
├── README.md                          ← Site homepage (Docsify renders this)
├── TABLE_OF_CONTENTS.md               ← Full navigation with chapter summaries
├── index.html                         ← Docsify config + CDN loading
├── _sidebar.md                        ← Docsify sidebar navigation (89 lines)
├── _coverpage.md                      ← Docsify cover page (landing page)
├── _404.md                            ← Custom 404 page
├── 00_Introduction_*.md               ← Introduction chapter
├── 30_Conclusion_*.md                 ← Conclusion chapter
├── LICENSE                            ← CC BY-SA 4.0
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
│
├── Section1_Restoring_Good_Governance/    (Chapters 1-3)
├── Section2_The_Common_Defense/           (Chapters 4-9)
├── Section3_The_General_Welfare/          (Chapters 10-20)
├── Section4_The_Economy/                  (Chapters 21-26)
├── Section5_Independent_Regulatory_Agencies/ (Chapter 27)
├── Section6_Safeguarding_Democracy_And_Accountability/ (Chapters 28-31)
│
├── Supporting_Materials/
│   ├── Quick_Reference_Guide.md
│   ├── Master_Legislative_Requirements.md
│   ├── Master_Bibliography.md
│   ├── Evidence_Appendix_Trump_Administration_Violations.md
│   ├── Opposition_Playbook.md
│   ├── Advisory_Board.md
│   ├── Activist_Toolkit.md
│   ├── Implementation_Checklists/
│   │   ├── First_100_Days_Checklist.md
│   │   └── Year_1_4_Implementation_Roadmap.md
│   ├── Study_Guides/
│   │   ├── Activist_Study_Guide.md
│   │   └── Educator_Study_Guide.md
│   └── One-Pagers/                    (28 individual reform fact sheets, #01-28, #30)
│
├── .github/workflows/                 ← CI/CD: links.yml, lint.yml, spellcheck.yml
└── .claude/agents/                    ← Custom agents (see below)
```

---

## Chapter Completion Status

### Fully Developed (500+ lines)
| Chapter | Topic | Lines |
|---------|-------|-------|
| Ch 28 | Legal Accountability | 3,512 |
| Ch 30 | Fundamental Transformation | 2,373 |
| Ch 4 | Department of Defense | 1,962 |
| Ch 13 | EPA | 1,549 |
| Ch 22 | Treasury | 1,485 |
| Ch 12 | Energy | 1,108 |
| Ch 29 | Structural Safeguards | 1,028 |
| Ch 15 | HUD | 950 |
| Ch 17 | DOJ | 973 |
| Ch 11 | Education | 913 |
| Ch 31 | Constitutional Hardball | 769 |
| Ch 1 | White House Office | 708 |

### Partially Developed (100-500 lines)
| Chapter | Topic | Lines |
|---------|-------|-------|
| Ch 5 | Homeland Security | 375 |
| Ch 8 | Media Agencies | 280 |
| Ch 7 | Intelligence Community | 157 |
| Ch 6 | Department of State | 171 |
| Ch 3 | Personnel Agencies | 533 |
| Ch 2 | Executive Office | 765 |

### Stubs — Need Full Development (under 100 lines)
| Chapter | Topic | Lines | Priority |
|---------|-------|-------|----------|
| Ch 14 | HHS | 32 | HIGH |
| Ch 18 | Labor | 23 | HIGH |
| Ch 16 | Interior | 16 | HIGH |
| Ch 20 | Veterans Affairs | 16 | HIGH |
| Ch 21 | Commerce | 15 | MEDIUM |
| Ch 19 | Transportation | 15 | MEDIUM |
| Ch 10 | Agriculture | 71 | MEDIUM |
| Ch 24 | Federal Reserve | 14 | MEDIUM |
| Ch 26 | Trade Policy | 14 | MEDIUM |
| Ch 25 | Small Business | 15 | MEDIUM |
| Ch 23 | Export-Import Bank | 13 | MEDIUM |
| Ch 27 | Financial Regulatory | 27 | MEDIUM |
| Ch 9 | USAID | 56 | LOW |

---

## Chapter Template (Follow This Structure)

Every chapter should follow this pattern. Use Chapter 13 (EPA) as the gold standard template.

```markdown
# Chapter N: [Department/Agency Name]

## Executive Summary

[2-3 paragraph overview of what the department does, what Project 2025 did to it,
and what we will do to restore and transform it]

**The Stakes**: [One paragraph on why this matters urgently]

**Key Reforms**:
- [Bullet list of 5-10 major reforms]

**Constitutional and Legal Basis**: [Key statutes and constitutional authorities]

---

## Part I: Project 2025 [Topic] Damage/Destruction

### [Damage Area 1 — e.g., "The Assault on Workers' Rights"]

**What Project 2025 Did:**

[Specific actions, with bold subheadings for each policy area]

[Continue with 3-6 damage areas]

### The Human Cost
[Specific statistics on who was harmed and how]

---

## Part II: Legal and Constitutional Foundations

### Constitutional Authority
[Article I, II, specific amendments, Commerce Clause, etc.]

### Major Applicable Statutes
[Specific U.S. Code sections, named acts]

### [Area-specific legal analysis]

---

## Part III: Comprehensive [Topic] Restoration and Reform

### Reform I: [First Major Reform Area]
#### [Subheading]
[Specific policy actions with legal grounding]

[Continue for 5-10 major reform areas]

---

## Implementation Timeline

### Day One Executive Actions
- [Specific executive orders and directives]

### First 100 Days
- [Legislative asks, key appointments, regulatory reversals]

### Year 1: Foundation
- [Primary legislation, structural changes]

### Years 2-4: Consolidation
- [Deeper reforms, institutional embedding]

---

## Legislative Requirements

### [Proposed Act Name] (e.g., "The [Name] Act of 202X")
- **Purpose:** [One sentence]
- **Key Provisions:** [Bullet list]
- **Constitutional Authority:** [Clause/statute]

[List 3-8 specific legislative proposals]

---

## Success Metrics

[Measurable outcomes: specific statistics, timelines, benchmarks]

---

## References

[Legal citations: U.S. Code sections, CFR regulations, SCOTUS cases, statutes]
```

**Target length:** 500–1,500 lines (4,000–12,000 words) per chapter.

---

## Writing Style Conventions

1. **Direct Project 2025 quotes** go in bold with page citations: **"[quote]"** *(Project 2025, p. XX)*
2. **Every policy claim** needs a legal authority: statute, CFR section, or SCOTUS case
3. **Implementation actions** are specific: "Issue Executive Order reinstating X" not "restore X"
4. **Tone:** Serious, prosecutorial, evidence-based. No hedging. No passive voice.
5. **No emojis** in chapter content (README and one-pagers use them, chapters do not)
6. **Statistics** should be sourced; use "approximately" when exact figures unavailable
7. **Headings:** Use `##` for major sections, `###` for subsections, `####` for sub-subsections
8. **Cross-references** use Docsify-compatible relative links: `[Chapter 30](Section6_.../Chapter_30_...md)`

---

## Custom Claude Agents (in `.claude/agents/`)

| Agent | File | Purpose |
|-------|------|---------|
| Constitutional Law Advisor | `constitutional-law-advisor.md` | Legal analysis, constitutional review of policy proposals |
| Policy Researcher | `policy-researcher.md` | Web research for chapter development, current department status |
| Fact Checker | `fact-checker.md` | Verify citations, statute numbers, statistics |
| Content Editor | `content-editor.md` | Consistency review, style enforcement across chapters |

**When developing a chapter:** Use Policy Researcher → draft content → Constitutional Law Advisor review → Fact Checker verification → Content Editor final pass.

---

## Docsify Configuration

**Key files:** `index.html` (CDN, plugins, config), `_sidebar.md` (navigation), `_coverpage.md` (landing page)

**Plugins loaded:**
- Docsify core (pinned version with SRI hash)
- Search plugin
- Copy-code plugin
- Pagination plugin (Previous/Next between chapters)
- Sidebar collapse plugin

**GitHub Pages:** Deploys directly from `main` branch. Push to `main` = live site. No build step.

---

## CI/CD (GitHub Actions in `.github/workflows/`)

| Workflow | File | What it checks |
|----------|------|----------------|
| Link checking | `links.yml` | All internal links and cross-references |
| Markdown linting | `lint.yml` | Formatting consistency (markdownlint-cli2) |
| Spell checking | `spellcheck.yml` | Typos + policy acronym dictionary (cspell) |

---

## Git Workflow

- **Feature branches** for major chapter development: `feature/chapter-14-hhs`
- **Direct commits to `main`** acceptable for small edits, config changes, metadata
- **Commit message format:** Imperative verb, descriptive: `Add Chapter 14 HHS - comprehensive healthcare reform`
- **Never force push to main**

---

## Key Policy Context

- **The opponent:** Heritage Foundation's Project 2025 (Mandate for Leadership)
- **The goal:** Ready-made policy playbook for next Democratic administration
- **Two agendas:** Restorative (Chapters 1-29) + Transformative (Chapter 30 + throughout)
- **6 proposed constitutional amendments:** 28th (Voting Rights), 29th (Presidential Accountability), 30th (Citizens United), 31st (Senate Terms), 32nd (Electoral College), 33rd (SCOTUS Terms)
- **90+ proposed federal laws** consolidated in `Supporting_Materials/Master_Legislative_Requirements.md`
