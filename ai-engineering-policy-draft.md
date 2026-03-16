# AI-Assisted Software Development Policy

## 1. Purpose

This policy defines how `[Organization]` may use AI tools, including AI agents, during the software development lifecycle. Its purpose is to enable practical productivity gains while preserving engineering quality, security, legal compliance, and accountability for delivered software.

This policy establishes rules for:

- Selecting and approving AI tools used in software development.
- Using AI assistance in requirements analysis, design, implementation, testing, documentation, and operational support.
- Protecting `[Organization]` data, customer data, source code, and intellectual property when AI tools are used.
- Preventing unsafe delegation of engineering decisions to autonomous or semi-autonomous systems.
- Ensuring that authorized human personnel remain accountable for code, architecture, releases, and production outcomes.

This policy is intended to reduce risks including:

- Data leakage to unapproved external services.
- Introduction of insecure, incorrect, unlicensed, or non-compliant code.
- Unauthorized integrations, plugins, Skills, MCP servers, and automation paths.
- Prompt injection, malicious tool execution, and supply-chain compromise through AI-connected tooling.
- Loss of traceability in engineering decisions and software change history.

## 2. Scope

This policy applies to all personnel who use AI capabilities in connection with software delivery for `[Organization]`, including:

- Employees.
- Contractors.
- Interns.
- Third-party service providers acting on behalf of `[Organization]`.

For the purposes of this policy, User has the meaning defined in Section 3.11.

This policy applies to all AI-enabled software development activities, including:

- Product discovery and requirements drafting.
- Architecture and design support.
- Source code generation, editing, refactoring, and migration.
- Test creation, test maintenance, and debugging.
- Documentation, runbooks, and knowledge base content.
- CI/CD assistance, scripting, developer automation, and operational troubleshooting.
- Use of AI during code review, incident analysis, and post-incident remediation.

This policy applies to all AI delivery mechanisms used for engineering work, including:

- Chat-based AI assistants.
- IDE-integrated code assistants.
- Autonomous or semi-autonomous AI agents.
- Agent Skills, plugins, connectors, and APIs.
- Model Context Protocol (MCP) servers.
- External automation services invoked by AI systems.

This policy covers both:

- Internally built and internally hosted AI systems.
- Third-party, SaaS-provided, partner-provided, or open-source AI tools.

If an AI tool is used on `[Organization]` devices, `[Organization]` repositories, `[Organization]` tickets, `[Organization]` documents, or `[Organization]` data, it falls within the scope of this policy.

## 3. Definitions

### 3.1. AI Agent

An AI-enabled software system capable of executing tasks with limited or significant autonomy, including planning, calling tools, manipulating files, retrieving data, or taking actions across one or more systems.

### 3.2. AI-Assisted Software Development

The use of AI tools to support any part of the software development lifecycle, including ideation, specification, design, coding, testing, review, release preparation, operational support, and maintenance.

### 3.3. Skill

A callable capability used by an AI agent to perform a task, such as retrieving data, manipulating files, invoking scripts, calling APIs, or performing automation within an engineering workflow.

### 3.4. Model Context Protocol (MCP)

A protocol or integration mechanism that enables AI systems to interact with external tools, services, repositories, infrastructure components, or data sources through a standardized interface.

### 3.5. Approved AI Tool

An AI system, agent, model integration, Skill, plugin, connector, or MCP server that has been reviewed and explicitly authorized for use under the `[Organization]` approval process and is listed in the official AI tool decision register with a status of `Approved` or `Approved with restrictions`.

Approval applies only within the scope, environments, data classes, connected systems, and workflow conditions recorded in the official AI tool decision register. Listing in the register does not constitute unrestricted approval for all use cases, execution contexts, or connected capabilities.

### 3.6. High-Risk Change

A code, configuration, infrastructure, security, or data-related change that could materially affect production availability, confidentiality, integrity, regulatory obligations, customer trust, or financial outcomes if it is incorrect or misused.

### 3.7. AI Governance Function

The AI Governance Function is the organization-defined function, committee, or delegated authority that reviews and decides whether AI tools, integrations, and related capabilities may be used under this policy.

Under this policy, this function is assigned to `[AI Governance Function]`. It may include designated representatives from `[Engineering Governance Role]`, `[Platform or Architecture Governance Role]`, `[Security or Risk Governance Role]`, and `[Additional Governance Role]`.

### 3.8. Engineering Team Function

The Engineering Team Function is the organization-defined engineering team or equivalent delivery function responsible for repository-level implementation practices under this policy.

Under this policy, this function is assigned to `[Engineering Team Function]`.

### 3.9. Engineering Management Role

The Engineering Management Role is the organization-defined management role accountable for engineering team oversight under this policy.

