# Project 007 - Elite Multi-Agent Development Plugin Marketplace

```
     ___     ___    _____
    / _ \   / _ \  |___  |
   | | | | | | | |    / /
   | | | | | | | |   / /
   | |_| | | |_| |  / /
    \___/   \___/  /_/

   ACCELERATE YOUR VELOCITY
```

> Transform your solo development workflow into an elite multi-agent operation. Let AI agents handle the repetitive work while you focus on architecture and innovation.

## 💡 The Problem

You're a skilled engineer, but you're constantly context-switching between:
- Writing requirements → Planning implementation → Coding → Testing → Documenting
- Bouncing between 5 open files trying to keep patterns consistent
- Writing the same boilerplate for the 47th time this month
- Waiting for CI to tell you about that test you forgot to update

**Sound familiar?** You need force multipliers, not more coffee.

## ✨ The Solution

Project 007 gives you a team of specialized AI agents that work autonomously:

- **Strategic Planner** - Transforms requirements into detailed, executable implementation plans
- **Autonomous Executor** - Deploys 3+ agents simultaneously to knock out tasks in parallel
- **Quality Assurance** - Runs comprehensive test suites and fixes failing tests automatically
- **Specialized Engineers** - Frontend, security, testing specialists available on-demand

### Real Example: What You Get

**Before Project 007:**
```bash
You: "I need to implement user authentication"
Claude: "Sure! Let me write that for you..."
[2 hours later, you have code but no tests, incomplete docs, and security gaps]
```

**After Project 007:**
```bash
You: /write-implementation-plan
# Creates: 15 discrete tasks with acceptance criteria, dependencies, specs

You: /next-priority docs/plans/main.md 3
# Spawns 3 agents:
#   Agent 1: Database schema + migrations
#   Agent 2: API endpoints + rate limiting
#   Agent 3: UI components + validation
# [All complete in ~45 minutes with tests, docs, security review]

You: *Goes to lunch feeling like a 10x engineer*
```

**Productivity multiplier:** 3-5x on well-defined tasks.

---

## 🚀 Quick Start (5 Minutes)

### 1. Add the Marketplace & Install Plugin

```bash
# Add the 007 marketplace
/plugin marketplace add ajbrown/007

# Install the ajentic plugin
/plugin install ajentic@007
```

**Verify installation:**
```bash
claude plugin list
# You should see "ajentic" in the output
```

### 2. Try Your First Command

Open Claude Code and run:

```bash
/write-implementation-plan
```

