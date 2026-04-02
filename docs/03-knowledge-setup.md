# Knowledge Setup – SpecX AI Agent and Audit Agent

Knowledge quality and structure are the most critical factors influencing the
accuracy and usefulness of a **declarative Copilot Studio agent**.

In the SpecX implementation, knowledge is intentionally **split across a
parent–child agent architecture** to balance breadth and depth while maintaining
clear scope boundaries.

---

## Knowledge architecture overview

The SpecX solution uses **two agents with distinct knowledge responsibilities**:

- **SpecX AI Agent (Parent Agent)** – readiness and guidance context
- **Audit Agent (Child Agent)** – audit‑specific depth and evidence grounding

This separation improves clarity, response relevance, and maintainability.

Users interact only with the **SpecX AI Agent**.  
The **Audit Agent** is invoked internally when deeper audit‑specific reasoning
is required.

---

## Knowledge for SpecX AI Agent (Parent Agent)

### Purpose
Knowledge attached to the SpecX AI Agent should support:

- High‑level specialization understanding
- Readiness framing and preparation guidance
- Common partner questions and patterns
- Conceptual explanations rather than evidence evaluation

### Recommended knowledge types
- Overview documentation for specializations
- Readiness guides and partner enablement material
- General audit preparation guidance
- Non‑sensitive reference documentation

### What to avoid
- Deep audit checklists intended for strict interpretation
- Evidence‑level PDFs that require precise grounding
- Content that could trigger over‑authoritative responses

The goal of SpecX AI Agent knowledge is **orientation and guidance**, not audit decisions.

---

## Knowledge for Audit Agent (Child Agent)

### Purpose
The Audit Agent is designed to handle **deep, audit‑focused queries** and should
be grounded in authoritative, specialization‑specific documentation.

### Recommended knowledge types
- Specialization‑specific audit PDFs
- Evidence expectations and checklists
- Control descriptions and audit guidance
- Structured documents used during audit preparation

### Key considerations
- Ensure documents are current and versioned
- Prefer official or validated sources
- Avoid mixing unrelated specializations in the same knowledge scope
- Keep content tightly aligned to audit interpretation and explanation

Knowledge attached to the Audit Agent enables **precision and depth**, while
remaining advisory in nature.

---

## Structuring knowledge content

Regardless of the agent, well‑structured knowledge improves response quality.

Recommended practices:
- Use clear section headers and descriptive titles
- Maintain consistent terminology across documents
- Avoid large, unstructured blocks of text
- Clearly distinguish guidance from requirements
- Remove outdated or redundant content

Poorly structured knowledge often results in vague or generic responses.

---

## Organizing knowledge across agents

To avoid confusion and overlap:

- Place **broad guidance** with the SpecX AI Agent
- Place **audit‑specific depth** with the Audit Agent
- Do not duplicate the same document across both agents unless necessary
- Review routing behavior during testing to confirm correct invocation

Intentional placement is more effective than volume.

---

## Updating knowledge over time

Knowledge updates should be treated as part of ongoing agent maintenance.

Recommendations:
- Review knowledge periodically for accuracy
- Update documents when specialization guidance changes
- Re‑test agent behavior after significant knowledge updates
- Remove deprecated or superseded content promptly

Declarative agents improve primarily through **knowledge refinement**, not code changes.

---

## Relationship to other files

- Knowledge inventory → `docs/01-prerequisites.md`
- Agent behavior design → `docs/02-agent-instructions.md`
- Starter prompt usage → `docs/04-starter-prompts.md`
- Testing and validation → `docs/05-testing-and-validation.md`

---

## What’s next

Once knowledge is structured and assigned correctly, proceed to:

- **Starter prompts** → `docs/04-starter-prompts.md`