Under this policy, this role is assigned to `[Engineering Management Role]`.

### 3.10. Technical Leadership Role

The Technical Leadership Role is the organization-defined technical leadership role accountable for architecture, quality, or delivery decisions under this policy.

Under this policy, this role is assigned to `[Technical Leadership Role]`.

### 3.11. User

Any employee, contractor, intern, or third-party service provider acting on behalf of `[Organization]` who uses AI tools, AI agents, or AI-enabled workflows covered by this policy.

### 3.12. Accountable Engineering Decision

A decision that selects, approves, authorizes, or rejects an engineering outcome on behalf of `[Organization]` where responsibility, escalation duties, compliance obligations, or formal governance consequences attach to that choice. Accountable engineering decisions include release approvals, security exceptions, architecture approvals, required code review approvals, production data access approvals, and incident severity classifications that determine formal response obligations.

An accountable engineering decision is not the same as executing a previously approved step. If a workflow has already been approved by the required human authority, later execution of that workflow may still create external side effects, but it does not transfer the underlying decision authority to the AI system.

### 3.13. External Side Effect

An action performed by an AI tool or AI agent that creates, modifies, deletes, transmits, grants, revokes, deploys, reconfigures, or otherwise changes state outside the current analytical exchange. External side effects include writing files, updating tickets, sending messages, calling APIs that change records, changing permissions, modifying infrastructure, or executing deployment steps.

An external side effect may occur without an accountable engineering decision if the action is merely carrying out a bounded and already authorized instruction. However, any such action remains subject to approval boundaries, access controls, and change controls under this policy.

### 3.14. State-Changing Production Action

Any external side effect that creates, modifies, deletes, deploys, restarts, scales, reconfigures, grants access in, or otherwise changes the behavior or data state of a production environment, production service, or production dataset. Read-only inspection, monitoring, and analysis do not by themselves constitute state-changing production actions.

## 4. Governance Principles

1. Human accountability remains mandatory.
   AI may assist with engineering work, but responsibility for design decisions, code quality, security posture, approvals, and production outcomes remains with authorized human personnel.
2. Default-deny for unapproved external capabilities.
   External AI-connected tools, public MCP servers, public Skills, and third-party connectors must not be used unless they have been approved.
3. Risk-based use is required.
   The level of oversight, validation, and control must increase in proportion to the sensitivity of the code, data, environment, and business impact involved.
4. Least privilege must be enforced.
   AI systems may receive only the minimum context, permissions, and tool access needed for the task being performed.
5. Verification before reliance is required.
   AI-generated outputs must be reviewed, tested, and validated before they are merged, deployed, shared externally, or treated as authoritative.
6. Traceability must be preserved.
   Significant AI-assisted work must remain attributable to a responsible user and recoverable through standard engineering records such as tickets, commits, reviews, logs, and change histories.
7. Security and compliance controls are not optional.
   AI use must operate within the same security, privacy, legal, and regulatory constraints that apply to any other engineering activity.
8. AI is a support capability, not an approval authority.
   AI tools may inform decisions, but they must not replace required human approvals in architecture review, security review, change management, or release governance.

## 5. Permitted Use in the Software Development Lifecycle

AI tools may be used to support software development when the use is consistent with this policy, the tool is approved, and required human review is applied.

This section defines the categories of development work for which AI assistance is permitted. The mandatory control gates that apply before AI-assisted outputs are accepted, merged, deployed, or otherwise relied on are defined in Section 9.

### 5.1. Planning, Analysis, and Design Support

Approved AI tools may be used to:

- Summarize product requirements, technical specifications, and issue histories.
- Propose solution options, design alternatives, and tradeoff analyses.
- Assist with drafting architecture notes, decision records, and implementation plans.
- Help identify dependencies, edge cases, failure modes, and operational considerations.

Users must validate that AI-generated analysis reflects the actual system context and does not omit important technical, security, or compliance constraints.

### 5.2. Coding, Refactoring, and Migration Support

Approved AI tools may be used to:

- Generate code drafts, scaffolding, repetitive boilerplate, tests, and documentation.
- Suggest refactorings, modernization steps, dependency updates, and migration approaches.
- Explain unfamiliar code, logs, configuration, or framework behavior to accelerate engineering work.
- Assist in translating logic between languages, frameworks, or internal system conventions.

AI-generated code must be treated as untrusted until reviewed. Engineers must confirm correctness, maintainability, security, licensing implications, and consistency with internal coding standards.

Where an AI agent generates, refactors, or migrates code with limited direct human authorship, the workflow must still assign a responsible human for review, merge, and deployment decisions as required by this policy.

### 5.3. Testing, Quality, and Debugging Support

Approved AI tools may be used to:

- Propose unit, integration, regression, and negative test cases.
- Help analyze failing tests, logs, traces, and error reports.
- Suggest debugging hypotheses and remediation options.
- Draft test data or test fixtures when allowed by data handling requirements.

AI assistance must not be used to fabricate test evidence or to claim test coverage, performance results, or security assurance that was not actually achieved.

### 5.4. Documentation and Knowledge Support

Approved AI tools may be used to:

- Draft developer documentation, onboarding materials, runbooks, and release notes.
- Improve clarity, structure, and consistency of existing technical documentation.
- Summarize implementation details for internal knowledge transfer.

Users must verify that generated documentation accurately matches the implemented system and does not disclose confidential or restricted information inappropriately.

### 5.5. Operational and Automation Support

Approved AI tools may be used to assist with:

- Drafting scripts for internal automation.
- Investigating incidents and operational anomalies.
- Summarizing telemetry, tickets, and operational timelines.
- Preparing remediation plans and post-incident follow-up items.

Operational use must remain subject to existing change management, production access, segregation of duties, and incident management controls.

AI-assisted operational workflows may prepare or recommend production changes, but execution of any state-changing production action must remain under the Human-in-the-Loop controls defined in Sections 8 and 9.

## 6. Restricted and Prohibited Use

The following restrictions apply even when an AI tool is otherwise approved.

### 6.1. No Unsupervised Delegation of Accountable Engineering Decisions

Users must distinguish between accountable engineering decisions and external side effects. An accountable engineering decision is the human-governed choice or approval described in Section 3.12. An external side effect is the execution activity described in Section 3.13. A workflow may involve both, but users must not delegate the accountable engineering decision to AI.

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
- Install unverified Skills, plugins, or extensions from public repositories.
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

Users may use only AI tools and integrations that have been reviewed and approved for the intended use case under the workflow defined in Section 7.2. Approval must cover both the tool itself and any connected capabilities that materially change its risk profile, including Skills, plugins, APIs, MCP servers, or automation endpoints.

All such use must remain within the restrictions recorded in the official AI tool decision register, including any limits on environments, data classes, repositories, connected systems, user groups, approval steps, or permitted workflows.

### 7.2. Approval Workflow

The standard approval workflow is:

1. A requester submits a tool or integration request describing the intended engineering use case, users, data involved, connected systems, and expected operational benefits.
2. The AI Governance Function operates as the approval body for this workflow.
3. The AI Governance Function assesses:
   - Security architecture and authentication model.
   - Data handling, retention, residency, and training usage terms.
   - Vendor risk, licensing terms, and legal restrictions.
   - Operational reliability, supportability, and business continuity implications.
   - Potential for prompt injection, privilege escalation, or unsafe autonomous behavior.
4. The AI Governance Function decides whether the request also requires an additional opinion from `[Legal Review Function]` or `[Executive Leadership Function]`.
5. If an additional opinion is required, that opinion must be obtained and considered before a final approval decision is recorded.
6. At least `[Approval Quorum]` members of the AI Governance Function review the request and record one of the following decisions:
   - Approved.
   - Approved with restrictions.
   - Rejected.
7. Any approval conditions, such as environment limits or data restrictions, are recorded in the official AI tool decision register.
8. Access is provisioned only after the required controls are in place.

### 7.3. Decision Register Management

The AI Governance Function must maintain the official AI tool decision register. The register should include, as applicable:

- Tool or integration name.
- GitHub link or `N/A` when no public repository is available.
- Tool description.
- Decision.
- Restrictions.
- Rationale.

The decision register may be maintained as a separate operational appendix to this policy, such as [`ai-governance-approved-tools-appendix.md`](./ai-governance-approved-tools-appendix.md), provided that the appendix remains governed under this policy framework.

### 7.4. Revalidation and Retirement

Approved tools must be reviewed periodically and when material changes occur, including:

- A significant product feature change.
- A change in vendor terms, hosting model, or model provider.
- A newly discovered security weakness or compliance concern.
- Expansion to new data types, repositories, or environments.

Approval may be suspended or revoked if the tool no longer meets `[Organization]` requirements.

## 8. Security and Engineering Control Requirements

Approved AI usage must meet the following baseline control requirements regardless of lifecycle stage. These controls complement, and do not replace, the stage-specific acceptance, review, merge, and deployment gates defined in Section 9.

### 8.1. Identity, Authentication, and Access Control

- Enterprise authentication or equivalent controlled identity must be used wherever available.
- Shared anonymous accounts must not be used for engineering AI activity.
- Access to repositories, environments, and tools must remain role-based and least-privilege.
- Agent permissions must be scoped to the minimum set required for the assigned task.

### 8.2. Data Protection and Context Minimization

