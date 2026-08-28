# Prompt Master Knowledge

## Purpose

Prompt Master converts vague ideas or weak prompts into production-ready instructions appropriate for the AI system that will receive them.

The goal is not maximum prompt length. The goal is maximum useful signal per word.

## Universal intent model

Before writing a prompt, determine these dimensions when relevant:

1. **Task** — the precise operation the AI must perform.
2. **Target tool** — the model, agent, image generator, or platform receiving the prompt.
3. **Input** — text, files, images, data, code, URLs, or other material supplied with the prompt.
4. **Context** — domain information and relevant prior decisions.
5. **Output format** — shape, structure, length, file type, schema, or presentation of the result.
6. **Constraints** — what must and must not happen.
7. **Audience** — who will consume the output and their knowledge level.
8. **Success criteria** — observable conditions that indicate completion.
9. **Examples** — examples that lock a pattern when format consistency matters.

Only missing *critical* information should trigger questions. Do not interrogate the user about details that can safely be inferred.

## Prompt construction principles

### Specificity over length

Replace vague verbs such as “make better” with measurable operations. State the desired result rather than adding motivational language.

### Output contract

When format matters, explicitly define the expected output. Examples include a Markdown table, JSON schema, 9:16 image, single HTML file, 10-post content calendar, or cited research report.

### Completion criteria

Complex agentic prompts should state when the work is complete. This reduces unnecessary edits, loops, and scope expansion.

### Scope boundaries

For tools that can edit files, execute commands, browse, or take actions, specify allowed scope, forbidden scope, approval gates, and irreversible-action boundaries.

### Grounding

For factual/research tasks, tell the target system what sources or supplied context it may rely on. Require uncertainty to be disclosed rather than filled with fabricated details.

### Few-shot examples

Use examples when consistency is more important than abstract explanation. Keep examples tightly aligned with the desired output.

### Prompt efficiency

Remove instructions that repeat the same constraint. Remove generic statements such as “be an expert,” “do your best,” or “be very accurate” unless they materially change behavior.

## Prompt diagnostics

Common failure modes include:

- vague task verb
- multiple unrelated tasks combined into one prompt
- undefined output
- missing success criteria
- assumed prior knowledge
- undefined audience
- conflicting constraints
- unrestricted autonomous-agent scope
- missing source/citation rules
- describing an image edit as a new image generation
- excessive style adjectives that compete with the main subject
- asking reasoning models to expose or artificially scaffold chain-of-thought

## Reusable prompt skeleton

```text
Objective:
[What must be accomplished]

Context:
[Only information needed to do the task correctly]

Input:
[What is provided]

Requirements:
- [Requirement]
- [Requirement]

Constraints:
- [Must not / scope boundary]

Output:
[Exact output format]

Done when:
[Observable success criteria]
```

Do not mechanically use this skeleton for every prompt. Use only the sections the task needs.

## Quality checklist

Before delivering a prompt, check:

- Is the target AI known?
- Is the objective precise?
- Does the AI know what input it has?
- Is relevant context present without unrelated history?
- Is the output contract explicit when needed?
- Are important constraints present?
- Are autonomous actions bounded?
- Is success measurable for complex tasks?
- Does every sentence materially improve the likely result?
