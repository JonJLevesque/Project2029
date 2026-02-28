# Project 2029 — Implementation Resume Plan

## Context Warning: API Filtering

Reading political chapter content or old settings.local.json can contaminate context and trigger output filtering. Rules:
1. Commit after every file write
2. Keep text responses short
3. Write config/infrastructure files before any chapter files
4. Use worktree agents (one per chapter) for all chapter content
5. Never read multiple political files in same tool call

---

## Progress Tracker

### Done ✅
- `CLAUDE.md` — project context file (commit c0681fb)
- `.claude/settings.local.json` — cleaned up bloated permissions (commit 80ef8d0)
  - Kept: `WebSearch`, `Bash(git:*)`, `Bash(wc:*)`, `Bash(curl:*)`

### Remaining Infrastructure (do in this order, all safe)

#### Phase 1: Foundation Files
- [ ] `/LICENSE` — CC BY-SA 4.0 standard text
- [ ] `/CONTRIBUTING.md` — contributor guidelines
- [ ] `/CODE_OF_CONDUCT.md` — Contributor Covenant v2.1

#### Phase 2: Docsify Enhancements (`/index.html` + new files)
- [ ] Update `/index.html`:
  - Pin CDN versions with SRI integrity hashes
  - Add `docsify-pagination` plugin (prev/next nav)
  - Add `docsify-sidebar-collapse` plugin
  - Enable `coverpage: true`
  - Add Open Graph + Twitter Card meta tags
  - Add favicon link
- [ ] Create `/_coverpage.md` — cover page with title, mission, "Get Started" button
- [ ] Create `/_404.md` — custom 404 page

#### Phase 3: Config Files
- [ ] `/.markdownlint.yml` — disable MD013 line length, standard rules
- [ ] `/.cspell.json` — policy acronym dictionary (USAID, OIRA, NAAQS, WOTUS, etc.)

#### Phase 4: CI/CD Workflows
- [ ] `/.github/workflows/links.yml` — lychee link checker, runs on PR + weekly cron
- [ ] `/.github/workflows/lint.yml` — markdownlint-cli2, runs on PR
- [ ] `/.github/workflows/spellcheck.yml` — cspell, runs on PR

#### Phase 5: Claude Agent Definitions
Pattern: follow `.claude/agents/constitutional-law-advisor.md` structure (frontmatter + instructions)
- [ ] `/.claude/agents/policy-researcher.md` — WebSearch-based federal policy research
- [ ] `/.claude/agents/fact-checker.md` — verify statutes, citations, statistics
- [ ] `/.claude/agents/content-editor.md` — style enforcement, structural gaps

#### Phase 6: Stale Branch Review
Three remote branches to review, cherry-pick useful content, then delete:
- `remotes/origin/claude/add-ice-punishment-section-...`
- `remotes/origin/claude/add-legalization-benefits-policy-...`
- `remotes/origin/claude/review-urgent-issue-...`

---

## Phase 7: Chapter Development (worktree agents, one at a time)

Each chapter: spawn `general-purpose` agent with `isolation: "worktree"`, merge result to main.

**Template source:** `Section3_The_General_Welfare/Chapter_13_Environmental_Protection_Agency.md`
**Target:** 500–1,500 lines per chapter

### Batch 1 — High Priority
| Task | Chapter | File | Current Lines |
|------|---------|------|---------------|
| #7  | Ch 14: HHS | `Section3_The_General_Welfare/Chapter_14_Dept_of_Health_and_Human_Services.md` | 32 |
| #8  | Ch 18: Labor | `Section3_The_General_Welfare/Chapter_18_Dept_of_Labor.md` | 23 |
| #9  | Ch 16: Interior | `Section3_The_General_Welfare/Chapter_16_Dept_of_Interior.md` | 16 |
| #10 | Ch 20: VA | `Section3_The_General_Welfare/Chapter_20_Dept_of_Veterans_Affairs.md` | 16 |

