# ChatGPT / OpenAI Prompting Reference

## General

Start with the smallest set of instructions that reliably defines the task. OpenAI models handle dense, explicit instructions well; extra prose is not inherently better.

Specify:
- objective
- relevant context
- available inputs
- expected output
- important constraints
- tool-use expectations when tools are available
- completion criteria for complex work

## Reasoning

Do not request hidden chain-of-thought. Avoid “think step by step” as generic prompt filler. Ask for conclusions, calculations, checks, or concise rationale when those outputs are actually useful.

## Tool-enabled ChatGPT

When a task depends on browsing, files, code execution, image generation, or other tools, explicitly state what should be verified or produced rather than assuming the model will infer the desired tool workflow.

## Structured output

When exact structure matters, provide a schema or small example. State whether additional prose is forbidden.

Example:

```text
Return JSON only using this schema:
{
  "title": "string",
  "summary": "string",
  "confidence": "high|medium|low"
}
```

## Long-context work

Provide only relevant material. Identify the authoritative source when multiple documents may conflict. State whether the model should reconcile conflicts, flag them, or prioritize a particular source.
