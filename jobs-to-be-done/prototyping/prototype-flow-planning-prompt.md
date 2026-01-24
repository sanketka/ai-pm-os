
### Read & Decompose
You will receive a PRD for Feature X. Analyze the full document, but present your response **ONE FLOW AT A TIME**.

A “flow” is an end-to-end user journey with:
- a clear starting point
- a series of actions
- a concrete end state / outcome

---

## Output Format (Per Flow)

### Flow N: <Flow Name>
#### 1) User journey
- **Start state:**  
- **Primary actor:**  
- **Steps:**  
  1.  
  2.  
  3.  
- **End state / success criteria:**  

#### 2) New screens to create
List any new screens required.
For each screen include:
- **Name:**  
- **Route:**  
- **Purpose:**  
- **Primary components:** (table, filter bar, detail panel, modal, etc.)

#### 3) Existing screens to update
List any existing screens that must be modified.
For each screen include:
- **Screen name / route:**  
- **What changes:**  
- **Why changes are required:**  

#### 4) Screenshot patterns to follow (per screen)
For every new or updated screen, explicitly state:
- **Pattern reference:** (which screenshot / pattern name)
- **Elements reused:** (layout, table style, filter bar, modals, etc.)
- **Any required deviation:** (if any)  
  - If deviation is required, **stop and ask for permission** with justification.

#### 5) Ambiguities / questions
List questions that block prototyping accuracy, e.g.:
- undefined permissioning
- missing edge cases
- unclear default states
- unclear empty states
- unclear API/system behavior implied by the PRD

---

## Scope Control

### Out of Scope
Explicitly excluded from this work (pull verbatim from the PRD out-of-scope section, but also highlighted here):

- Auto-imported contracts  
- Integration List View updates  
- Integration Detail View updates  

If the PRD implies these areas, call it out under **Ambiguities / Questions** and propose an alternate in-scope approach.

---

## Constraints

- **Do NOT generate UI yet.** No wireframes, no component layouts, no HTML, no v0 prompts.
- **Do NOT jump ahead.** Only present **Flow 1** in your first response.
- End Flow 1 with: **“Approve Flow 1 or request changes; I will not proceed to Flow 2 until approved.”**

---

## Success Criteria
A successful output:
- cleanly decomposes the PRD into flows
- ties every screen to an existing UX pattern
- surfaces gaps early
- makes the next step (actual prototyping) fast and low-risk
