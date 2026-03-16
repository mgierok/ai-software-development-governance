# AI-Assisted Software Development Policy

## 1. Purpose

This policy defines how `[Organization]` may use AI tools during the software development lifecycle. Its purpose is to enable practical productivity gains while preserving engineering quality, security, legal compliance, and clear human accountability for delivered software.

This policy is written for engineering readers and assumes baseline familiarity with standard software delivery practices such as code review, testing, CI/CD, access control, and production operations. It defines terms only where this policy gives them a specific governance, approval, or control meaning.

This policy establishes the organization-level rules for:

- Approving AI tools and connected capabilities used in engineering work.
- Using AI assistance in analysis, design, implementation, testing, documentation, and operational support.
- Protecting `[Organization]` data, customer data, source code, and intellectual property.
- Preventing unsafe delegation of decisions, approvals, and production actions to AI systems.

This policy does not attempt to restate detailed external threat taxonomies or security guidance in full. Where this policy requires users to review recognized external guidance, that guidance supplements this policy rather than being duplicated within it.

## 2. Scope

This policy applies to all Users who use AI capabilities in connection with software delivery for `[Organization]`.

This policy applies to AI-enabled engineering activities across the software delivery lifecycle, including:

- Product discovery, requirements drafting, architecture, and design support.
- Source code generation, editing, refactoring, migration, testing, debugging, and code review support.
- Documentation, runbooks, knowledge-base content, and release support.
- CI/CD assistance, scripting, developer automation, incident analysis, and operational troubleshooting.

This policy applies to AI delivery mechanisms used for engineering work, including chat-based assistants, IDE-integrated assistants, AI agents, plugins, connectors, APIs, Model Context Protocol (MCP) servers, and external automation services invoked by AI systems.

This policy covers both internally built and third-party AI systems. If an AI tool is used on `[Organization]` devices, repositories, tickets, documents, or data, it falls within the scope of this policy.

## 3. Definitions

This section defines only the terms that have a specific meaning in this policy. Routine engineering terms are used in their ordinary technical sense.

### 3.1. AI Agent

An AI-enabled system that can plan, call tools, manipulate files, retrieve data, or take actions across one or more systems with some degree of autonomy.

### 3.2. Approved AI Tool

An AI system, agent, model integration, skill or other callable capability, plugin, connector, or MCP server that has been reviewed and explicitly authorized for use under the `[Organization]` approval process and is listed in the official AI tool decision register with a status of `Approved` or `Approved with restrictions`.

Approval applies only within the scope, environments, data classes, connected systems, and workflow conditions recorded in the official AI tool decision register. Listing in the register does not constitute unrestricted approval for all use cases, execution contexts, or connected capabilities.

### 3.3. High-Risk Change

A code, configuration, infrastructure, security, or data-related change that could materially affect production availability, confidentiality, integrity, regulatory obligations, customer trust, or financial outcomes if it is incorrect or misused.

### 3.4. AI Governance Function

The function, committee, or delegated authority assigned to review and decide whether AI tools, integrations, and related capabilities may be used under this policy.

Under this policy, this function is assigned to `[AI Governance Function]`. It may include designated representatives from `[Engineering Governance Role]`, `[Platform or Architecture Governance Role]`, `[Security or Risk Governance Role]`, and `[Additional Governance Role]`.

### 3.5. User

Any employee, contractor, intern, or third-party service provider acting on behalf of `[Organization]` who uses AI tools, AI agents, or AI-enabled workflows covered by this policy.

### 3.6. Accountable Engineering Decision

A decision that selects, approves, authorizes, or rejects an engineering outcome on behalf of `[Organization]` where responsibility, escalation duties, compliance obligations, or formal governance consequences attach to that choice. Accountable engineering decisions include release approvals, security exceptions, architecture approvals, required code review approvals, production data access approvals, and incident severity classifications that determine formal response obligations.

An accountable engineering decision is not the same as executing a previously approved step. If a workflow has already been approved by the required human authority, later execution of that workflow may still create external side effects, but it does not transfer the underlying decision authority to the AI system.

### 3.7. External Side Effect

An action performed by an AI tool or AI agent that creates, modifies, deletes, transmits, grants, revokes, deploys, reconfigures, or otherwise changes state outside the current analytical exchange. External side effects include writing files, updating tickets, sending messages, calling APIs that change records, changing permissions, modifying infrastructure, or executing deployment steps.