This creates an implementation plan from your requirements. (Don't have requirements yet? That's fine—it'll help you create them!)

### 3. Experience the Force Multiplier

```bash
/next-priority
```

Watch as 3 AI agents simultaneously execute tasks from your plan. Each agent:
- Works in isolated git worktrees (no conflicts!)
- Writes tests for their changes
- Updates documentation
- Merges back to main when complete

---

## 📦 What's Included

### 🎯 Commands (Your Mission Control)

| Command | What It Does | When to Use |
|---------|-------------|-------------|
| `/write-implementation-plan` | Transforms requirements into detailed execution plans with phases, milestones, and parallelizable tasks | Start of sprint, new feature, refactor planning |
| `/next-priority` | Deploys 1-N AI agents to autonomously execute top-priority tasks in parallel | After planning, during sprints, for autonomous execution |
| `/testing/fix-tests` | Runs test suite, identifies failures, deploys agents to fix all failing tests | After merges, during CI troubleshooting, pre-release |

### 🎭 Agents (Your Specialist Team)

These specialized agents work autonomously or can be invoked on-demand:

| Agent | Specialization | Example Use |
|-------|---------------|-------------|
| `product-manager` | Requirements, planning, feature prioritization | Strategic planning, roadmap creation |
| `frontend-engineer` | React, UI/UX, design systems, accessibility | Building interfaces, component work |
| `security-reviewer` | OWASP, vulnerability assessment, penetration testing | Security audits, pre-deployment reviews |
| `quality-engineer` | Test development, coverage analysis, test strategy | Writing tests, improving test quality |
| `code-reviewer` | Code quality, best practices, refactoring | PR reviews, code quality checks |
| `linear-scrum-master` | Linear integration, sprint planning, ticket management | Syncing Linear with implementation plans |

**Note:** Agents are deployed automatically by commands, but you can also invoke them directly for specific tasks.

---

## 📖 Core Workflow: Plan → Execute → Ship

### The Autonomous Development Cycle

```bash
# 1. PLAN - Create your strategic implementation plan
/write-implementation-plan docs/reqs/main.md docs/plans/sprint-5.md

# 2. EXECUTE - Deploy autonomous agents to work the plan
/next-priority docs/plans/sprint-5.md 3

# 3. REVIEW - Check the completed milestone, provide feedback
# (Review the PRs, test the functionality, gather learnings)

# 4. ITERATE - Continue execution or update plan based on learnings
/next-priority docs/plans/sprint-5.md 3

# 5. VALIDATE - Ensure quality before shipping
/testing/fix-tests

# 6. SHIP - Deploy with confidence
git push origin main
```

### Key Principles

1. **Plan in Milestones** - Each milestone should be demonstrable and valuable
2. **Execute in Parallel** - Let agents handle independent tasks simultaneously
3. **Review at Boundaries** - Check work between milestones, not constantly
4. **Iterate Continuously** - Update plans as you learn, repeat the cycle

---

## 💎 When to Use Project 007

### ✅ Perfect For

- **Feature Development** - Turn requirements into working code fast
- **Technical Debt** - Systematically eliminate debt with parallel execution
- **Testing Initiatives** - Boost coverage with dedicated test-writing agents
- **Refactoring Projects** - Break down large refactors into safe, discrete tasks
- **Documentation Sprints** - Update docs across your codebase efficiently
- **Prototyping** - Rapidly build MVPs with multi-agent parallelization

### ⚠️ Not Ideal For

- **Exploratory Coding** - When you're not sure what to build yet
- **Learning New Tech** - When you need to understand deeply, not just ship
- **Single-File Changes** - Overhead isn't worth it for trivial edits
- **Highly Coupled Work** - Tasks with complex interdependencies

---

## 🎓 Learning Resources

### For Beginners

**New to Claude Code?**
- [Claude Code Documentation](https://code.claude.com/docs)
- Start with `/write-implementation-plan` to see how planning works
- Use concurrency=1 for `/next-priority` until you understand the workflow

**New to Agentic Workflows?**
- Think of agents as specialized team members who work autonomously
- Each agent has specific skills and works on isolated tasks
- You provide direction, agents handle execution and details

### For Advanced Users

- **[PLUGIN.md](./PLUGIN.md)** - Technical architecture and plugin development
- **[PUBLISHING.md](./PUBLISHING.md)** - Publishing and distribution guide
- **[/write-implementation-plan Deep Dive](./docs/commands/write-implementation-plan.md)** - Complete planning guide
- **[/next-priority Deep Dive](./docs/commands/next-priority.md)** - Advanced execution patterns
- **[/testing/fix-tests Reference](./docs/commands/fix-tests.md)** - Test repair guide

---

## 🔧 Configuration & Customization

### Adjusting Concurrency

Start conservative (1-3 agents), increase as you get comfortable:

```bash
# Conservative - one task at a time
/next-priority docs/plans/main.md 1

# Balanced - most common usage
/next-priority docs/plans/main.md 3

# Aggressive - for highly parallelizable work
/next-priority docs/plans/main.md 5
```

### Custom Paths

All commands support custom paths:

```bash
# Custom requirements and plan locations
/write-implementation-plan docs/reqs/v2.md docs/plans/v2-plan.md

# Different implementation plans for different initiatives
/next-priority docs/plans/frontend-work.md 3
/next-priority docs/plans/backend-work.md 2
```

### Integration with Your Workflow

Project 007 works alongside your existing tools:
- **Linear** - Use `linear-scrum-master` agent for ticket sync
- **Git** - All work happens in proper branches with clean commits
- **CI/CD** - Agents respect your test suite and linting rules
- **Code Review** - Work is organized into reviewable PRs

---

## 🆘 Troubleshooting

### "The agents aren't working as expected"

- **Check your implementation plan** - Agents need clear acceptance criteria
- **Review dependencies** - Ensure task dependencies are correctly marked
- **Start with concurrency=1** - Debug with sequential execution first
- **Check git status** - Ensure you have a clean working directory

### "I'm not seeing the plugin commands"

```bash
# Verify plugin is installed
claude plugin list

# Reinstall if needed
claude plugin uninstall ajentic
/plugin marketplace add ajbrown/007
/plugin install ajentic@007
```

### "Tasks aren't completing properly"

- Ensure acceptance criteria are specific and measurable
- Check that required files/dependencies exist in your project
- Review agent output for blockers or errors
- Try smaller, more focused tasks

---

## 🤝 Contributing

Contributions welcome! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

**Ways to contribute:**
- Add new specialized agents
- Improve existing commands
- Share your workflows and patterns
- Report issues or suggest enhancements

---

## 📄 License

MIT License - See [LICENSE](./LICENSE) for details.

---

## ⚡ Quick Links

- **[Installation](#-quick-start-5-minutes)** - Get started in 5 minutes
- **[Core Workflow](#-core-workflow-plan--execute--ship)** - Learn the development cycle
- **[Commands Reference](#-commands-your-mission-control)** - Available commands
- **[Agents Reference](#-agents-your-specialist-team)** - Available agents
- **[PLUGIN.md](./PLUGIN.md)** - Technical documentation
- **[PUBLISHING.md](./PUBLISHING.md)** - Distribution guide
- **[GitHub Issues](https://github.com/ajbrown/007/issues)** - Bug reports & features

---

```
"The name's Code... Claude Code." 🍸

Built with ❤️ for developers who want to ship faster.
```

**Marketplace Version:** 1.0.0 | **Plugin: ajentic** v1.0.0
**Last Updated:** 2026-02-18
