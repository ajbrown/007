# 007 - Agentic Software Delivery Workflows

```
     ___     ___    _____ 
    / _ \   / _ \  |___  |
   | | | | | | | |    / / 
   | | | | | | | |   / /  
   | |_| | | |_| |  / /   
    \___/   \___/  /_/    
                          
   CLASSIFIED: AGENT WORKFLOWS
```

> **Mission Briefing**: Your destination for advanced agentic software delivery configurations, examples, and operational intelligence.

## 🎯 Project Overview

Project 007 is a comprehensive collection of resources for orchestrating sophisticated agentic workflows in software development. This repository contains battle-tested agent definitions, workflow patterns, and operational configurations designed to enhance your software delivery capabilities.

## 🗂️ Repository Structure

```
007/
├── agents/              # Elite agent definitions tuned for specific missions
├── commands/            # Advanced operational commands and tool showcases
├── workflows/           # Complex multi-agent orchestration patterns
├── configurations/      # Operational configs and environment setups
├── examples/            # Field-tested implementation scenarios
├── documentation/       # Classified operational manuals
└── README.md           # You are here
```

## 🚀 Core Capabilities

### Agent Arsenal
- **Specialized Agents**: Each agent is precision-tuned for specific operations
- **Multi-Agent Coordination**: Orchestrate complex missions with multiple agents
- **Adaptive Workflows**: Dynamic agent selection based on mission parameters

### Workflow Patterns
- **Sequential Operations**: Chain agents for step-by-step execution
- **Parallel Deployments**: Run multiple agents simultaneously
- **Conditional Branching**: Smart routing based on outcomes
- **Error Recovery**: Built-in contingency protocols

### Configuration Management
- **Environment Templates**: Pre-configured operational environments
- **Tool Integrations**: Seamless connection to your existing arsenal
- **Security Protocols**: Built-in safety measures and access controls

## 📖 Documentation

