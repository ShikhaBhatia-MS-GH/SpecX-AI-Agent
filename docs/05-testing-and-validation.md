# Testing and Validation – SpecX AI Agent

Testing and validation are critical steps before sharing the **SpecX AI Agent**
with a broader audience. Since SpecX is a **declarative Copilot Studio agent**, 
response quality depends entirely on:

- Agent instructions
- Knowledge sources
- Starter prompts

This document provides a structured approach to **validate behavior, accuracy,
and compliance** before publishing or sharing the agent.

---

## Why testing is important

The SpecX AI Agent is designed to guide partners on specialization and audit
readiness. Poorly tested agents may:

- Provide vague or misleading guidance
- Appear over‑confident or authoritative
- Hallucinate requirements not present in knowledge sources
- Create audit or compliance risk

Testing helps confirm the agent behaves as intended and stays within scope.

---

## When to test

Testing should be performed:

- After initially creating the agent
- After changing instructions
- After adding, removing, or updating knowledge sources
- After modifying starter prompts
- Before sharing the agent more broadly

---

## What to test (core validation areas)

Testing should focus on the following five areas:

---

### 1. Instruction adherence

Validate that the agent consistently:

- Follows the defined agent role
- Avoids audit guarantees or pass/fail language
- Uses a partner‑friendly, explanatory tone
- Refuses or redirects out‑of‑scope questions appropriately

✅ If the agent sounds authoritative or decisive, review:
- Instruction guardrails
- Prompt phrasing

---

### 2. Knowledge grounding

Check whether responses:

- Reference concepts aligned with uploaded knowledge
- Avoid inventing requirements or interpretations
- Clearly indicate when information is missing or unavailable

✅ If the agent hallucinates or generalizes too much, review:
- Knowledge completeness
- Document structure and clarity
- Instruction emphasis on knowledge‑first responses

---

### 3. Starter prompt behavior

Test all starter prompts configured for the agent.

Evaluate:
- Does the response match the *intent* of the prompt?
- Is the level of detail appropriate?
- Does the prompt lead to consistent, useful behavior?

Starter prompts should guide—not constrain—the agent.

---

### 4. Edge case handling

Test questions that are intentionally difficult or ambiguous, such as:
- “Will this guarantee a successful audit?”
- “Can you confirm we will pass?”
- “Is this evidence enough to clear the audit?”

Expected behavior:
- Polite refusal or redirection
- Explanation of limits
- Guidance without commitment

---

### 5. Tone and clarity

Assess whether responses are:
- Clear and easy to understand
- Free of unnecessary jargon
- Consistent across similar questions
- Supportive rather than judgmental

Tone issues typically indicate instruction or prompt refinement is needed.

### 6. Parent–Child agent routing behavior

In addition to validating response quality, testing must confirm that
queries are handled by the appropriate agent.

Validation should confirm that:
- High‑level readiness questions are handled by the SpecX AI Agent
- Deep, audit‑specific questions are routed to the Audit Agent
- Conversation context is preserved across agent hand‑offs
- Responses remain consistent in tone and guardrails


Testing should include prompts that are intentionally borderline between
readiness guidance and audit‑specific depth to confirm correct routing
between the SpecX AI Agent and the Audit Agent.

---

## Recommended testing approach

### Step 1: Use the SpecX starter prompt packs

Start testing using the curated prompt packs stored under:

---

## Recommended testing approach

### Step 1: Use the SpecX prompt packs

Start testing using the curated prompt packs stored under:
samples/starter-prompts/
├─ level-1-foundational.md
├─ level-2-evidence-coach.md
└─ level-3-audit-ready.md
