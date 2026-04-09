# Prerequisites – SpecX AI Agent (Declarative)

This section outlines **all prerequisites** required before building the
**SpecX AI Agent** using **Copilot Studio**.

Please review and complete all steps before proceeding to agent creation.

---

## 1. Access and permissions

Before you begin, ensure the following access is in place:

- ✅ Access to **Microsoft Copilot Studio**
- ✅ Appropriate role to **create and configure agents**
  (for example: Maker or equivalent permissions in the environment)
- ✅ Ability to add **knowledge sources** (such as SharePoint sites or documents)

> ⚠️ If you do not have sufficient permissions, agent creation or knowledge
> ingestion may fail later in the process.

---

## 2. Supported agent type (important)

This repository supports **ONLY one agent type**:

✅ **Declarative agent**
- Built using:
  - Instructions
  - Knowledge sources
  - Starter prompts

❌ The following are **out of scope**:
- Power Automate flows
- Custom actions or connectors
- APIs or external integrations
- Code-based extensions

Keep this in mind while following the rest of the guide.

---

## 3. SpecX AI Agent – creation details

When creating the agent in Copilot Studio, you will be asked to provide
basic configuration details.

📍 **Where to find this in Copilot Studio:**  
Copilot Studio → Create new agent → **Configure** tab (top section)

### Agent configuration

👉 Copy the values used while creating the agent and paste them below.

```text
Agent Name:
SpecX AI Agent

Agent Description:
A smart Specialization Coach guiding you through audit readiness, evidence preparation, and faster specialization achievement. It delivers instant, accurate responses so that you can progress confidently and reduce turnaround time.

Agent Purpose (optional, if noted separately):
<OPTIONAL – short summary of intended use>


## Audit Agent – child agent configuration

In addition to the parent SpecX AI Agent, this solution includes a
**child agent named Audit Agent**.  
The Audit Agent is used to handle **deep, audit‑specific and evidence‑level
queries** and is invoked only by the SpecX AI Agent.

Users do **not** interact with the Audit Agent directly.

---

### Audit Agent – basic configuration details

📍 **Where to find this in Copilot Studio:**  
Copilot Studio → Open SpecX AI Agent → **Agents** → Select **Audit Agent** → Details

👉 Copy the values used and paste them below for reference.

```text
Audit Agent Name:
Audit Agent

Audit Agent Description:
Helps answer audit-related queries for Microsoft Azure Partner Specializations by referencing grounded PDF documents for each specialization and providing detailed responses.
