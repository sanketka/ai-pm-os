# ai-pm-os
An evolving operating system for building B2B products using AI.

## Jobs to Be Done

This repository organizes product management workflows as discrete "Jobs to Be Done" (JTBD). Each JTBD folder contains the prompts, templates, and instructions needed to complete a specific PM task with AI assistance.

### JTBD-1: Problem Brainstorming & PRD Creation

**Location:** `jobs-to-be-done/problem-brainstorming-prd/`

**Purpose:** Transform customer problems into rigorous, execution-ready PRDs through structured discovery and critical thinking.

**What's Inside:**

- **`project-instructions.md`** — Core instructions for the AI to act as a critical product partner. These instructions ensure the AI challenges assumptions, demands evidence, and pushes for clarity before drafting any artifacts. Use this in your favorite AI tool. 

- **`problem-statement-template.md`** — A structured template for documenting problems. Covers the problem itself, impact, current state, success criteria, and constraints.

- **`prd-prompt.md`** — The main prompt for PRD creation. Instructs the AI to ask clarifying questions, understand workflows and personas, and draft PRDs that are persona-driven, workflow-based, and technically grounded.

- **`project-inputs.md`** — Documentation of required inputs that must be provided separately (customer evidence, personas, product strategy, screenshots, etc.). 

**How to Use**

1. **Start with `project-instructions.md`.**  
   Treat this as the governing instruction set for the project. It defines how the AI should think, challenge assumptions, and engage with you throughout the work.

2. **Fill out `problem-statement-template.md`.**  
   Capture as much context as you can about the problem you’re trying to solve. It’s okay if this is incomplete or messy — gaps will be surfaced and challenged during discovery.

3. **Add supporting documentation to your project.**  
   Bring in any relevant inputs such as customer evidence, personas, strategy documents, screenshots, or reference materials. These are not included in this repository and should live in your own working environment.

4. **Use `prd-prompt.md` to begin the PRD workflow.**  
   Use the prompt with your AI assistant, referencing the project instructions and supplied inputs. Expect the AI to push back, ask clarifying questions, and force decisions before drafting.

The goal is not speed. The goal is a PRD that is grounded in reality, aligned to strategy, and ready for engineering execution.

**Philosophy:** This JTBD enforces discovery before drafting, persona-driven requirements, and evidence-based problem framing. It prevents solutioning too early and ensures every feature ties back to real user workflows and business outcomes.

## JTBD-2: Prototype Planning & UX-Constrained Design

**Location:**  `jobs-to-be-done/prototype-planning/`

**Purpose:**  
Translate an approved PRD into a **clear, flow-by-flow prototype plan** that is grounded in existing UX patterns and ready for design or engineering execution.

This JTBD focuses on *what to build* and *where it fits*, **before** any UI or wireframes are generated. Once that is clear, building he prototype is as easy as typing "Build this now". 

---

### What’s Inside

- **project-instructions.md**  
  Governing instructions for how the AI should reason during prototype planning. Enforces flow-based thinking, design consistency, and scope discipline.

- **design-context-prompt.md**  
  Extracts and documents existing UX patterns from product screenshots. Produces a lightweight, implicit design system used to constrain future prototypes.

- **prototype-planning-prompt.md**  
  Converts the PRD (from JTBD-1 output) into a flow-by-flow breakdown:
  - user journeys
  - new vs existing screens
  - route definitions
  - UX pattern references
  - open questions and ambiguities  
  UI generation is explicitly blocked at this stage.

- **project-inputs.md**  
  Documents required inputs (PRD from JTBD-1, existing product screenshots, feature-area screenshots, and optional reference UX patterns).

---

### How to Use JTBD-2

1. **Start with the finalized PRD from JTBD-1**  
   JTBD-2 assumes scope, goals, and requirements are already locked.

2. **Run the Design Context prompt**  
   Use real product screenshots to extract and document existing UX patterns.  
   This becomes the constraint system for all future UI work.

3. **Run the Prototype Planning prompt**  
   Break the PRD into discrete user flows.  
   Review and approve **one flow at a time** before proceeding.

4. **Only then move to UI generation**  
   Wireframes, mocks, or v0-style prompts should come *after* this. 

---

### Philosophy

JTBD-2 enforces **structure before pixels** and optimizes for one-shot prototype generation for complicated features. 

It prevents:
- inconsistent UX
- scope creep during design
- premature wireframing
- silent design assumptions