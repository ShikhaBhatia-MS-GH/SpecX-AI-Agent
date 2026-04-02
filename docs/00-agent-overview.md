# SpecX AI Agent – Overview

## What is the SpecX AI Agent?

The **SpecX AI Agent** is a **declarative Copilot Studio agent** designed to help Microsoft partners
understand, prepare for, and navigate **Microsoft specialization and audit readiness** by
providing guidance based on approved knowledge sources.

This agent is built using **only declarative capabilities** in Copilot Studio:
- Agent instructions
- Knowledge sources
- Starter prompts

No custom actions, flows, APIs, or connectors are used.

---

## What the SpecX AI Agent is designed to do

The SpecX AI Agent is intended to:

- Explain specialization and audit-related concepts in **plain, partner-friendly language**
- Help partners understand **what evidence is expected** for specific requirements
- Guide users on **how to think about readiness and gaps**
- Reference uploaded knowledge sources when responding
- Provide consistent, compliant, and grounded responses

Typical questions the agent can help with:
- “What type of evidence is expected for this specialization requirement?”
- “How should partners approach audit readiness?”
- “What are common gaps partners should watch for?”

---
## Agent Architecture (Parent and Child Agents)


The SpecX AI Agent is implemented as a **multi‑agent declarative architecture**
within Microsoft Copilot Studio.

This architecture consists of:

- **SpecX AI Agent** – the parent (orchestrator) agent  
- **Audit Agent** – a child agent focused on audit‑specific depth

Users interact only with the **SpecX AI Agent**, which acts as the single
entry point for all conversations.

---

### SpecX AI Agent (Parent Agent)

The SpecX AI Agent serves as the **primary orchestrator** and is responsible for:

- Receiving and managing user conversations
- Maintaining conversational context
- Handling high‑level specialization and readiness queries
- Determining when deeper audit‑specific expertise is required
- Routing relevant queries to the Audit Agent when appropriate

The parent agent ensures consistent tone, scope control, and guardrails
across all interactions.

---

### Audit Agent (Child Agent)

The Audit Agent is a **specialized child agent** that supports the SpecX AI Agent
by handling **deep, audit‑focused queries**, such as:

- Detailed questions about audit expectations
- Evidence‑level reasoning and explanations
- Specialization‑specific audit scenarios grounded in documentation

The Audit Agent operates only in the context of the SpecX AI Agent and is not
directly exposed to end users.

Conversation history is passed from the SpecX AI Agent to the Audit Agent to
ensure responses remain contextual and relevant.

---

### How the agents work together

At a high level:

1. A user asks a question to the SpecX AI Agent
2. The SpecX AI Agent evaluates the intent and depth of the query
3. If the question requires deeper audit‑specific reasoning, the SpecX AI Agent
   invokes the Audit Agent
4. The Audit Agent provides a grounded, detailed response
5. The SpecX AI Agent returns the response to the user in a consistent,
   partner‑friendly manner

This design enables both **breadth and depth** while preserving clear scope
boundaries and responsible behavior.

---

### Architectural boundaries and intent

Even with a child Audit Agent:

- No agent provides audit guarantees or pass/fail outcomes
- No agent replaces official audit guidance or documentation
- All responses remain advisory and guidance‑oriented

This multi‑agent structure improves clarity and depth without changing the
declarative, governance‑friendly nature of the solution.

## What the SpecX AI Agent is NOT designed to do

To ensure compliance and responsible AI use, the SpecX AI Agent **must not**:

- Guarantee audit outcomes or pass/fail results
- Provide legal, contractual, or compliance advice
- Replace official audit guidance or partner documentation
- Invent requirements or speculate beyond available knowledge
- Act as an authoritative decision-maker

If a question is outside scope or insufficient information is available, the agent should
respond with an appropriate clarification or refusal.

---

## Target audience

The SpecX AI Agent is intended for:
- Microsoft partners preparing for specializations or audits
- Partner technical and delivery teams
- Partner practice leads and readiness owners

It is **not** intended for end-customers or anonymous users.

---

## How this repository helps you

This repository provides:
- Step-by-step guidance to build the SpecX AI Agent in Copilot Studio
- Ready-to-use instruction templates
- Guidance on preparing and structuring knowledge sources
- Starter prompt packs to guide user interaction
- A testing and validation approach before sharing the agent

All guidance in this repository assumes a **single declarative agent implementation**.

---

## Important constraints and assumptions

- Anonymous or unauthenticated agents are not supported
- Agent behavior is limited to uploaded knowledge and provided instructions
- Answers may not surface sensitivity labels when responses are generated
- Agent accuracy depends heavily on the quality and structure of knowledge sources

These constraints should be understood before building or sharing the agent.

---

## What’s next

Proceed to:
- **Prerequisites** → `01-prerequisites.md`
- **Agent instructions** → `02-agent-instructions.md`
- **Knowledge setup** → `03-knowledge-setup.md`
