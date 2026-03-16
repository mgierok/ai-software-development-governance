# AI Governance Function AI Tool Decision Register

## 1. Purpose

This appendix maintains the operational register of AI Governance Function decisions for AI tools, integrations, and related capabilities used for software development within `[Organization]`.

This appendix supplements [`ai-engineering-policy-draft.md`](./ai-engineering-policy-draft.md) and is intended to be updated independently from the revision cycle of any specific version of that policy.

## 2. Maintenance Rules

- The AI Governance Function should update this appendix whenever an approval decision is issued, changed, suspended, or revoked.
- This appendix should record approvals, approvals granted with restrictions, rejections, suspensions, and revocations.
- If a tool does not have a public source repository, the GitHub link field should be marked as `N/A`.
- Each restriction should be stated concretely so that users can determine whether a proposed use remains within the approved boundary.
- Each record should define the approved scope of use, including applicable environments, data classes, connected systems, user groups, and workflow conditions where relevant.
- Inclusion in this appendix does not by itself authorize unrestricted use. A proposed use is permitted only when it remains within the recorded decision and restrictions for that tool or capability.

## 3. AI Tool Decision Register

The register should contain one row per tool, integration, plugin, Skill, connector, or MCP server decision record, together with the specific restrictions and conditions that define its approved organizational use.

| Tool name | GitHub link | Tool description | Decision | Restrictions | Rationale |
| --- | --- | --- | --- | --- | --- |
| `[Tool Name]` | `[Repository URL or N/A]` | `[Short description of the tool and its engineering use case.]` | `[Approved / Approved with restrictions / Rejected / Suspended / Revoked]` | `[Environment, data, access, or workflow restrictions.]` | `[Summary of the approval or decision basis.]` |