An external side effect may occur without an accountable engineering decision if the action is merely carrying out a bounded and already authorized instruction. However, any such action remains subject to approval boundaries, access controls, and change controls under this policy.

### 3.8. State-Changing Production Action

Any external side effect that creates, modifies, deletes, deploys, restarts, scales, reconfigures, grants access in, or otherwise changes the behavior or data state of a production environment, production service, or production dataset. Read-only inspection, monitoring, and analysis do not by themselves constitute state-changing production actions.

### 3.9. Engineering Team Function

The engineering team or equivalent delivery function responsible for repository-level implementation practices under this policy.

Under this policy, this function is assigned to `[Engineering Team Function]`.

### 3.10. Engineering Management Role

The management role accountable for engineering team oversight under this policy.

Under this policy, this role is assigned to `[Engineering Management Role]`.

### 3.11. Technical Leadership Role

The technical leadership role accountable for architecture, quality, or delivery decisions under this policy.

Under this policy, this role is assigned to `[Technical Leadership Role]`.

## 4. Governance Principles

1. Human accountability remains mandatory.
   AI may assist with engineering work, but responsibility for design decisions, code quality, security posture, approvals, and production outcomes remains with authorized human personnel.
2. Default-deny for unapproved external capabilities.
   External AI-connected tools, public MCP servers, public skills, and third-party connectors must not be used unless they have been approved.
3. Risk-based use is required.
   The level of oversight, validation, approval, and control must increase when AI-assisted work involves a High-Risk Change, sensitive data, privileged access, production environments, or material business impact.
4. Least privilege must be enforced.
   AI systems may receive only the minimum context, permissions, and tool access needed for the task being performed.
5. Verification before reliance is required.
   AI-generated outputs must be reviewed, tested, and validated before they are merged, deployed, shared externally, or treated as authoritative.
6. Traceability must be preserved.
   Significant AI-assisted work must remain attributable to a responsible user and recoverable through standard engineering records such as tickets, commits, reviews, logs, and change histories.
7. Security and compliance requirements remain mandatory.
   AI-assisted work must comply with the security, privacy, legal, regulatory, and contractual controls that apply to any other engineering activity.
8. External guidance may be required.
   This policy defines `[Organization]` rules and approval boundaries. Detailed agentic threat and mitigation guidance may be required separately through recognized external references such as the OWASP Top 10 for Agentic Applications.

## 5. Permitted Use in the Software Development Lifecycle

AI tools may be used to support software development when the use is consistent with this policy, the tool is approved, and required human review is applied.

This section defines the categories of development work for which AI assistance is permitted. Section 9 defines the minimum acceptance, review, and deployment gates that apply before AI-assisted outputs are relied on.

### 5.1. Planning, Analysis, and Design Support

Approved AI tools may be used to summarize requirements, propose design alternatives, draft architecture notes, and identify dependencies, edge cases, and operational considerations.

Users must validate that AI-generated analysis reflects the actual system context and does not omit important technical, security, or compliance constraints.

### 5.2. Coding, Refactoring, and Migration Support

Approved AI tools may be used to generate code drafts, refactorings, modernization steps, migration support, tests, documentation, and implementation explanations.

AI-generated code must be treated as untrusted until reviewed. Users must confirm correctness, maintainability, security, licensing implications, and consistency with internal coding standards.

Where an AI agent materially generates or transforms code, a responsible human must remain assigned for review, merge, and deployment decisions.

### 5.3. Testing, Quality, and Debugging Support

Approved AI tools may be used to propose tests, analyze failing tests and logs, suggest debugging hypotheses, and draft test data or fixtures where data handling rules permit it.

AI assistance must not be used to fabricate test evidence or to claim test coverage, performance results, or security assurance that was not actually achieved.

### 5.4. Documentation and Knowledge Support

Approved AI tools may be used to draft or improve developer documentation, onboarding materials, runbooks, release notes, and knowledge-transfer materials.

Users must verify that generated documentation accurately matches the implemented system and does not disclose confidential or restricted information inappropriately.

### 5.5. Operational and Automation Support

Approved AI tools may be used to assist with internal automation drafts, incident analysis, telemetry and ticket summarization, remediation planning, and post-incident follow-up preparation.

