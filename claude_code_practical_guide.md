# Claude Code - Practical Guide for Solo Developers & Small Teams

**Target Audience:** Non-coders doing "vibe coding" | Solo entrepreneurs | Small teams (1-2 people)  
**Focus:** Project management, practical usage, avoiding technical complexity

---

## 1. SETUP & INSTALLATION

### What You Need to Install Claude Code

**Three Installation Methods:**

**Option A: MacOS (Homebrew)**
```bash
brew install --cask claude-code
```

**Option B: MacOS, Linux, WSL**
```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Option C: Windows CMD**
```bash
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

### First Time Setup

After installation:
1. Run `claude` in your terminal
2. You'll be prompted to authenticate
3. Follow the authentication flow

### Optional: Cloud Provider Setup

If you're using AWS or Google Cloud (most solo users won't need this):
- AWS Bedrock: https://code.claude.com/docs/en/amazon-bedrock
- Google Cloud Vertex: https://code.claude.com/docs/en/google-vertex-ai

---

## 2. PROJECT SETUP (For Vibe Coders)

### Key Insight
**"Working with Claude Code is more interesting if you have a project to work with."**

You don't need to run the course's demo project - you can use your own codebase!

### Setting Up Your Own Project

**Step 1:** Have a project folder on your computer
- Can be an existing website/app
- Can be a new idea you want to build
- Doesn't matter if it's "messy" - Claude can help organize it

**Step 2:** Navigate to your project folder in terminal
```bash
cd /path/to/your/project
```

**Step 3:** Start working with Claude Code
```bash
claude
```

### Optional: API Integration

**When You Need It:**
If your project needs to generate UI components using Claude's API directly

**How to Set It Up:**
1. Get an API key at: https://console.anthropic.com/
2. Create a file called `.env` in your project folder
3. Add your API key to that file
4. **Important:** This is optional - if you skip this, Claude Code will still work, just with limited features for that specific project

**What Happens Without API Key:**
The app will generate "static fake code" instead of real AI-generated components. This is fine for learning!

**Running Your Project:**
```bash
npm run setup    # Install dependencies
npm run dev      # Start the project
```

---

## 3. MANAGING YOUR PROJECTS

### File Organization Tips

**The `.claude` Directory:**
After running Claude Code commands, you'll see a `.claude` folder with `settings.json` files inside

**What This Means:**
- These files store Claude Code configurations for your project
- Different projects will have different paths
- **Don't share these files** - paths on your machine are different from paths on other machines

**Solution for Sharing Projects:**
The course uses a `settings.example.json` file with a `$PWD` placeholder that gets replaced with your actual project path when you run `npm run setup`

---

## 4. WORKING WITH CLAUDE CODE

### Critical Concepts

**Context Management (Most Important!)**
From the "Adding Context" lesson, we learned that:
- Your project might have dozens or hundreds of files
- Claude only needs the RIGHT information
- **Too much irrelevant context DECREASES Claude's performance**
- Learning to guide Claude to relevant files is essential

**What to Include as Context:**
- Relevant code files only
- Documentation for libraries you're using
- Configuration files Claude needs to see
- The specific part of your project you're working on

**What NOT to Include:**
- Your entire project folder at once
- Unrelated files
- Old code you're not using
- Files from other projects

### Practical Example

**Bad Approach:**
"Claude, here's my entire project folder with 500 files. Build me a login page."

**Good Approach:**
"Claude, I'm working on adding a login page. Here are my existing:
- authentication config file
- user database schema
- design system components
Focus on these files to create a login page that matches my existing setup."

---

## 5. HOOKS - AUTOMATION FOR YOUR WORKFLOW

### What Are Hooks?

**Simple Definition:** Automated actions that run at specific moments

**When They Run:**
- `PreToolUse` - Before Claude uses a tool
- `PostToolUse` - After Claude uses a tool
- `Notification` - When Claude sends you a notification (or after being idle 60 seconds)
- `Stop` - When Claude finishes responding
- `SubagentStop` - When a background task finishes
- `PreCompact` - Before a file/folder operation

