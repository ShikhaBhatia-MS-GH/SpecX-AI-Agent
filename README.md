# SpecX AI Agent – Declarative Build Guide

This repository provides a step‑by‑step guide for Microsoft partners to build the  
**SpecX AI Agent** using **Microsoft Copilot Studio (declarative architecture)**.

The SpecX AI Agent is designed to support partners in understanding
specialization expectations and preparing for audit readiness through
knowledge‑grounded guidance.

---

## What this repository helps you do

Using this guide, you can:

- Recreate the SpecX AI Agent in Copilot Studio
- Configure a multi‑agent declarative setup
- Attach and organize knowledge sources effectively
- Add curated starter prompts
- Validate agent behavior before sharing
- Publish and share the agent responsibly within your organization

---

## Agent architecture overview

The SpecX solution uses a **parent–child agent architecture**:

- **SpecX AI Agent (Parent Agent)**  
  - Primary user‑facing agent  
  - Handles high‑level readiness and specialization queries  
  - Maintains tone and guardrails  
  - Routes deep audit‑specific queries when required  

- **Audit Agent (Child Agent)**  
  - Invoked internally by the SpecX AI Agent  
  - Handles detailed audit and evidence‑level questions  
  - Grounded in specialization‑specific documentation  
  - Receives conversation context from the parent agent  

Users interact only with the **SpecX AI Agent**.  
The Audit Agent operates internally and is not shared independently.

---

## Declarative‑only implementation

This repository supports **declarative agents only**, built using:

- Agent instructions
- Knowledge sources
- Starter prompts

The following are out of scope:

- Power Automate flows
- Custom connectors
- APIs or external integrations
- Code‑based extensibility

---

## Quick Start (15‑minute setup)

Follow the steps below to build the SpecX AI Agent:

1. Review prerequisites  
   → `docs/01-prerequisites.md`

2. Create the SpecX AI Agent in Copilot Studio  
   - Add name and description  
   - Paste instruction block from  
     `samples/instructions/specx-agent-instructions.md`

3. Create and configure the Audit Agent  
   - Paste instruction block from  
     `samples/instructions/audit-agent-instructions.md`

4. Attach knowledge sources  
   → `docs/03-knowledge-setup.md`

5. Add starter prompts  
   → `samples/starter-prompts/`

6. Test and validate behavior  
   → `docs/05-testing-and-validation.md`

7. Publish and share responsibly  
   → `docs/06-publishing-and-sharing.md`

---

## Repository structure

docs/
→ Explanatory guidance and best practices
samples/
→ Copy‑paste assets used directly in Copilot Studio
- instructions/
- starter-prompts/
- knowledge/


## Important usage notes

The SpecX AI Agent:

- Provides guidance only
- Does not guarantee audit outcomes
- Does not replace official audit documentation
- Should be reviewed periodically after sharing
- Improves primarily through knowledge updates

Any governance or ownership applies to the complete  
**SpecX + Audit Agent setup**.

---

## Recommended next steps

Proceed through the documentation in order:

1. Agent Overview → `docs/00-agent-overview.md`
2. Prerequisites → `docs/01-prerequisites.md`
3. Instruction Design → `docs/02-agent-instructions.md`
4. Knowledge Setup → `docs/03-knowledge-setup.md`
5. Starter Prompts → `docs/04-starter-prompts.md`
6. Testing & Validation → `docs/05-testing-and-validation.md`
7. Publishing & Sharing → `docs/06-publishing-and-sharing.md`

---

## Support

For guidance on implementation, testing, or customization,
refer to the documentation under the `docs/` directory.