Operational use remains subject to existing change management, production access, segregation of duties, and incident management controls. AI-assisted workflows may prepare or recommend production changes, but state-changing production actions remain subject to the human approval requirements in this policy.

## 6. Restricted and Prohibited Use

The following restrictions apply even when an AI tool is otherwise approved.

### 6.1. No Unsupervised Delegation of Accountable Engineering Decisions

Users must distinguish between accountable engineering decisions and external side effects. AI may assist with analysis or execute a bounded and already authorized step, but users must not delegate the accountable engineering decision itself to AI.

Users must not allow AI agents to make final decisions on behalf of `[Organization]` for:

- Production releases.
- Security exceptions.
- Architecture approvals.
- Code review approvals where human review is required.
- Data access approvals.
- Incident severity classification where formal response obligations depend on the decision.

### 6.2. No Use of Unapproved Tools, Integrations, or Access Paths

Users must not:

- Connect agents to unapproved public MCP servers or external connectors.
- Install unverified skills, plugins, or extensions from public repositories.
- Circumvent approved procurement, legal review, vendor review, or security review processes.
- Route `[Organization]` work through personal AI accounts or unapproved shadow IT services.

### 6.3. No Non-`[Organization]` Use of `[Organization]`-Provisioned Licensed Tools

Users must not use AI tools made available under licenses provisioned by `[Organization]` for personal, external client, partner, or other non-`[Organization]` purposes. Such tools are permitted only for internal `[Organization]` use.

### 6.4. No Unauthorized Exposure of Sensitive Data

Users must not submit to unapproved AI services any content that includes, unless explicitly permitted by policy and tool approval conditions:

- Source code from internal repositories.
- Production credentials, secrets, tokens, keys, or certificates.
- Customer data, personal data, regulated data, or contractual confidential information.
- Security findings, incident details, or architectural information classified above the approved threshold for the tool.
- Internal documents that contain strategic, legal, financial, or merger-related information.

### 6.5. No Blind Acceptance of AI Outputs

Users must not:

- Merge AI-generated code without human review appropriate to the change risk.
- Deploy AI-generated changes without required testing and release controls.
- Represent AI-generated content as verified engineering fact when it has not been validated.
- Use AI output to bypass normal review depth, documentation, or evidence expectations.

### 6.6. No Bypass of Security or Compliance Controls

Users must not use AI tools to:

- Evade access controls, audit controls, security tooling, or segregation-of-duties requirements.
- Generate or execute payloads intended to disable safeguards or exploit internal systems.
- Create undocumented automation paths into production environments or sensitive data stores.

## 7. Approval and Onboarding of AI Tools and Integrations

### 7.1. Mandatory Approval Requirement

Users may use only AI tools and integrations that have been reviewed and approved for the intended use case under the workflow defined in Section 7.2. Approval must cover both the tool itself and any connected capabilities that materially change its risk profile, including plugins, APIs, MCP servers, or automation endpoints.

All such use must remain within the restrictions recorded in the official AI tool decision register, including any limits on environments, data classes, repositories, connected systems, user groups, approval steps, or permitted workflows.

### 7.2. Approval Workflow

The standard approval workflow is:

1. A requester submits a tool or integration request describing the intended engineering use case, users, data involved, connected systems, and expected operational benefit.
2. The AI Governance Function reviews the request for security, privacy, legal, licensing, operational, and autonomy-related risk, including the effect of connected capabilities and external integrations.
3. The AI Governance Function records one of the following decisions in the official AI tool decision register:
   - Approved.
   - Approved with restrictions.
   - Rejected.
4. Access is provisioned only after the required controls and approval conditions are in place.

### 7.3. Decision Register Management

The AI Governance Function must maintain the official AI tool decision register. The register should include, as applicable:

- Tool or integration name.
- Source location or `N/A` when no public source location is available.
- Tool description.
- Decision.
- Restrictions.
- Rationale.

The decision register may be maintained as a separate operational appendix to this policy, such as [`ai-governance-approved-tools-appendix.md`](./ai-governance-approved-tools-appendix.md), provided that the appendix remains governed under this policy framework.

### 7.4. Revalidation and Retirement

Approved tools must be reviewed periodically and when material changes occur, including:

