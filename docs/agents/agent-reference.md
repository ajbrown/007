# Agent Reference Guide

This document provides comprehensive information about all available agents in Project 007.

## 🎭 Available Agents

### product-manager

**Specialization:** Requirements, Planning, Feature Prioritization

**Description:** Principal Product Manager focused on strategy, product vision, and roadmap. Ensures clear product requirements and maintains implementation plans that deliver progressive user value.

**Capabilities:**
- Requirements documentation
- Implementation planning
- Product strategy
- User experience design
- Feature prioritization
- Milestone planning

**When to Use:**
- Creating or updating implementation plans
- Defining product requirements
- Strategic planning sessions
- Feature prioritization discussions
- Roadmap planning

**Example Usage:**
```
Use the product-manager agent when you need to transform high-level product vision
into detailed, actionable implementation plans with clear milestones and priorities.
```

---

### frontend-engineer

**Specialization:** React, UI/UX, Design Systems, Accessibility

**Description:** Senior Frontend Engineer specializing in user interfaces, design systems, and React components. Delivers visually stunning, accessible, and user-friendly web applications.

**Capabilities:**
- UI/UX implementation
- React component development
- Design system management
- Accessibility compliance (WCAG 2.1 AA)
- Mobile-responsive design
- Performance optimization

**When to Use:**
- Building new UI components
- Implementing design systems
- Creating responsive layouts
- Ensuring accessibility compliance
- Optimizing frontend performance

**Example Usage:**
```
Deploy the frontend-engineer agent for implementing complex React components
with proper accessibility, responsive design, and design system integration.
```

---

### security-reviewer

**Specialization:** OWASP, Vulnerability Assessment, Penetration Testing

**Description:** Senior Application Security Engineer with deep expertise in identifying and remediating security vulnerabilities across the application stack.

**Capabilities:**
- OWASP Top 10 vulnerability assessment
- Code security audits
- Authentication and authorization review
- API security analysis
- Penetration testing
- Security best practices enforcement

**When to Use:**
- Pre-deployment security reviews
- Assessing new features for vulnerabilities
- Auditing authentication/authorization code
- API security validation
- Compliance requirements

**Example Usage:**
```
Use the security-reviewer agent before deploying new authentication features
to ensure proper implementation of security controls and identify vulnerabilities.
```

---

### quality-engineer

**Specialization:** Test Development, Coverage Analysis, Test Strategy

**Description:** Quality engineering specialist focused on building comprehensive test suites, improving test coverage, and ensuring code quality through rigorous testing practices.

**Capabilities:**
- Unit test development
- Integration test design
- E2E test implementation
- Test coverage analysis
- Test strategy planning
- Quality metrics tracking

**When to Use:**
- Writing tests for new features
- Improving test coverage
- Refactoring test suites
- Planning test strategies
- CI/CD test pipeline optimization

**Example Usage:**
```
Deploy the quality-engineer agent to develop comprehensive test coverage for
a new API endpoint, including unit, integration, and contract tests.
```

---

### code-reviewer

**Specialization:** Code Quality, Best Practices, Refactoring

**Description:** Code quality specialist focused on reviewing code for maintainability, performance, security, and adherence to best practices.

**Capabilities:**
- Code quality analysis
- Best practices enforcement
- Performance optimization suggestions
- Refactoring recommendations
- Security vulnerability detection
- Code maintainability assessment

**When to Use:**
- Pre-commit code reviews
- Refactoring guidance
- Code quality assessments
- Performance optimization reviews
- Learning best practices

**Example Usage:**
```
Use the code-reviewer agent to analyze a complex module for potential improvements
in readability, performance, and maintainability before merging to main.
```

---

### linear-scrum-master

**Specialization:** Linear Integration, Sprint Planning, Ticket Management

**Description:** Senior Product Owner and Scrum Master ensuring crisp alignment between implementation plans and Linear project management. Maintains synchronization between technical execution and project tracking.

**Capabilities:**
- Linear issue management
- Implementation plan synchronization
- Sprint planning coordination
- Story creation and updates
- Task tracking and assignment
- Project status reporting

**When to Use:**
- Syncing implementation plans with Linear
- Creating stories for planned work
- Updating ticket status
- Sprint planning sessions
- Project status reporting

**Example Usage:**
```
Deploy the linear-scrum-master agent after updating your implementation plan
to automatically create and update corresponding Linear issues.
```

---

## 🚀 Using Agents

### Automatic Deployment

Agents are automatically deployed by commands:
- `/write-implementation-plan` uses `product-manager`
- `/next-priority` uses various specialist agents based on task type
- `/testing/fix-tests` uses `quality-engineer`

### Manual Invocation

Agents can be invoked directly for specific tasks through Claude Code's conversation interface. They work autonomously with access to:
- Full codebase context
- Git history and status
- Project documentation
- Relevant tools and APIs

## 🎖️ Agent Best Practices

1. **Choose the Right Agent** - Match agent specialization to task requirements
2. **Provide Clear Context** - Give agents clear objectives and acceptance criteria
3. **Trust the Process** - Agents work autonomously; avoid micromanagement
4. **Review Outcomes** - Always review agent work before merging to production
5. **Iterate and Improve** - Provide feedback to improve future agent performance

## 📚 Related Resources

- [Commands Reference](../commands/) - Commands that deploy agents
- [README](../../README.md) - Main documentation
- [PLUGIN.md](../../PLUGIN.md) - Plugin architecture

---

**Back to:** [README](../../README.md)