- Users must provide only the minimum data needed for the task.
- Sensitive code, tickets, logs, and documents must be redacted or withheld unless the approved tool explicitly permits that data class.
- Data submitted to AI systems must be handled according to `[Organization]` classification, retention, and privacy requirements.
- Where technically feasible, approved internal or privacy-preserving deployment models should be preferred for higher-sensitivity work.

### 8.3. Secure Prompt and Tool Interaction Practices

- Users must consider prompt injection and malicious content risks when providing external content, logs, web results, or repository material to AI agents.
- AI agents must not be granted broad tool execution rights without guardrails, approval boundaries, and monitoring.
- Tool invocation paths must be constrained to intended systems and approved operations.
- External side effects must be explicitly bounded to approved systems, operations, and authorization paths.
- Human-in-the-Loop workflows are mandatory for any state-changing production action.
- For state-changing production actions, the workflow must require an authorized human to review the intended target, proposed change, and expected effect and to issue the approval that permits execution.

### 8.4. Output Validation and Secure Coding Expectations

- AI-generated code must be treated as untrusted input until it has been technically validated under the applicable lifecycle gates defined in Section 9.
- Engineers must verify that generated code does not introduce known insecure patterns, hidden functionality, unsupported dependencies, or licensing conflicts.
- AI-generated infrastructure or configuration changes must be reviewed for operational safety, rollback feasibility, and blast radius.
- Security-sensitive changes may require additional review from security or platform specialists.

### 8.5. Logging, Monitoring, and Traceability

- Material AI-assisted actions should be logged or otherwise recoverable through normal engineering records.
- Logs should capture, where feasible and appropriate, the responsible user, tool used, action taken, target system, and relevant data classification.
- Teams must preserve sufficient evidence to support incident investigation, audit, and retrospective review.

### 8.6. Environment Isolation and Change Control

- Sensitive workflows should run in controlled environments with restricted connectivity and monitored access.
- AI-assisted automation must respect existing branch protections, CI controls, deployment approvals, and production change windows.
- Direct production actions by AI agents are prohibited unless an approved narrowly defined use case includes an authorized Human-in-the-Loop approval step, compensating controls, and auditable traceability.

## 9. Lifecycle Control Gates for AI-Assisted Delivery

This section defines the mandatory stage-specific control gates for AI-assisted outputs produced during the lifecycle activities described in Section 5. Section 8 defines the baseline controls that apply to all approved AI use; this section determines when specific outputs may be accepted, merged, deployed, or otherwise relied on.

### 9.1. Requirements and Design Controls

- AI-generated requirements, user stories, and design proposals must be reviewed by accountable product and engineering stakeholders.
- Teams must confirm that non-functional requirements, security expectations, and compliance obligations are not omitted because of AI summarization or simplification.

### 9.2. Implementation Controls

- Developers may use AI to accelerate implementation, but they remain responsible for understanding the submitted code.
- For AI-assisted changes proposed for merge, the responsible human submitter must be able to explain the change objective, logic, dependencies, risks, and validation performed.
- If an AI agent generated or materially transformed the submitted code, the agent may be recorded as the technical origin of the change, but accountability for merge, approval, and deployment outcomes must remain explicitly assigned to authorized human reviewers, approvers, or deployers.
- Large or high-risk AI-assisted changes should be broken into reviewable units where practical.

### 9.3. Testing and Validation Controls

- AI-assisted changes must pass the tests, checks, and quality gates appropriate to the repository and change type.
- Additional validation is required when the AI-generated output affects authentication, authorization, cryptography, payments, personal data handling, infrastructure, or production safety.

### 9.4. Review and Approval Controls

- Human reviewers must review AI-assisted changes according to the same or stricter standards as other changes.
- Reviewers should challenge unclear logic, unverifiable claims, weak tests, unexplained dependencies, and suspicious code patterns regardless of whether the author used AI assistance.
- Required approvals must come from authorized humans, not from an AI-generated recommendation alone.

### 9.5. Deployment and Post-Deployment Controls

- AI-assisted releases must follow existing release management and deployment controls.
- Any state-changing production action prepared, recommended, or initiated through an AI-assisted workflow must require an authorized human approval step before execution.
- Teams must retain clear rollback plans and ownership for changes materially influenced by AI output.
- Post-deployment issues linked to AI-assisted work must be documented and fed back into tool usage guidance, approval conditions, or team practices.

## 10. Responsibilities

### 10.1. Users

Users must:

- Use only approved tools and approved integration paths.
- Understand the limitations of the AI capability they are using.
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
- Regulatory, contractual, or legal changes affecting AI usage.
- Material incidents, audit findings, or recurring control failures related to AI-assisted development.
