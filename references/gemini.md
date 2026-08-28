# Gemini Prompting Reference

## Grounding

For factual work, define the allowed evidence and require unsupported claims to be marked as uncertain rather than invented.

For research prompts specify:
- question
- date/freshness requirements
- preferred source types
- citation requirements
- how conflicting sources should be handled

## Multimodal work

When images, documents, audio, or video are supplied, tell Gemini exactly what information to extract and how it should relate that information to the task.

## Output locks

When formatting is important, state the format explicitly and provide a minimal example/schema. Tell the model whether explanatory text outside the requested format is allowed.

## Long context

Identify the relevant documents/sections and the decision the model must make from them. Do not treat a large context window as a reason to include irrelevant material.
