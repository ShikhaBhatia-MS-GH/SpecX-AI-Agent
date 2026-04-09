# Starter Prompts – Design and Usage Guidance

Starter prompts play a critical role in shaping how users interact with the
**SpecX AI Agent**. They help set expectations, guide behavior, and encourage
questions that are within scope of a declarative agent.

This document explains **how the SpecX starter prompts are designed** and
**how partners should use or extend them responsibly**.

---

## What are starter prompts?

Starter prompts are example questions displayed to users when they first
interact with the agent. They serve to:

- Demonstrate the kinds of questions the agent can answer
- Encourage users to ask scoped, meaningful queries
- Reduce ambiguity and off‑topic requests
- Improve the quality and consistency of interactions

For declarative agents like SpecX, well-designed starter prompts are especially
important because there are no actions or workflows to guide the experience.

---
### Relationship to the Audit Agent

Starter prompts are configured only on the **SpecX AI Agent**.
However, certain prompts—especially Levels 2 and 3—are designed to
trigger deeper, audit‑specific reasoning.

In such cases, the SpecX AI Agent may internally delegate the query to
the **Audit Agent** while preserving context and guardrails.

Users remain unaware of this delegation and experience a single,
seamless interaction.

## Where the actual starter prompts live

The **actual starter prompt text** used for the SpecX AI Agent is stored under:
samples/starter-prompts/
├─ level-1-foundational.md
├─ level-2-evidence-coach.md
└─ level-3-audit-ready.md

Each file contains raw, copy‑paste–ready prompts that can be added
directly to the **Starter prompts** section in Copilot Studio.
