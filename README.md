# Prompt Master for ChatGPT

A ChatGPT-optimized adaptation of the public `nidhinjs/prompt-master` project.

This repository is designed for use with a Custom GPT. It separates the short behavior instructions required by ChatGPT's 8,000-character instruction limit from longer reference material that can be uploaded as Knowledge.

## Setup

1. Open the ChatGPT GPT Builder.
2. Create or edit your GPT.
3. Copy the contents of `GPT-INSTRUCTIONS.md` into the **Instructions** field.
4. Upload `PROMPT-MASTER-KNOWLEDGE.md` and the files in `references/` as **Knowledge**.
5. Enable Web Search, Image Generation, and Code Interpreter/Data Analysis if available and useful.
6. Save the GPT.

## Suggested GPT configuration

**Name:** Prompt Master AI

**Description:** Creates precise, efficient prompts optimized for ChatGPT, Claude, Gemini, Perplexity, image/video AI, and coding agents.

### Suggested conversation starters

- Create a prompt for ChatGPT
- Optimize this prompt for Claude
- Turn this idea into a Midjourney prompt
- Make this prompt work better with Gemini
- Convert this prompt for Perplexity
- Create a prompt for an AI coding agent

## Repository structure

- `GPT-INSTRUCTIONS.md` — short governing instructions for the GPT Builder
- `PROMPT-MASTER-KNOWLEDGE.md` — general reference knowledge
- `references/chatgpt.md` — ChatGPT/OpenAI prompting guidance
- `references/claude.md` — Claude prompting guidance
- `references/gemini.md` — Gemini prompting guidance
- `references/image-ai.md` — image generation/editing guidance
- `references/video-ai.md` — video prompting guidance
- `references/coding-agents.md` — coding-agent guidance
- `references/prompting-frameworks.md` — reusable prompt architectures

## Notes

This is an adaptation for ChatGPT, not a direct installable Claude Skill. The original project is MIT licensed; check the upstream repository for the latest version and license terms.
