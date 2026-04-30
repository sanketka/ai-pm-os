# craft

A personal toolkit for doing better work with AI. Organized into two types of artifacts: **Skills** (self-contained Claude Skills you upload directly) and **Workflows** (multi-step prompt sequences for Claude Projects).

---

## Skills

Self-contained Claude Skills. Download the folder, zip it, upload to Claude under Settings → Skills.

### Jira Story Writing
**Location:** `skills/jira-story-writing/`

Generates concise, well-structured Jira enhancement stories. Enforces a strict separation between Solution (what and why, in prose) and Acceptance Criteria (testable engineer checklist). Outputs stories sized so an engineer can complete one and say "done."

### Grill UX Mock
**Location:** `skills/grill-ux-mock/`

Critiques a mockup or wireframe against a requirements file and persona. Grills across four dimensions: UX and interaction patterns, copy and language, persona fit, and polish consistency. Always outputs a structured recommendation table with exact fixes and P0/P1/P2 triage, not vague suggestions.

### Learning Tree
**Location:** `skills/learning-tree/`

Breaks any topic into a structured learning tree from foundational roots to actionable leaves, with curated resources at each level. General-purpose: works for technical, business, creative, or scientific subjects. Trigger it when you want to deeply understand something new or need a learning path from first principles.

---

## Workflows

Multi-step prompt sequences. Use these inside a Claude Project by loading `project-instructions.md` first, then following the documented steps.

### PRD Creation
**Location:** `workflows/prd/`

Transforms customer problems into execution-ready PRDs through structured discovery. Enforces discovery before drafting, persona-driven requirements, and evidence-based problem framing. Prevents solutioning too early.

Files: `project-instructions.md`, `problem-statement-template.md`, `prd-prompt.md`, `project-inputs.md`

### Prototype Planning
**Location:** `workflows/prototype/`

Translates an approved PRD into a flow-by-flow prototype plan grounded in existing UX patterns. Structure before pixels: defines what to build and where it fits before any UI or wireframes are generated.

Files: `project-instructions.md` (load into Claude Project), `design-system-prompt.md`, `prototype-flow-planning-prompt.md`, `project-inputs`
