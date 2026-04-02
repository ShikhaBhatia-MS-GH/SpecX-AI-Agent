# Publishing and Sharing – SpecX AI Agent

This document explains **when** the SpecX AI Agent is ready to be published,
**how** to share it safely, and **what sharing does and does not imply**.

Since SpecX is a **declarative Copilot Studio agent**, publishing and sharing
should be handled carefully to avoid misuse, confusion, or compliance risk.

---

## When is the agent ready to be published?

The SpecX AI Agent should be published only after:

- ✅ All testing and validation steps are completed
- ✅ Agent instructions are finalized and reviewed
- ✅ Knowledge sources are verified and up to date
- ✅ Starter prompts behave as expected
- ✅ Out‑of‑scope questions are handled safely

Refer to `docs/05-testing-and-validation.md` before proceeding.

---

## Publishing the agent

📍 **Where to do this in Copilot Studio:**  
Copilot Studio → Open the SpecX AI Agent → **Publish**

Publishing makes the agent:
- Available for use within the configured scope
- Ready to be shared with selected users or groups

> ⚠️ Publishing does **not** automatically make the agent publicly accessible.

---

## Sharing the agent (recommended approach)

The SpecX AI Agent is intended to be shared **in a controlled manner**, based on
partner readiness and governance expectations.

### Recommended sharing practices

✅ Do:
- Share with specific users or groups
- Start with a limited audience
- Brief users on the agent’s scope and limitations
- Monitor usage and feedback

❌ Avoid:
- Broad, unrestricted sharing
- Treating the agent as an authoritative audit source
- Assuming sharing implies endorsement or certification

---

## What sharing does NOT imply (important)

Sharing the SpecX AI Agent does **NOT** mean:

- Certification or audit approval
- Guaranteed outcomes or pass/fail decisions
- Replacement for official documentation or guidance
- Authorization to bypass standard audit processes

This distinction should be clearly communicated to all users.

---

## Ongoing maintenance after sharing

Once the agent is shared, ongoing ownership is required.

Recommended activities:
- Periodically review agent responses
- Update knowledge sources as guidance evolves
- Retest after significant content updates
- Revisit instructions if behavior drifts over time

Declarative agents improve through **content and clarity**, not code changes.

---

## Handling feedback and issues

If users report issues such as:
- Vague or generic responses
- Over‑confident answers
- Missing coverage for common questions

Use the following guidance:
- Knowledge gaps → update knowledge sources
- Tone or guardrail issues → review instructions
- Misleading interactions → refine starter prompts

Make one change at a time and re‑test.

---

## Governance and responsibility

Owners of the SpecX AI Agent should ensure:

- The agent remains within intended scope
- Changes are documented and intentional
- Sharing aligns with organizational policies
- Users understand the agent’s purpose and limitations

---

## Relationship to other files

- Readiness checks → `docs/05-testing-and-validation.md`
- Agent behavior design → `docs/02-agent-instructions.md`
- Knowledge management → `docs/03-knowledge-setup.md`
