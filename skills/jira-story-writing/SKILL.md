---
name: jira-story-writing
description: Generate concise, well-structured Jira enhancement stories for UI improvements, feature extensions, and workflow updates.
---

## Instructions

### Story Structure
Every enhancement story MUST include these four sections in order:

1. **User Story**
   - Format: "AS A [user type], I WANT [goal], SO THAT [benefit]"
   - Keep it concise and user-focused
   - Example: "As an IT Admin, I want Group Sync when I connect our app with our IDP for SSO, so that I can quickly onboard and offboard users."

2. **Problem**
   - 2-3 sentences maximum
   - Describe the current state and why it's problematic
   - Focus on user impact or confusion
   - Be specific about what's wrong

3. **Solution**
   - 2-4 sentences maximum — a concise narrative of the approach, NOT a detailed spec
   - Answers "what are we doing and why this approach?" at a high level
   - Should read like a brief explanation to a colleague, not a checklist
   - Do NOT duplicate details that belong in Acceptance Criteria
   - No bullet points — write it as a short paragraph
   - The Solution is the "what", the ACs are the "prove it works"

4. **Acceptance Criteria**
   - The engineer's implementation checklist — each item is a testable statement
   - Cover happy path, edge cases, and error cases
   - Include specific UI copy in quotes, button labels, state transitions
   - Each criterion should be independently verifiable
   - Group related ACs under labeled sub-sections when the story is large
   - An engineer should be able to check off each AC and say "done"

**CRITICAL: Solution ≠ Acceptance Criteria**
   - If the Solution reads like a list of ACs, it's too detailed — condense it
   - If the ACs read like a summary, they're too vague — make them testable
   - Solution = "We will parse SAML groups on login and auto-create them in the platform"
   - AC = "SSO login with `groups: ['Team-A', 'Team-B']` results in user being a member of both groups"

### Writing Guidelines

**Be Concise**
- Keep Problem section under 100 words
- Keep Solution section under 75 words — it's a paragraph, not a spec
- Each AC should be one clear, testable statement
- No engineer likes to read LONG stories. Real estate in the words we use is really important
- If the Solution section has bullet points, it's probably too detailed — condense into prose

**Be Specific**
- Include exact UI copy in quotes
- Specify button labels: [Cancel], [Re-authenticate], [Save]
- Detail status flows: "Status → 'Connected'"
- Name specific UI elements: toggle, modal, tooltip

**Common Enhancement Patterns**
- **UI Consistency**: Extending a pattern from one area to another
- **Status/State Management**: Clear transitions and messaging
- **Error Handling**: Modals, error copy, recovery flows
- **Feature Extensions**: Taking existing functionality to new contexts
- **Workflow Improvements**: Reducing clicks, improving clarity

**Formatting**
- Use bullets (asterisks) for lists
- Indent sub-bullets with spaces
- Use → for state transitions
- Put UI copy in quotes
- Use [Button Name] for buttons

### What to Include
- Tooltips that provide context
- Error messages and modal copy
- Button labels and their actions
- Status indicators and their meanings
- Auto-triggered actions (scans, validations)
- Redirect behaviors

### What to Avoid
- Vague acceptance criteria
- Technical implementation details (unless necessary for clarity)
- Overly long problem descriptions
- Missing error cases
- Ambiguous UI copy

### Story Template

```
User Story
As a [user type], I want [goal], so that [benefit].

Problem
[2-3 sentences describing current state and why it's problematic]

Solution
[2-4 sentence paragraph explaining the approach at a high level. No bullets. Answers "what are we doing?" without duplicating the ACs.]

Acceptance Criteria
* [Testable action] results in [specific outcome]
* [User action] displays [specific UI element] with copy: "Exact text"
   * [Button behavior]: [Button Name] redirects to [destination]
* [Edge case condition]: [Expected result with specific status/message]
* [Error case]: [Expected behavior]
```

### Example

**User Story**
As an Admin, I want to see a clear connection status after linking a new integration, so that I know whether setup succeeded without digging through logs.

**Problem**
After an admin completes an OAuth flow for a new integration, the integration card still shows "Not Connected" until the page is manually refreshed. This causes confusion and support tickets, because admins assume the connection failed and retry the flow.

**Solution**
Automatically poll the connection status after the OAuth callback completes and update the integration card in real-time. If the connection succeeds, transition the card to a connected state with a timestamp. If it fails, surface an inline error with a retry option.

**Acceptance Criteria**
* Completing OAuth flow → integration card updates to Status: "Connected" with timestamp within 5 seconds, no page refresh required
* Connection success displays green badge with copy: "Connected as of [timestamp]"
* Connection failure displays inline error with copy: "Connection failed. Please try again."
   * [Retry] button re-initiates the OAuth flow
   * [Cancel] button returns card to "Not Connected" state
* If polling exceeds 30 seconds with no response → display copy: "Connection is taking longer than expected. Check back shortly." with [Dismiss] button
* Admin navigating away and returning sees the persisted connection status, not a stale state

### Tips for Best Results
When providing input, include as much of the following as you can:
- What area of the product does this affect?
- Who is the primary user (CS team, end user, admin)?
- Does this extend an existing pattern from another area?
- Are there specific error cases to handle?
- Is there existing UI copy or patterns to match?

**Story sizing**: Before writing, consider whether the work should be one story or multiple. A good story is something an engineer can complete and say "done." If a story has both backend logic and UI changes, only split if the UI work is substantial enough to stand alone. Small UI tweaks (labels, read-only fields) can be ACs on the same story. Group related ACs under labeled sub-sections for larger stories.