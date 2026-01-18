# /testing/fix-tests - Comprehensive Test Repair

**Mission Classification**: Quality Assurance & Test Repair
**Clearance Level**: Quality Engineer
**Operational Theater**: Test Suites

The `/testing/fix-tests` command deploys specialized quality engineer agents to identify and repair all failing tests in your test suite. This command ensures your codebase maintains high quality standards and test coverage.

## 🎯 Operational Capabilities

**Comprehensive Test Analysis**
- Runs entire test suite to identify failures
- Categorizes failures by type (unit, integration, e2e)
- Identifies root causes of test failures
- Prioritizes fixes based on impact and complexity

**Parallel Test Fixing**
- Deploys multiple quality-engineer agents simultaneously
- Each agent focuses on specific test failures
- Works in isolated git worktrees to prevent conflicts
- Merges fixes back to main branch

**Quality Standards Enforcement**
- Ensures tests follow best practices
- Maintains or improves test coverage
- Validates fixes don't introduce new failures
- Updates test documentation as needed

## 📋 Command Syntax

```bash
/testing/fix-tests [test_pattern] [concurrent_agents]
```

**Arguments**:
- `test_pattern` (optional): Specific test files or patterns to fix
  - Default: All tests
- `concurrent_agents` (optional): Number of agents to deploy
  - Default: `3`

## 🚀 Usage Examples

**Standard Repair Mission** - Fix all failing tests:
```bash
/testing/fix-tests
```

**Targeted Repair** - Fix specific test category:
```bash
/testing/fix-tests "**/*.integration.test.ts"
```

**High-Velocity Repair** - Deploy more agents for faster fixes:
```bash
/testing/fix-tests "" 5
```

## 💡 When to Use

**After Dependency Updates**
When package updates break existing tests

**Post-Merge**
After merging feature branches that introduce test failures

**Pre-Release**
Before deploying to ensure all tests pass

**CI/CD Failures**
When continuous integration reports test failures

**Refactoring Aftermath**
After large code refactors that affect test assumptions

## 🎖️ Best Practices

1. **Run Regularly**: Use after major changes or merges
2. **Review Fixes**: Examine what agents fixed to understand root causes
3. **Update Patterns**: If certain tests fail repeatedly, improve test design
4. **Maintain Coverage**: Ensure fixes maintain or improve coverage metrics
5. **Document Changes**: Review commit messages to understand what was fixed

## 🔗 Related Resources

**Commands:**
- [/write-implementation-plan](./write-implementation-plan.md) - Include testing tasks in plans
- [/next-priority](./next-priority.md) - Execute test-writing tasks

**Agents:**
- `quality-engineer` - Test development and coverage specialist
- `code-reviewer` - Validates test quality and coverage

**Back to:** [README](../../README.md)
