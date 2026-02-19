---
description: Runs tests and fixes all failing tests using parralel subagents.
---

Your task is to ensure the tests for this project are passing. After running the test suite, you
will use subagents to fix any failing tests by either correcting the code or by fixing the test
itself (where appropriate). You'll continue running tests and fixing them until all tests are
passing.

## YOUR PROCESS

1. Use the test-runner subagent to run the full test suite.
2. Develop a plan to fix each of the failing test. Think hard about the logical grouping of the code
   under test for each failing test. Group related tests and tests from the same suite into a single
   task.
3. For every test fix task from the plan, use the quality-engineer subagent to work through the task
   and fix the failing tests. Use up to 5 parallel quality-engineer subagents to work on test
   failure fixes.
4. As each parallel quality-engineer subagent completes, replace it with another subagent to pick up
   the next task in the plan. Continue this pattern until all tasks are complete.

## TASK WORKFLOW

- Each subagent must use a new git worktree in a /tmp directory to perform it's work. Prefix the
  name of each worktree with `fix/`.
- When fixing a test, DO NOT ASSUME THE TEST IS WRONG! think hard about the failure, and what it's
  attempting to test, and whether it's the test that is incorrect, or the code that it's testing is
  in fact incorrect.
- As you find common patterns or problems with the tests causing failures, document them in
  @docs/specs/testing-patterns.md . For example, if you find that more than one test is failing
  because we're not properly instantiating a certain class, make a note of that and document the bad
  behavior versus the corrected behavior.
- IMPORTANT: Once the tests and code for a subagent is fixed, immediately commit the changes, then
  do a `git commit --no-gpg-sign` with a message that describes the changes you made to the code in
  your git worktree.
- Once all subagents are complete, ensure their changes are pulled into the main repository path
  that the worktrees were created from by doing a `git merge --ff-only` of the worktree/branch. If
  fast-forward merge is not possible, you will need to do a simple `git merge`, and resolve merge
  conflicts if they arise. Once all changes are incorporated into the main tree, remove each
  subagent's worktree.

## IMPORTANT

- Do not create mock, fake, or alternative classes, methods, or functions just to get a test
  passing. You may use mocking utilities to mock implementations where appropriate (as is standard
  testing practice), but you may _not_ create useless implementations in the main code just to get a
  test to pass. If you feel that an implementation cannot be tested or mocked as is, think hard
  about the best way to refactor it without creating test-only code that lives in the main code.
