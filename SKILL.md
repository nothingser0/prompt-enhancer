---
name: prompt-enhancer
description: Use when raw prompts need to become structured prompts.
version: 2.0.0
updated: 2026-11-04
---

# Prompt Enhancer (Advanced Framework Edition)

An enterprise-grade prompt engineering toolkit designed to transform raw, vague, or incomplete user ideas into rigorous, production-ready, highly structured prompts. It incorporates strict anti-hallucination protocols, structured execution steps, quality gates, and modular routing (General vs. Lifecycle/SDLC).

---

## Core Architecture

When activated, the prompt enhancer operates through a 4-phase transformation pipeline:
1. **Intent Analysis**: Detects whether the input is a general problem (coding, debugging, research, copywriting) or an SDLC project execution (aligned with `solo-project-lifecycle`).
2. **Context Enrichment**: Injects strict boundaries, domain standards, and technical constraints to prevent lazy or generic AI output.
3. **Execution Schema**: Imposes a rigorous, step-by-step breakdown (Role, Objective, Context, Constraints, Workflow, Verification, and Output Format).
4. **Verification & Guardrails**: Enforces anti-hallucination checks, explicit evidence reporting, and mandatory validation gates before task completion.

---

## Operating Modes

### 1. General Mode (Coding, Architecture, Debugging, Copywriting)
Use when the prompt requires deep technical execution, code refactoring, system architecture design, or specialized creative work.

**Enhanced Prompt Template:**
```markdown
Role: Elite [Domain] Expert & Senior Architect
Task: [Precise, unambiguous objective translated from raw input]
Context: [Project background, technical stack, or environment constraints]

Constraints & Guardrails:
- YAGNI & Minimalist Approach: No unnecessary abstractions or boilerplate.
- Security First: Input validation at trust boundaries, secure handling of secrets.
- Strict Verification: Every change or claim must be backed by tangible execution evidence (exit codes, test runs, file verification).

Workflow:
1. Review existing codebases or constraints using read_file / search_files.
2. Formulate the minimal viable solution adhering to standard patterns.
3. Execute changes/code via targeted tools.
4. Run validation checks / tests and verify output against acceptance criteria.

Output Format:
- Concise, production-ready code blocks or technical findings.
- Step-by-step implementation notes with exact file paths.
```

### 2. Lifecycle Mode (`solo-project-lifecycle` Integration)
Use when building project specifications, PRDs, database schemas, modules (M01–M13), or executing structured SDLC workflows.

**Enhanced Prompt Template:**
```markdown
Role: Solo Project Architect & SDLC Enforcer
Task: Generate compliant artifact for Module [M01-M13] based on project scale (Small, Solo SaaS, Client, Large, Enterprise).
Framework Reference: solo-project-lifecycle

Mandatory Rules:
1. Template-First: Copy and fill official templates from `templates/` rather than freeform writing.
2. Gate Validation: Run `./scripts/gates/validate-gate.sh <MODULE>` before declaring any phase complete.
3. Stop per Gate: Honor explicit stops (Intake Gate, Design References, M05 Stack Lock, Client Gates M03/M09/M11, and M06 single-task progression).
4. Cross-Document Consistency: Ensure downstream docs strictly align with upstream scopes and sitemaps.

Workflow:
1. Identify project scale and current phase from `docs/pm/PROJECT_STATE.md`.
2. Inspect required inputs and templates.
3. Draft artifact following strict structure.
4. Execute gate validation script and report exact exit codes.
```

---

## Usage Guide

To use this skill effectively, pass your raw prompt or idea alongside your desired mode or target module:
- `enhance prompt for general: [your raw idea]`
- `enhance prompt for lifecycle M04: [your project scope]`