- A significant product feature change.
- A change in vendor terms, hosting model, or model provider.
- A change in connected tools, prompts, memory features, update channels, or dependency provenance.
- A newly discovered security weakness or compliance concern.
- Expansion to new data types, repositories, or environments.

Approval may be suspended or revoked if the tool no longer meets `[Organization]` requirements.

## 8. Security and Engineering Control Requirements

Approved AI usage must meet the following baseline control requirements regardless of lifecycle stage. These controls complement, and do not replace, the acceptance, review, merge, and deployment gates defined in Section 9.

### 8.1. Identity, Authentication, and Access Control

- Enterprise authentication or an organization-approved controlled identity must be used for engineering AI activity.
- Shared anonymous accounts must not be used for engineering AI activity.
- Access to repositories, environments, and tools must remain role-based and least-privilege.
- Agent permissions must be scoped to the minimum set required for the assigned task.

### 8.2. Data Protection and Context Minimization

- Users must provide only the minimum data needed for the task.
- Sensitive code, tickets, logs, and documents must be redacted or withheld unless the approved tool explicitly permits that data class.
- Data submitted to AI systems must be handled according to `[Organization]` classification, retention, and privacy requirements.
- Persistent memory, retrieved context, embeddings, and shared knowledge stores must be treated as controlled data stores with validation, segregation, retention, and purge expectations appropriate to the risk.
- Approved internal or privacy-preserving deployment models must be used for higher-sensitivity work unless the approved use case explicitly authorizes another deployment model.

### 8.3. Secure Prompt and Tool Interaction Practices

- Users and approvers must assess AI-agent risks arising from external content, connected tools, autonomy, memory, and multi-step workflows.
- AI agents must not be granted broad tool execution rights without explicit scope limits, approval boundaries, and monitoring appropriate to the use case.
- Tool invocation paths and external side effects must be constrained to intended systems and approved operations.
- Detailed agentic threat and mitigation practices should be derived from the external guidance required by this policy, including the OWASP Top 10 for Agentic Applications where applicable.

### 8.4. Output Validation and Secure Coding Expectations

- AI-generated code must be treated as untrusted input until it has been technically validated under the applicable lifecycle gates defined in Section 9.
- Users must verify that generated code does not introduce known insecure patterns, hidden functionality, unsupported dependencies, or licensing conflicts.
- AI-generated infrastructure or configuration changes must be reviewed for operational safety, rollback feasibility, and blast radius.
- Security-sensitive changes may require additional review from security or platform specialists.

### 8.5. Logging, Monitoring, and Traceability

- Material AI-assisted actions must be logged or otherwise recoverable through normal engineering records.
- Logs must capture the responsible user, tool used, action taken, target system, and relevant data classification for the workflow records maintained under this policy.
- The Engineering Team Function must preserve sufficient evidence to support incident investigation, audit, and retrospective review.

### 8.6. Environment Isolation and Change Control

- Sensitive workflows must run in controlled environments with restricted connectivity and monitored access.
- AI-assisted automation must respect existing branch protections, CI controls, deployment approvals, and production change windows.
- Direct production actions by AI agents are prohibited unless an approved narrowly defined use case includes an authorized human approval step, compensating controls, and auditable traceability.

## 9. Lifecycle Control Gates for AI-Assisted Delivery

This section defines the mandatory stage-specific control gates for AI-assisted outputs produced during the lifecycle activities described in Section 5. Section 8 defines the baseline controls that apply to all approved AI use; this section defines when specific outputs may be accepted, merged, deployed, or otherwise relied on.

### 9.1. Requirements and Design Controls

- AI-generated requirements, user stories, and design proposals must be reviewed by authorized human reviewers designated by `[Organization]` for product and engineering review.
- The Engineering Team Function must confirm that non-functional requirements, security expectations, and compliance obligations are not omitted because of AI summarization or simplification.

### 9.2. Implementation Controls

- Users may use AI to accelerate implementation, but they remain responsible for understanding the submitted code.
- For AI-assisted changes proposed for merge, the responsible human submitter must be able to explain the change objective, logic, dependencies, risks, and validation performed.
- If an AI agent generated or materially transformed the submitted code, the agent may be recorded as the technical origin of the change, but accountability for merge, approval, and deployment outcomes must remain explicitly assigned to authorized human reviewers, approvers, or deployers.
- AI-assisted changes that add or modify high-impact AI integrations or connected capabilities must receive review appropriate to their privilege scope, provenance, and rollback risk.
- Large or high-risk AI-assisted changes must be broken into reviewable units unless an approved workflow requires a different review structure.

