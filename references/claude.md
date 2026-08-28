# Claude Prompting Reference

Claude benefits from explicit instructions and relevant context, particularly on complex or agentic work.

## Complex tasks

Use clear sections when useful:

```text
<context>...</context>
<task>...</task>
<constraints>...</constraints>
<output_format>...</output_format>
```

Do not add structure when a simple request is sufficient.

## Agentic/coding work

State:
- starting state
- target state
- files/directories in scope
- areas that must remain untouched
- acceptance criteria
- verification/tests
- actions requiring approval
- stop conditions

Prevent unnecessary over-engineering with an explicit scope rule such as: only make changes directly required by the requested task; do not add unrelated abstractions or features.

## Reasoning

Do not request hidden chain-of-thought. Ask for a concise rationale or verification summary only when the user needs one.

## Long context

Front-load critical context and distinguish authoritative requirements from optional background. More context is useful only when it is relevant.
