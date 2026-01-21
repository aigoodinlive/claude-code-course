# Claude Code Training Course

## Project Overview

**Product:** Hebrew Claude Code Training Course
**Target Audience:** Small businesses, freelancers, individuals
**Delivery:** In-person + online workshops
**Language:** Hebrew (RTL support)

---

## Course Tiers (NEW STRUCTURE)

### FREE Course - למתחילים לגמרי
**Goal:** Non-technical users can install and start using Claude Code
**Duration:** Self-paced (~2 hours total)
**Price:** Free

| Lesson | Topic | Description |
|--------|-------|-------------|
| 01 | מה זה טרמינל? | For people who never used command line |
| 02 | התקנה צעד אחר צעד | Step-by-step with images |
| 03 | מה זה Claude Code? | Comparison with ChatGPT |
| 04 | צעדים ראשונים | Basic commands and questions |
| 05 | קובץ CLAUDE.md | Introduction to project configuration |
| 06 | מה זה Skills? | Basic understanding of skills |
| 07 | פרויקט ראשון | Build a simple task manager |

**Materials:** Written lessons, exercises
**Outcome:** Comfortable using Claude Code independently

### PAID Course - למי שכבר התחיל
**Goal:** People who started using Claude Code and want to level up
**Duration:** 3 hours
**Price:** ₪XXX (TBD)

| Lesson | Topic | Description |
|--------|-------|-------------|
| 01 | CLAUDE.md מתקדם | Advanced project configuration |
| 02 | צלילה לעולם ה-Skills | Understanding and using skills |
| 03 | בניית Skill משלכם | Hands-on skill creation |
| 04 | זרימות עבודה | Workflows and automation |

**Materials:** Templates, reference code, WhatsApp support group
**Outcome:** Can build custom skills and workflows

---

## Teaching Principles

1. **Live demos over slides** - Show, don't tell
2. **Immediate practice** - Theory → Demo → Hands-on
3. **Real problems** - Use actual business scenarios
4. **Hebrew-first** - All explanations in Hebrew
5. **Safe environment** - Sandboxed exercises, no production risk
6. **Progressive complexity** - Build on previous lessons
7. **Non-technical friendly** - Free course designed for people who don't know CMD

---

## Project Structure

```
CLAUDE Course/
├── CLAUDE.md              # This file
├── .claude/
│   ├── skills/            # Course-specific skills
│   ├── agents/            # Teaching assistants
│   └── hooks/             # Automation
├── content/
│   ├── free/              # FREE course lessons (7 lessons)
│   ├── paid/              # PAID course lessons (4 lessons)
│   └── archive/           # Old 3-tier structure (deprecated)
├── dashboard/             # Course management dashboard
├── examples/              # Demo code
├── exercises/             # Student workspaces
├── templates/             # Quick-start files
└── tools/                 # Course management scripts
```

---

## Content Status

### FREE Course (7/7 complete)
- [x] 01-what-is-terminal.md
- [x] 02-installation.md
- [x] 03-what-is-claude-code.md
- [x] 04-first-steps.md
- [x] 05-claude-md-intro.md
- [x] 06-skills-intro.md
- [x] 07-first-project.md

### PAID Course (0/4 complete - outlines only)
- [ ] 01-claude-md-advanced.md
- [ ] 02-skills-deep-dive.md
- [ ] 03-build-your-skill.md
- [ ] 04-workflows.md

---

## Skills Available

| Skill | Purpose |
|-------|---------|
| `/generate-lesson` | Auto-create lesson content |
| `/create-exercise` | Generate exercises with solutions |
| `/evaluate-progress` | Check student submissions |

---

## Agents Available

| Agent | Role |
|-------|------|
| `training-coach` | Main training assistant |
| `intro-coach` | Patient beginner guide |
| `advanced-mentor` | Production patterns expert |

---

## Safety Rules

- All student exercises run in isolated directories
- No access to instructor's production systems
- Examples use public APIs only
- All code is version-controlled and recoverable

---

## Hebrew Display Note

When outputting Hebrew in terminal:
1. Reverse letters within each word
2. Reverse word order

Example: "שלום עולם" → "םלוע םולש"

---

## Dashboard

Access the course dashboard at: `dashboard/index.html`
Run with: `python -m http.server 8888` from the project root

---

## Links

- **Dashboard:** `http://localhost:8888/`
- **Cheatsheet:** `claude-code-cheatsheet.pdf`
- **Skills Library:** `skills-pdfs/`
- **GitHub:** (to be created)