- **[Installation & Usage](#-getting-started)** - Get started with Project 007
- **[PLUGIN.md](PLUGIN.md)** - Technical plugin architecture and development guide
- **[PUBLISHING.md](PUBLISHING.md)** - Complete guide to publishing and distributing plugins

### Command Operations
- **Advanced Tool Showcases**: Demonstration of Claude Code's full capabilities
- **Multi-Agent Orchestration**: Complex parallel and sequential agent deployments
- **Automated Workflows**: Pre-built commands for common development scenarios
- **Next Priority**: Autonomous execution of top-priority tasks from implementation plans

## 🔥 Featured Commands

### /write-implementation-plan - Strategic Mission Planning

**Mission Classification**: Strategic Planning & Architecture  
**Clearance Level**: Principal Software Engineer  
**Operational Theater**: Requirements & Specifications  

The `/write-implementation-plan` command deploys a Principal Software Engineer operative to transform your requirements and specifications into a comprehensive, battle-ready implementation plan. This strategic command creates the blueprint that `/next-priority` executes autonomously.

#### 🎯 Operational Capabilities

**Requirements Analysis**
- Deep analysis of PRD (Product Requirements Document)
- Git history review to identify recent changes
- Priority assessment based on user value and business impact

**Specification Integration**
- Subagent-driven study of technical specifications
- Cataloging specs by feature area and topic
- Automatic spec-to-task mapping for compliance tracking

**Phase & Milestone Architecture**
- Strategic phase planning (Foundation → MVP → Production Ready → Scale)
- Tactical milestone definition with clear deliverables
- Progressive value delivery at every checkpoint

**Problem-First Task Design**
- Each task starts with WHY before HOW
- Comprehensive acceptance criteria (testing, security, docs, observability)
- Skeleton implementation examples for complex tasks
- User experience obsession across all touchpoints

**Parallelization Optimization**
- Tasks designed for maximum concurrent execution
- Clear dependency chains enable intelligent sequencing
- Milestone grouping for `/next-priority` efficiency

#### 📋 Command Syntax

```bash
/write-implementation-plan [requirements_path] [plan_path] [specs_path]
```

**Arguments**:
- `requirements_path` (optional): Path to your PRD/requirements document
  - Default: `docs/reqs/main.md`
- `plan_path` (optional): Path to the implementation plan to create/update
  - Default: `docs/plans/main.md`
- `specs_path` (optional): Path to directory with implementation specifications
  - Default: `docs/specs`

#### 🚀 Usage Examples

**Standard Planning Mission** - Create plan from default requirements:
```bash
/write-implementation-plan
```

**Custom Requirements** - Different requirements document:
```bash
/write-implementation-plan docs/reqs/mvp-requirements.md
```

**Separate Plan File** - Keep multiple plans:
```bash
/write-implementation-plan docs/reqs/main.md docs/plans/sprint-3.md
```

**With Specifications** - Include technical specs:
```bash
/write-implementation-plan docs/reqs/main.md docs/plans/main.md docs/specs
```

**Full Custom Configuration**:
```bash
/write-implementation-plan docs/reqs/v2-features.md docs/plans/v2-plan.md docs/specs/v2
```

#### 💡 The Planning Workflow

**1. Transform Requirements into Action**
Your PRD describes WHAT users need. The planner analyzes WHY it matters and designs HOW to build it incrementally.

**2. Structure with Phases & Milestones**
- **Phases**: Strategic stages (Foundation, MVP, Production Ready)
- **Milestones**: Tactical deliverables within each phase
- **Tasks**: Operational units with clear acceptance criteria

**3. Specification-Driven Standards**
When specs exist, tasks automatically reference them:
- API design patterns → RESTful endpoint tasks
- Form validation standards → UI form tasks
- Security requirements → Authentication tasks

**4. Parallel Execution Ready**
Tasks are designed with `/next-priority` in mind—clear dependencies, proper grouping, maximum parallelization opportunities.

#### 🔄 The Complete Workflow: Plan → Execute → Iterate

**The Autonomous Development Cycle:**

```bash
# Phase 1: Strategic Planning
/write-implementation-plan docs/reqs/main.md docs/plans/main.md docs/specs

# Phase 2: Autonomous Execution
/next-priority docs/plans/main.md 3

# Phase 3: Review & Adjust
# Review completed milestone, provide feedback, adjust plan

# Phase 4: Continue Execution
/next-priority docs/plans/main.md 3

# Repeat until phase/milestone complete, then review before next phase
```

**Key Workflow Principles:**
- **Plan First**: Create comprehensive implementation plan with phases and milestones
- **Execute by Milestone**: Use `/next-priority` to execute tasks within current milestone
- **Review at Boundaries**: Review and course-correct between milestones and phases
- **Iterate Continuously**: Update plan based on learnings, repeat cycle

#### ⚡ The Power of Strategic Planning

**Without /write-implementation-plan:**
> "Let's build user authentication. Uh... where do we start? What about the database? Oh wait, we need to decide on the auth library first. And what about password reset? Should that be in this PR or separate? How do we test this? When do we write docs?"

**With /write-implementation-plan:**
> **Phase 2: MVP Launch**
> 
> **Milestone 2.1: User Authentication System**
> - [TASK-015] Database schema for users and sessions (follows db-design-spec.md)
> - [TASK-016] Auth library integration with JWT (follows api-security-spec.md)
> - [TASK-017] Login/logout endpoints with rate limiting
> - [TASK-018] Password reset flow with email notifications
> - [TASK-019] Unit tests achieving 80% coverage
> - [TASK-020] E2E authentication tests
> - [TASK-021] User documentation for account management
> - [TASK-022] Security review and penetration testing
> 
> All tasks parallelizable except 016→017. Deploy with: `/next-priority docs/plans/main.md 3`

Clear direction. No ambiguity. Maximum velocity.

#### 🎖️ Best Practices

1. **Start with Requirements**: Write clear requirements before planning implementation
2. **Leverage Specifications**: Create specs for patterns you'll use repeatedly (API design, validation, etc.)
3. **Think in Milestones**: Each milestone should be a demonstrable, potentially shippable deliverable
4. **Design for Parallelization**: Structure tasks so `/next-priority` can maximize concurrency
5. **Review and Iterate**: Update the plan as you learn—it's a living document
6. **Celebrate Milestones**: Mark phase/milestone completion before moving to the next

### /next-priority - The Ultimate Force Multiplier

**Mission Classification**: Elite Autonomous Task Execution  
**Clearance Level**: Senior Software Engineer  
**Operational Theater**: Implementation Plans  

The `/next-priority` command is your secret weapon for accelerating development velocity. This command deploys an elite senior software engineer operative who autonomously identifies, prioritizes, and executes multiple high-value tasks from your implementation plan—all while you focus on strategic initiatives.

#### 🎯 Operational Capabilities

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

#### 📋 Command Syntax

```bash
/next-priority [implementation_plan_path] [concurrent_tasks]
```

**Arguments**:
- `implementation_plan_path` (optional): Path to your implementation plan
  - Default: `docs/plans/main.md`
- `concurrent_tasks` (optional): Number of tasks to execute in parallel
  - Default: `3`
  - Range: `1` to `N` (limited by system resources)

#### 🚀 Usage Examples

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

#### 💡 Strategic Applications

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

#### ⚡ The Power of Autonomous Execution

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

#### 🎖️ Best Practices

1. **Structure Your Plans**: Use `/write-implementation-plan` to create well-defined tasks with clear acceptance criteria
2. **Respect Boundaries**: `/next-priority` works within current milestone/phase only—review before advancing
3. **Manage Dependencies**: Mark dependent tasks clearly so the operative can sequence properly  
4. **Start Conservative**: Begin with 1-3 concurrent tasks until you understand the workflow
5. **Monitor Progress**: Check the implementation plan periodically for status updates
6. **Validate Outcomes**: Review completed milestones before advancing to the next phase
7. **Iterate and Improve**: Refine your plans based on what works and what doesn't

## 🎭 Featured Agents

- **code-reviewer**: Security and quality analysis specialist
- **test-runner**: Automated testing and validation operative
- **frontend-engineer**: UI/UX implementation expert
- **product-manager**: Strategic planning and coordination
- **security-reviewer**: Vulnerability assessment specialist
- **And more classified operatives...**

## 📡 Getting Started

### Mission Prerequisites
- Claude Code (claude.ai/code) access
- Basic understanding of agentic workflows
- Security clearance (just kidding, it's open source!)

### Installation

#### Option 1: Install from GitHub (Recommended)
```bash
claude plugin install ajbrown/007
```

#### Option 2: Install from Local Clone
```bash
# Clone the repository
git clone https://github.com/ajbrown/007.git

# Install as a plugin
claude plugin install /path/to/007
```

#### Option 3: Install from URL
```bash
claude plugin install https://github.com/ajbrown/007
```

### Verify Installation
```bash
# List installed plugins
claude plugin list

# You should see "project-007" in the list
```

### Using the Plugin

Once installed, Project 007's commands and agents are available in your Claude Code sessions:

#### Command Operations
```bash
# Strategic planning - create implementation plan
/write-implementation-plan

# Autonomous execution - work the plan
/next-priority

# Comprehensive test fixing
/testing/fix-tests
```

#### Agent Deployment
Use agents in your conversations via the Task tool:

```yaml
Task:
  subagent_type: code-reviewer
  description: Review critical security updates
  prompt: Analyze the authentication module for vulnerabilities
```

**Available Agents:**
- `code-reviewer` - Code quality and security analysis
- `security-reviewer` - Comprehensive security assessments
- `frontend-engineer` - UI/UX implementation
- `product-manager` - Requirements and planning
- `quality-engineer` - Test development and coverage
- `linear-scrum-master` - Linear project sync

### Update the Plugin
```bash
claude plugin update project-007
```

### Uninstall
```bash
claude plugin uninstall project-007
```

## 🔧 Contributing

New recruits welcome! When contributing:
1. Follow the established agent definition format
2. Document your workflows thoroughly
3. Test in isolated environments first
4. Submit via secure channels (pull requests)

### Plugin Development

**Directory Structure:**
```
007/
├── .claude-plugin/
│   └── plugin.json      # Plugin manifest
├── agents/              # Agent definitions (*.md)
├── commands/            # Command definitions (*.md)
├── LICENSE             # MIT License
└── README.md
```

**Agent Format:**
```markdown
---
description: What this agent does and when to use it
capabilities:
  - Capability 1
  - Capability 2
---

# Agent Name
Detailed instructions and operational guidelines
```

**Command Format:**
```markdown
---
description: What this command does
arguments:
  - name: arg_name
    description: Argument description
    default: default_value
    required: false
---

# Command Name
Detailed command instructions and usage
```

### Publishing Your Fork

If you fork this plugin and want to publish it:

1. Update `.claude-plugin/plugin.json` with your details:
   ```json
   {
     "name": "your-plugin-name",
     "author": {
       "name": "Your Name",
       "email": "your@email.com",
       "url": "https://github.com/yourusername"
     },
     "repository": "https://github.com/yourusername/your-repo"
   }
   ```

2. Commit and push to your GitHub repository

3. Users can install with:
   ```bash
   claude plugin install yourusername/your-repo
   ```

## 📚 Documentation

Detailed operational manuals available in the `documentation/` directory:
- Agent Creation Guide
- Workflow Orchestration Patterns
- Best Practices & Conventions
- Troubleshooting Protocols

## ⚡ Quick Links

- [Agent Catalog](./agents/)
- [Command Operations](./commands/)
- [Workflow Library](./workflows/)
- [Example Missions](./examples/)
- [Configuration Templates](./configurations/)

---

```
REMEMBER: WITH GREAT AGENTS COMES GREAT RESPONSIBILITY
```

*This project is licensed for peaceful software development purposes only.*