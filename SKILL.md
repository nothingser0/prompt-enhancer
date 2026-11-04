---
name: prompt-enhancer
description: Use when raw prompts need to become structured prompts.
version: 1.0.0
updated: 2026-11-04
---

# Prompt Enhancer

Transforms raw, vague user prompts into precise, structured prompts with clear roles, contexts, constraints, and verification protocols.

## Modes

1. **General Mode**: For coding, debugging, copywriting, or research prompts. Adds Role, Context, Constraints, Step-by-step Workflow, and Output Format.
2. **Lifecycle Mode**: Automatically integrates `solo-project-lifecycle` constraints, modules (M01-M13), and validation gates when building project documents or specs.

## Usage Rule
Analyze input intent. If it mentions project files, PRDs, specs, or SDLC phases, route to Lifecycle Mode. Otherwise, use General Mode.
