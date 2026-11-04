# Prompt Enhancer

A modular, production-grade prompt engineering toolkit that transforms raw, vague user inputs into structured, rigorous LLM instructions.

## Features

- **Dual Mode Support**:
  - **General Mode**: Optimizes prompts for coding, debugging, copywriting, and architecture design by injecting Role, Context, Constraints, Step-by-Step Workflow, and Output Format.
  - **Lifecycle Mode**: Automatically integrates with `solo-project-lifecycle` framework to generate compliant module specs, docs, and gate verification checklists (M01–M13).
- **Anti-Hallucination & Verification Protocol**: Enforces pre-flight checks, explicit evidence reporting, and strict output schemas.

## Usage

1. Input raw prompt/idea.
2. Select target mode (General or Lifecycle).
3. Execute generated enhanced prompt into target agent or model.
