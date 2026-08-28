# Coding Agent Prompting Reference

Coding agents can inspect files, edit code, run commands, test changes, and sometimes browse. Good prompts bound that autonomy.

## Required dimensions for complex edits

```text
Objective:
[desired behavior]

Starting state:
[current behavior/problem]

Scope:
[files/directories allowed]

Do not touch:
[explicit exclusions]

Requirements:
[implementation constraints]

Verification:
[tests/checks]

Done when:
[acceptance criteria]

Approval gates:
[actions requiring user confirmation]
```

## Scope

Anchor edits to known files/directories when possible. Avoid “fix the whole codebase” unless that is truly the intended task.

## Destructive actions

Require confirmation before actions such as deleting files/data, changing database schemas, modifying production infrastructure, adding significant dependencies, or performing irreversible external actions when those are not already explicitly authorized.

## Acceptance criteria

Prefer observable criteria: existing tests pass, a specified endpoint returns the expected response, UI renders at required breakpoints, no new lint/type errors, or a reproduction case no longer fails.

## Prevent scope creep

Tell the agent not to add unrelated features, abstractions, refactors, dependencies, or files.

## Cursor / Windsurf-style edits

Include file path, relevant symbol/function/component, current behavior, desired behavior, do-not-touch list, and “done when.” Split unrelated complex changes into sequential prompts.

## Autonomous agents

State the target outcome and permission boundaries. Include stop conditions so the agent does not repeatedly revise a solution after the acceptance criteria have been met.