### Practical Example

**TodoWrite Tool:**
Claude has a built-in tool to track to-do items

**Using a PostToolUse Hook:**
You can create a hook that runs AFTER Claude uses the TodoWrite tool to automatically log what was added

### Why This Matters for Vibe Coders

**Before Hooks:** You manually track what Claude does  
**With Hooks:** Automatic tracking and organization  
**Result:** Better project management without coding

---

## 6. SECURITY & BEST PRACTICES

### From "Gotchas around hooks"

**Critical Security Rule:**
"Validate and sanitize inputs - Never trust input data blindly"

**What This Means for You:**
When Claude generates code or files, always review before using in production

**File Path Security:**
- Absolute paths (full paths like `/Users/you/project/file.js`) are more secure
- The course recommends using absolute paths in settings files
- Problem: Hard to share between machines

**Solution:**
Use example files with placeholders (`$PWD`) that get replaced with your actual path during setup

---

## 7. DIFFERENT TYPES OF HOOKS

### Available Hook Types

**1. Notification Hook**
- Runs when Claude needs permission to use a tool
- Runs after Claude has been idle for 60 seconds

**2. Stop Hook**
- Runs when Claude finishes responding to you

**3. SubagentStop Hook**
- Runs when a background "Task" finishes
- Tasks are displayed in the UI

**4. PreCompact Hook**
- Runs before a file/folder operation
- Can be manual or automated

### Important Technical Detail

**stdin Changes Based on Hook Type:**
Different hooks receive different information:
- `PreToolUse` and `PostToolUse` get tool information
- Other hooks get different data
- `tool_input` content differs based on which tool was called

**What This Means:**
If you want to customize hooks, you'll need to understand what data each type receives

---

## 8. PROJECT MANAGEMENT TIPS

### For Solo Developers

**Start Small:**
- Work on one feature at a time
- Give Claude focused context
- Don't try to build everything at once

**Keep Projects Organized:**
- One project = one folder
- Use clear folder names
- Keep related files together

**Document Your Decisions:**
- When Claude suggests something, note why you chose it
- Keep a simple changelog
- Will help when you return to the project later

### For 2-Person Teams

**Avoid:**
- ❌ GitHub integration (too complex for just 2 people)
- ❌ Advanced workflows
- ❌ Complex deployment pipelines

**Instead:**
- ✅ Shared folder or Dropbox
- ✅ Simple communication about who's working on what
- ✅ One person leads each feature
- ✅ Clear file naming conventions

---

## 9. COMMON MISTAKES TO AVOID

### From the Course Lessons

**1. Too Much Context**
**Mistake:** "Claude, here's my entire project - fix this bug"  
**Fix:** "Claude, the bug is in login.js - here's that file and the related auth-config.js"

**2. Not Reading Error Messages**
**Mistake:** Panic when something doesn't work  
**Fix:** Read the error, ask Claude to explain it

**3. Skipping Setup Steps**
**Mistake:** Trying to run before installing properly  
**Fix:** Follow installation steps completely

**4. Not Using Your Own Projects**
**Mistake:** Only following tutorials  
**Fix:** Apply learnings to your actual projects immediately

---

## 10. PRACTICAL WORKFLOWS

### Daily Development Flow

**Morning Routine:**
1. Open terminal
2. Navigate to project: `cd my-project`
3. Start Claude Code: `claude`
4. Tell Claude what you want to work on today

**During Work:**
1. Give Claude focused context for each task
2. Review what Claude creates
3. Test changes before moving to next task
4. Keep context minimal and relevant

**End of Day:**
1. Save your work
2. Note what worked / what didn't
3. Plan tomorrow's focus

### Working on a New Feature

**Step 1: Planning**
Tell Claude: "I want to add [feature]. What files do you need to see?"

