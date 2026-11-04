---
name: prompt-enhancer
description: Use when raw prompts need to become structured prompts.
version: 1.1.0
updated: 2026-11-04
---

# Prompt Enhancer

Transforms raw, vague user prompts into precise, structured prompts with clear roles, contexts, constraints, and verification protocols.

## Modes

1. **General Mode**: For coding, debugging, copywriting, or research prompts. Adds:
   - **Role & Identity**: AI persona and domain expertise.
   - **Context & Goal**: Problem background and objective.
   - **Constraints**: Hard rules (what to do and what NOT to do).
   - **Step-by-Step Workflow**: Execution sequence.
   - **Output Format**: Precise schema or structure for results.

2. **Lifecycle Mode**: Automatically integrates `solo-project-lifecycle` constraints, modules (M01-M13), and validation gates when building project documents or specs.
   - Automatically references framework templates (`docs/modules/`, `templates/`).
   - Enforces gate scripts and verification protocols before sign-off.

## Templates & Examples

### General Mode Template
```markdown
Role: [Expert Persona]
Task: [Precise Objective]
Context: [Background]
Constraints: [Rules / What to avoid]
Workflow:
1. ...
2. ...
Output Format: [Markdown / Code / JSON]
Input: [Raw prompt here]
```

### Lifecycle Mode Template
```markdown
Role: Solo Project Architect & SDLC Enforcer
Task: Generate compliant artifact for Module [M01-M13]
Framework: solo-project-lifecycle
Rules: Follow official template, enforce validation gate, check downstream consistency.
Input Idea: [Raw feature / request]
```
