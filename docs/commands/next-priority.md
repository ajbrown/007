# /next-priority - The Ultimate Force Multiplier

**Mission Classification**: Elite Autonomous Task Execution
**Clearance Level**: Senior Software Engineer
**Operational Theater**: Implementation Plans

The `/next-priority` command is your secret weapon for accelerating development velocity. This command deploys an elite senior software engineer operative who autonomously identifies, prioritizes, and executes multiple high-value tasks from your implementation plan—all while you focus on strategic initiatives.

## 🎯 Operational Capabilities

**Intelligent Task Selection**
- Analyzes your entire implementation plan for priority, dependencies, and business value
- Automatically sequences dependent tasks to prevent conflicts
- Adapts to changing priorities and discovered complexities

**Parallel Multi-Agent Deployment**
- Spawns multiple specialized subagents working simultaneously
- Each agent operates in isolated git worktrees for clean separation
- Configurable concurrency from 1 (sequential) to N (parallel blitz)

**Quality Enforcement Protocol**
- Deploys quality-engineer subagents for comprehensive test coverage
- Runs test-runner subagents to validate changes don't break existing functionality
- Enforces acceptance criteria validation before marking tasks complete

**Autonomous Integration Pipeline**
- Creates feature branches with descriptive naming conventions
- Commits changes with meaningful messages
- Merges completed work via fast-forward when possible
- Handles merge conflicts intelligently when necessary
- Cleans up worktrees after successful integration

**Live Progress Intelligence**
- Marks tasks "in progress" when work begins
- Updates implementation plan with discoveries and learnings
- Marks tasks complete only after acceptance criteria validation
- Archives completed tasks to keep plans manageable

## 📋 Command Syntax

```bash
/next-priority [implementation_plan_path] [concurrent_tasks]
```

**Arguments**:
- `implementation_plan_path` (optional): Path to your implementation plan
  - Default: `docs/plans/main.md`
- `concurrent_tasks` (optional): Number of tasks to execute in parallel
  - Default: `3`
  - Range: `1` to `N` (limited by system resources)

## 🚀 Usage Examples

**Standard Mission** - Execute 3 tasks from default plan:
```bash
/next-priority
```

**Focused Assault** - Work one task at a time for complex dependencies:
```bash
/next-priority docs/plans/main.md 1
```

**Blitz Operation** - Maximum parallelization for independent tasks:
```bash
/next-priority docs/plans/main.md 5
```

**Custom Intelligence** - Different implementation plan:
```bash
/next-priority docs/plans/sprint-2.md 3
```

**Rapid Prototyping** - High concurrency on experimental plan:
```bash
/next-priority docs/plans/prototype.md 7
```

## 💡 Strategic Applications

**Sprint Acceleration**
Deploy at sprint start to knock out foundational tasks while your team tackles complex features.

**Technical Debt Elimination**
Point at a technical debt plan and let the operative systematically clean up your codebase.

**Documentation Sprints**
Create a documentation-focused plan and execute comprehensive doc updates in parallel.

**Test Coverage Campaigns**
Generate a test-writing plan and deploy multiple agents to boost coverage rapidly.

**Refactoring Operations**
Break down large refactors into discrete tasks and execute them with surgical precision.

## ⚡ The Power of Autonomous Execution

Imagine this scenario:

> **Monday 9 AM**: You create an implementation plan with 15 tasks for your new feature.
> **Monday 9:15 AM**: You run `/next-priority docs/plans/new-feature.md 3`
> **Monday 9:16 AM**: Three subagents spin up, each in isolated worktrees:
> - Agent 1: Implementing the data model
> - Agent 2: Creating API endpoints
> - Agent 3: Building the UI components
>
> **Monday 11 AM**: All three tasks complete with tests, documentation, and validation. Merged to main.
> **Monday 11:05 AM**: `/next-priority` automatically selects the next 3 tasks and continues.
> **Monday 3 PM**: 12 of 15 tasks complete. You review the work and guide the final 3 tasks.
> **Monday 5 PM**: Feature complete, tested, and ready for staging deployment.

This isn't science fiction. This is the force multiplier effect of intelligent agent orchestration.

## 🎖️ Best Practices

1. **Structure Your Plans**: Use `/write-implementation-plan` to create well-defined tasks with clear acceptance criteria
2. **Respect Boundaries**: `/next-priority` works within current milestone/phase only—review before advancing
3. **Manage Dependencies**: Mark dependent tasks clearly so the operative can sequence properly
4. **Start Conservative**: Begin with 1-3 concurrent tasks until you understand the workflow
5. **Monitor Progress**: Check the implementation plan periodically for status updates
6. **Validate Outcomes**: Review completed milestones before advancing to the next phase
7. **Iterate and Improve**: Refine your plans based on what works and what doesn't

## 🔗 Related Resources

**Commands:**
- [/write-implementation-plan](./write-implementation-plan.md) - Create the plan first
- [/testing/fix-tests](./fix-tests.md) - Validate implementation quality

**Agents Used:**
- See [Agent Reference](../agents/agent-reference.md) for all available specialists

**Back to:** [README](../../README.md)