**Step 2: Context**
Share only the files Claude asked for

**Step 3: Iteration**
Work in small steps, testing each change

**Step 4: Documentation**
Ask Claude to document what was changed

---

## 11. WHEN YOU'RE STUCK

### Common Issues & Solutions

**Issue: "Claude is suggesting code I don't understand"**  
**Solution:** Ask Claude to explain in simple terms first, then show code

**Issue: "Too many files, don't know where to start"**  
**Solution:** Ask Claude: "What's the main file I should focus on?"

**Issue: "Changes broke something"**  
**Solution:** Tell Claude what broke, share the error message

**Issue: "Don't know if I'm giving enough context"**  
**Solution:** Start minimal, add more only if Claude asks for it

---

## 12. DEFINITIONS & KEY TERMS

### Essential Concepts

**Claude Code:**
A command-line tool that helps you code with AI assistance

**Terminal:**
The text-based interface where you run commands (also called: Command Prompt on Windows, Terminal on Mac)

**Context:**
The information you give Claude about what you're working on

**Hook:**
An automated action that runs at specific times

**Tool:**
A specific action Claude can take (like TodoWrite, FileEdit, etc.)

**API Key:**
A password that lets your project connect to Claude's AI services

**stdin (Standard Input):**
The data that gets sent to a hook when it runs

**Placeholder:**
A temporary value (like `$PWD`) that gets replaced with real values

**Absolute Path:**
The complete location of a file on your computer  
Example: `/Users/goodin/projects/my-app/index.js`

**Relative Path:**
Location relative to where you currently are  
Example: `./index.js` (means: in my current folder)

---

## 13. RESOURCES & LINKS

### Official Documentation
- Quickstart: https://code.claude.com/docs/en/quickstart
- API Console: https://console.anthropic.com/
- AWS Bedrock: https://code.claude.com/docs/en/amazon-bedrock
- Google Vertex: https://code.claude.com/docs/en/google-vertex-ai

### When You Need Help
1. Check error messages first
2. Ask Claude to explain the error
3. Search official docs
4. Simplify what you're trying to do
5. Break problem into smaller pieces

---

## 14. NEXT STEPS

### For Complete Beginners

**Week 1:**
- Install Claude Code
- Run `claude` command
- Ask Claude simple questions about your project

**Week 2:**
- Practice giving Claude context
- Try asking Claude to explain your existing code
- Experiment with small changes

**Week 3:**
- Start a small new feature
- Practice the context management principles
- Document what works for you

### For Vibe Coders (You!)

**Immediate Actions:**
1. Install Claude Code on your machine
2. Pick ONE of your existing projects
3. Navigate to that project in terminal
4. Start a session: `claude`
5. Ask: "Can you help me understand the structure of this project?"

**This Week:**
- Build one small feature using Claude Code
- Practice the context management skills
- Note what questions you have

**This Month:**
- Develop your personal workflow
- Start using hooks for automation
- Create templates for your common tasks

---

## 15. YOUR SUCCESS CHECKLIST

**Setup Complete:**
- [ ] Claude Code installed
- [ ] Ran `claude` command successfully
- [ ] Authenticated with Anthropic
- [ ] Located one of my projects to work with

**Basic Skills:**
- [ ] Can navigate to project folder in terminal
- [ ] Can start Claude Code session
- [ ] Understand the importance of context management
- [ ] Know to give minimal, focused context

**Working Effectively:**
- [ ] Built at least one small feature with Claude
- [ ] Practiced breaking work into small steps
- [ ] Learned to read and understand error messages
- [ ] Developed a personal workflow

**Ready for Growth:**
- [ ] Comfortable working on multiple projects
- [ ] Starting to use hooks for automation
- [ ] Understand when to add/remove context
- [ ] Can explain Claude Code to others

---

*This guide focuses on practical application for solo developers and small teams doing "vibe coding" - knowing what to build without needing to write code from scratch.*
