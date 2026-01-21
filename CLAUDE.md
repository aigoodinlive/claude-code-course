# Claude Code Training Course

## Project Overview

**Product:** Hebrew Claude Code Training Course
**Target Audience:** Small businesses, freelancers, individuals
**Delivery:** In-person + online workshops
**Language:** Hebrew (RTL support)

---

## Course Tiers

### Tier 1: Intro (₪250, 1.5 hours)
**Goal:** Students can use Claude Code for daily tasks

| Module | Duration | Content |
|--------|----------|---------|
| What is Claude Code | 20 min | Overview, installation, first run |
| Basic Commands | 30 min | Chat, files, bash, navigation |
| First Project | 40 min | Hands-on: build something useful |

**Materials:** Slides, cheatsheet, exercise files
**Outcome:** Comfortable using Claude Code independently

### Tier 2: Advanced (₪500, 3 hours)
**Goal:** Students build production-ready tools

| Module | Duration | Content |
|--------|----------|---------|
| Skills Deep Dive | 45 min | Create custom skills |
| Subagents | 45 min | Parallel work, specialized agents |
| Hooks & Automation | 30 min | Pre/post tool hooks |
| MCP Servers | 30 min | External integrations |
| Hands-on Project | 30 min | Build a custom agent |

**Materials:** Templates, reference code, WhatsApp support group
**Outcome:** Can build custom agents and integrations

### Tier 3: Business (₪1,500)
**Goal:** Team-wide Claude Code adoption

| Module | Duration | Content |
|--------|----------|---------|
| Team Workflows | 1 hour | Shared skills, permissions |
| Security & Compliance | 45 min | API keys, data handling |
| Cost Optimization | 30 min | Model selection, context management |
| Deployment Patterns | 45 min | CI/CD, automation |

**Participants:** Up to 5 people
**Support:** Monthly office hours for 3 months
**Outcome:** Production-ready Claude Code integration

---

## Teaching Principles

1. **Live demos over slides** - Show, don't tell
2. **Immediate practice** - Theory → Demo → Hands-on
3. **Real problems** - Use actual business scenarios
4. **Hebrew-first** - All explanations in Hebrew
5. **Safe environment** - Sandboxed exercises, no production risk
6. **Progressive complexity** - Build on previous lessons

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
│   ├── intro/             # Tier 1 lessons
│   ├── advanced/          # Tier 2 lessons
│   └── business/          # Tier 3 lessons
├── examples/              # Demo code
├── exercises/             # Student workspaces
├── templates/             # Quick-start files
└── tools/                 # Course management scripts
```

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
| `intro-coach` | Patient beginner guide |
| `advanced-mentor` | Production patterns expert |
| `business-strategist` | Enterprise deployment advisor |

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

## Links

- **Cheatsheet:** `claude-code-cheatsheet.pdf`
- **Skills Library:** `skills-pdfs/`
- **GitHub:** (to be created)
