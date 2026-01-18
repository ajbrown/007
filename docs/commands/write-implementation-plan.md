# /write-implementation-plan - Strategic Mission Planning

**Mission Classification**: Strategic Planning & Architecture
**Clearance Level**: Principal Software Engineer
**Operational Theater**: Requirements & Specifications

The `/write-implementation-plan` command deploys a Principal Software Engineer operative to transform your requirements and specifications into a comprehensive, battle-ready implementation plan. This strategic command creates the blueprint that `/next-priority` executes autonomously.

## 🎯 Operational Capabilities

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

## 📋 Command Syntax

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

## 🚀 Usage Examples

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

## 💡 The Planning Workflow

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

## 🔄 The Complete Workflow: Plan → Execute → Iterate

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

## ⚡ The Power of Strategic Planning

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

## 🎖️ Best Practices

1. **Start with Requirements**: Write clear requirements before planning implementation
2. **Leverage Specifications**: Create specs for patterns you'll use repeatedly (API design, validation, etc.)
3. **Think in Milestones**: Each milestone should be a demonstrable, potentially shippable deliverable
4. **Design for Parallelization**: Structure tasks so `/next-priority` can maximize concurrency
5. **Review and Iterate**: Update the plan as you learn—it's a living document
6. **Celebrate Milestones**: Mark phase/milestone completion before moving to the next

---

**Related Commands:**
- [/next-priority](./next-priority.md) - Execute the plan with autonomous agents
- [/testing/fix-tests](./fix-tests.md) - Validate implementation quality

**Back to:** [README](../../README.md)