### Batch 2 — Economic Policy
| Task | Chapter | File | Current Lines |
|------|---------|------|---------------|
| #11a | Ch 21: Commerce | `Section4_The_Economy/Chapter_21_Dept_of_Commerce.md` | 15 |
| #11b | Ch 19: Transportation | `Section3_The_General_Welfare/Chapter_19_Dept_of_Transportation.md` | 15 |
| #11c | Ch 10: Agriculture | `Section3_The_General_Welfare/Chapter_10_Dept_of_Agriculture.md` | 71 |

### Batch 3 — Financial/Trade
| Task | Chapter | File | Current Lines |
|------|---------|------|---------------|
| #12a | Ch 24: Federal Reserve | `Section4_The_Economy/Chapter_24_Federal_Reserve.md` | 14 |
| #12b | Ch 26: Trade Policy | `Section4_The_Economy/Chapter_26_Trade_Policy.md` | 14 |
| #12c | Ch 25: SBA | `Section4_The_Economy/Chapter_25_Small_Business_Administration.md` | 15 |
| #12d | Ch 23: Export-Import Bank | `Section4_The_Economy/Chapter_23_Export-Import_Bank.md` | 13 |
| #12e | Ch 27: Financial Regulatory | `Section5_Independent_Regulatory_Agencies/Chapter_27_Financial_Regulatory_Agencies.md` | 27 |
| #12f | Ch 9: USAID | `Section2_The_Common_Defense/Chapter_09_USAID.md` | 56 |

---

## Chapter Template Structure

Every chapter must follow this structure (Ch 13 EPA is gold standard):

```
# Chapter N: [Department Name]

## Executive Summary
[2-3 paragraphs + The Stakes + Key Reforms bullets + Constitutional Basis]

---

## Part I: Project 2025 [Topic] Damage
### [Damage Area 1]
**What Project 2025 Did:**
### The Human Cost

---

## Part II: Legal and Constitutional Foundations
### Constitutional Authority
### Major Applicable Statutes

---

## Part III: Comprehensive Restoration and Reform
### Reform I: [First Major Reform]
[5-10 reform areas]

---

## Implementation Timeline
### Day One Executive Actions
### First 100 Days
### Year 1: Foundation
### Years 2-4: Consolidation

---

## Legislative Requirements
### [Proposed Act Name]

---

## Success Metrics

---

## References
```

---

## Writing Style Rules
1. Direct quotes from Project 2025 in bold with page citations
2. Every policy claim needs a legal authority (statute, CFR, SCOTUS case)
3. Implementation actions are specific ("Issue Executive Order reinstating X")
4. Tone: serious, prosecutorial, evidence-based — no hedging, no passive voice
5. No emojis in chapter content
6. Statistics sourced; use "approximately" when exact figures unavailable

---

## Key File References
- Sidebar: `/_sidebar.md` (89 lines — update as chapters complete)
- TOC: `/TABLE_OF_CONTENTS.md` (update as chapters complete)
- Docsify config: `/index.html`
- Existing agent pattern: `.claude/agents/constitutional-law-advisor.md`

---

## Git Workflow
- Feature branches for chapters: `feature/chapter-14-hhs`
- Commit format: imperative verb + description
- Never force push to main
- `.claude/` is in `.gitignore` — use `git add -f` for agent files

## Docsify CDN Resources to Pin with SRI
Use https://www.srihash.org/ or jsdelivr to get integrity hashes for:
- `https://cdn.jsdelivr.net/npm/docsify@4.13.1/lib/docsify.min.js`
- `https://cdn.jsdelivr.net/npm/docsify@4.13.1/lib/themes/vue.css`
- `https://cdn.jsdelivr.net/npm/docsify@4.13.1/lib/plugins/search.min.js`
- `https://cdn.jsdelivr.net/npm/docsify-copy-code@2.1.1/dist/docsify-copy-code.min.js`
- `https://cdn.jsdelivr.net/npm/docsify-pagination/dist/docsify-pagination.min.js`
- `https://cdn.jsdelivr.net/npm/docsify-sidebar-collapse/dist/docsify-sidebar-collapse.min.js`