### 9.3. Testing and Validation Controls

- AI-assisted changes must pass the tests, checks, and quality gates appropriate to the repository and change type.
- Additional validation is required when the AI-generated output affects authentication, authorization, cryptography, payments, personal data handling, infrastructure, or production safety.

### 9.4. Review and Approval Controls

- Authorized human reviewers must review AI-assisted changes according to the same or stricter standards as other changes.
- Authorized human reviewers must challenge unclear logic, unverifiable claims, weak tests, unexplained dependencies, and suspicious code patterns regardless of whether the author used AI assistance.
- Required approvals must come from authorized humans, not from an AI-generated recommendation alone.

### 9.5. Deployment and Post-Deployment Controls

- AI-assisted releases must follow existing release management and deployment controls.
- Any state-changing production action prepared, recommended, or initiated through an AI-assisted workflow must require an authorized human approval step before execution.
- The Engineering Team Function must retain clear rollback plans and ownership for changes materially influenced by AI output.
- Post-deployment issues linked to AI-assisted work must be documented and fed back into tool usage guidance, approval conditions, or team practices.

## 10. Responsibilities

### 10.1. Users

Users must:

- Use only approved tools and approved integration paths.
- Understand the limitations of the AI capability they are using.
- Review the [OWASP Top 10 for Agentic Applications for 2026](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/) guidance and remain familiar with its relevant risks and mitigations when using AI agents or connected agentic workflows.
- Protect `[Organization]` and customer data when preparing prompts, files, logs, or repository context.
- Review, test, and validate AI-generated outputs before relying on them.
- Report suspicious, unsafe, or unexpected AI behavior.
- Escalate when a task appears to exceed the approved use boundaries of a tool.

### 10.2. Engineering Team Function

The Engineering Team Function must:

- Define practical team-level guidance for approved AI use in their repositories and workflows.
- Maintain code review, testing, and release discipline for AI-assisted changes.
- Implement guardrails that restrict unapproved integrations and unsafe automation paths.
- Monitor recurring quality or security issues associated with AI usage and address them.

### 10.3. Engineering Management Role and Technical Leadership Role

The Engineering Management Role and Technical Leadership Role must:

- Ensure team members understand this policy and the approved tooling model.
- Decide when additional review, pair validation, or specialist approval is needed for higher-risk AI-assisted work.
- Balance productivity goals against engineering quality and operational risk.

### 10.4. AI Governance Function

The AI Governance Function must:

- Operate as the approval body defined by `[Organization]` for AI tool governance.
- Execute and maintain the approval and onboarding process defined in Section 7.
- Maintain the approval framework, evaluation criteria, official AI tool decision register, and associated usage restrictions.
- Periodically reassess approved tools based on evolving risk, legal, and security considerations.
- Periodically review this policy and its approval criteria against current recognized external guidance, such as the OWASP Top 10 for Agentic Applications, and update control expectations where needed.
- Advise on secure use patterns, threat scenarios, and required controls.
- Monitor for misuse, anomalous behavior, or policy violations where monitoring is in scope.
- Support investigation and remediation when AI-assisted activity contributes to a security event.

## 11. Enforcement

Violations of this policy may result in one or more of the following actions, subject to applicable `[Organization]` procedures:

- Removal or restriction of access to AI tools or connected systems.
- Mandatory remediation steps, retraining, or increased review requirements.
- Security or compliance investigation.
- Revocation of approval for a tool, integration, or use case.
- Disciplinary action consistent with `[Organization]` policy and contractual obligations.

## 12. Review and Updates

This policy must be reviewed at least annually and whenever a material change occurs in the `[Organization]` AI operating model, including:

- Introduction of new AI-enabled engineering workflows.
- Significant changes in security threats or attack techniques.
- Material updates to recognized external guidance that affect this policy's control assumptions, threat coverage, or required user obligations.
- Regulatory, contractual, or legal changes affecting AI usage.
- Material incidents, audit findings, or recurring control failures related to AI-assisted development.
