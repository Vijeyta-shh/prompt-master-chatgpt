# Prompt Architectures

Frameworks are tools, not mandatory output formats. Select the lightest architecture that fits the task and do not show framework names unless the user asks.

## Minimal task contract

Best for straightforward work:

```text
Do [specific task].
Input: [input]
Return: [output]
Constraints: [only critical constraints]
```

## Context / Objective / Requirements / Output

Best for business, content, and professional deliverables:

```text
Context:
...

Objective:
...

Requirements:
...

Output:
...
```

## Agentic implementation contract

Best for coding/computer-use agents:

```text
Goal:
...

Starting state:
...

Scope:
...

Allowed actions:
...

Forbidden actions:
...

Acceptance criteria:
...

Verification:
...

Stop conditions:
...
```

## Few-shot pattern lock

Best when the output must consistently imitate a structural pattern. Provide 2–5 tightly relevant input/output examples and then the new input. Avoid examples that contradict the written rules.

## Grounded research contract

```text
Research question:
...

Scope/date range:
...

Source requirements:
...

Rules:
- Cite factual claims.
- Distinguish facts from interpretation.
- Flag uncertainty or conflicting evidence.

Deliverable:
...
```

## Visual descriptor

Best for image generation:

```text
[subject], [environment], [composition], [style], [lighting], [mood], [camera/details], [parameters]
```

## Reference-image edit contract

```text
Use the supplied image as the source.

Change:
...

Preserve:
...

Final appearance:
...
```

## Prompt decompilation

When improving an existing prompt:
1. identify its intended result
2. preserve useful constraints
3. remove redundancy/conflict
4. add missing critical information
5. adapt syntax/structure to the target tool
6. return one clean replacement prompt
