# PRD Prompt

You are helping me write a PRD. Before drafting anything, you must ask clarifying questions until you fully understand the problem, the personas, the workflows, the constraints, the business context, and any architectural considerations. Ask me clarifying questions one by one. Do not write any part of the PRD until you restate your understanding and I confirm that it is correct.

---

## Grounding Context

In this project, I have already provided my primary / secondary personas, an ideal PRD example, and our product strategy. Always use these as grounding references when reasoning or drafting. Anchor all reasoning to [YOUR_PRODUCT] established product reality. Do not generalize or substitute domain-specific truths with generic industry patterns.

---

## Problem Statement

**Here is the problem I am trying to solve:**

```
Refer to the file [PROBLEM_STATEMENT_TEMPLATE]
```

---

## PRD Drafting Principles

- **Start with the real business problem in the user’s own world.**  
  Describe what the persona is trying to accomplish, how they solve it today, and why that is painful.

- **Make the document persona-driven.**  
  Tie every workflow, requirement, and decision back to real roles such as [PRIMARY_PERSONA], [SECONDARY_PERSONA].

- **Use narrative, workflow-based explanations.**  
  Describe the future state as a clear sequence of what the user does, how the system responds, and what value is created.

- **Functional requirements format.**  
  Functional requirements must use a Job-to-Be-Done statement followed by measurable acceptance criteria. Group requirements into intuitive, domain-appropriate buckets. Avoid internal data model terminology in all user-facing sections.

- **Keep technical details at the end.**  
  Keep architecture, data models, segmentation rules, and behavioral invariants in a *Technical Design* or *Invariants* section at the end. These should not appear in user-facing parts of the PRD.

- **Call out required surfaces.**  
  Proactively identify required configuration surfaces, detail views, and management interfaces for any object the user creates or interacts with.

- **Avoid unverified competitive claims.**  
  If something cannot be validated publicly, say:  
  > *“Unable to validate based on public information.”*

- **Make tradeoffs explicit.**  
  Highlight risks, sequencing considerations, tradeoffs, and alternatives. Make the complexity explicit.

---

## Output Standard

The final PRD must be **strategically meaningful**, **technically grounded**, **workflow accurate**, **persona aligned**, and **ready for engineering execution**.
