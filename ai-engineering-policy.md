# AI-Assisted Software Development Policy

## 1. Purpose

This policy defines how the company may use AI tools, including AI agents, during the software development lifecycle. Its purpose is to enable practical productivity gains while preserving engineering quality, security, legal compliance, and accountability for delivered software.

This policy establishes rules for:

- Selecting and approving AI tools used in software development.
- Using AI assistance in requirements analysis, design, implementation, testing, documentation, and operational support.
- Protecting company data, customer data, source code, and intellectual property when AI tools are used.
- Preventing unsafe delegation of engineering decisions to autonomous or semi-autonomous systems.
- Ensuring that human employees remain accountable for code, architecture, releases, and production outcomes.

This policy is intended to reduce risks including:

- Data leakage to unapproved external services.
- Introduction of insecure, incorrect, unlicensed, or non-compliant code.
- Unauthorized integrations, plugins, Skills, MCP servers, and automation paths.
- Prompt injection, malicious tool execution, and supply-chain compromise through AI-connected tooling.
- Loss of traceability in engineering decisions and software change history.

## 2. Scope

This policy applies to all personnel who use AI capabilities in connection with software delivery for the company, including:

- Employees.
- Contractors.
- Interns.
- Third-party service providers acting on behalf of the company.

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

- Company-built and internally hosted AI systems.
- Third-party, SaaS-provided, partner-provided, or open-source AI tools.

If an AI tool is used on company devices, company repositories, company tickets, company documents, or company data, it falls within the scope of this policy.

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

An AI system, agent, model integration, Skill, plugin, connector, or MCP server that has been reviewed and explicitly authorized for use under the company approval process and is listed in the official registry of approved capabilities.

### 3.6. High-Risk Change

A code, configuration, infrastructure, security, or data-related change that could materially affect production availability, confidentiality, integrity, regulatory obligations, customer trust, or financial outcomes if it is incorrect or misused.

### 3.7. Governance Group

A cross-functional group responsible for defining approval criteria and making decisions about the use of AI tools in software development. The group typically includes representatives from:

- Security.
- Platform engineering.
- Software engineering leadership.
- Compliance or risk management.
- Legal or procurement, where applicable.
- AI governance or technology governance functions.

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

## 6. Restricted and Prohibited Use

The following restrictions apply even when an AI tool is otherwise approved.

### 6.1. No Unsupervised Delegation of Accountable Engineering Decisions

Users must not allow AI agents to make final decisions on behalf of the company for:

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
- Route company work through personal AI accounts or unapproved shadow IT services.

### 6.3. No Unauthorized Exposure of Sensitive Data

Users must not submit to unapproved AI services any content that includes, unless explicitly permitted by policy and tool approval conditions:

- Source code from restricted repositories.
- Production credentials, secrets, tokens, keys, or certificates.
- Customer data, personal data, regulated data, or contractual confidential information.
- Security findings, incident details, or architectural information classified above the approved threshold for the tool.
- Internal documents that contain strategic, legal, financial, or merger-related information.

### 6.4. No Blind Acceptance of AI Outputs

Users must not:

- Merge AI-generated code without human review appropriate to the change risk.
- Deploy AI-generated changes without required testing and release controls.
- Represent AI-generated content as verified engineering fact when it has not been validated.
- Use AI output to bypass normal review depth, documentation, or evidence expectations.

### 6.5. No Bypass of Security or Compliance Controls

Users must not use AI tools to:

- Evade access controls, audit controls, security tooling, or segregation-of-duties requirements.
- Generate or execute payloads intended to disable safeguards or exploit internal systems.
- Create undocumented automation paths into production environments or sensitive data stores.

## 7. Approval and Onboarding of AI Tools and Integrations

### 7.1. Mandatory Approval Requirement

Employees may use only AI tools and integrations that have been reviewed and approved for the intended use case. Approval must cover both the tool itself and any connected capabilities that materially change its risk profile, including Skills, plugins, APIs, MCP servers, or automation endpoints.

### 7.2. Approval Workflow

The standard approval workflow is:

1. A requester submits a tool or integration request describing the intended engineering use case, users, data involved, connected systems, and expected operational benefits.
2. The governance group or delegated reviewers assess:
   - Security architecture and authentication model.
   - Data handling, retention, residency, and training usage terms.
   - Vendor risk, licensing terms, and legal restrictions.
   - Operational reliability, supportability, and business continuity implications.
   - Potential for prompt injection, privilege escalation, or unsafe autonomous behavior.
3. The tool is classified as:
   - Approved.
   - Approved with restrictions.
   - Rejected.
4. Any approval conditions, such as environment limits or data restrictions, are recorded in the official registry.
5. Access is provisioned only after the required controls are in place.

### 7.3. Registry Management

The governance group must maintain a current registry of approved AI tools and integrations. The registry should include, as applicable:

- Tool or integration name.
- Approved use cases.
- Approved user groups or teams.
- Permitted data classes.
- Connected systems and permissions granted.
- Risk classification.
- Required monitoring or logging controls.
- Usage restrictions or prohibitions.
- Approval owner and review date.

### 7.4. Revalidation and Retirement

Approved tools must be reviewed periodically and when material changes occur, including:

- A significant product feature change.
- A change in vendor terms, hosting model, or model provider.
- A newly discovered security weakness or compliance concern.
- Expansion to new data types, repositories, or environments.

Approval may be suspended or revoked if the tool no longer meets company requirements.

## 8. Security and Engineering Control Requirements

Approved AI usage must meet the following control requirements.

### 8.1. Identity, Authentication, and Access Control

- Enterprise authentication or equivalent controlled identity must be used wherever available.
- Shared anonymous accounts must not be used for engineering AI activity.
- Access to repositories, environments, and tools must remain role-based and least-privilege.
- Agent permissions must be scoped to the minimum set required for the assigned task.

### 8.2. Data Protection and Context Minimization

- Users must provide only the minimum data needed for the task.
- Sensitive code, tickets, logs, and documents must be redacted or withheld unless the approved tool explicitly permits that data class.
- Data submitted to AI systems must be handled according to company classification, retention, and privacy requirements.
- Where technically feasible, approved internal or privacy-preserving deployment models should be preferred for higher-sensitivity work.

### 8.3. Secure Prompt and Tool Interaction Practices

- Users must consider prompt injection and malicious content risks when providing external content, logs, web results, or repository material to AI agents.
- AI agents must not be granted broad tool execution rights without guardrails, approval boundaries, and monitoring.
- Tool invocation paths must be constrained to intended systems and approved operations.
- Autonomous actions with external side effects must require explicit policy-aligned authorization.

### 8.4. Output Validation and Secure Coding Expectations

- AI-generated code must undergo the same secure coding, review, and testing expectations as human-authored code.
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
- Direct production actions by AI agents are prohibited unless explicitly approved for a narrowly defined use case with compensating controls.

## 9. Software Delivery Process Requirements

AI use in software delivery must align with standard engineering controls at each lifecycle stage.

### 9.1. Requirements and Design Stage

- AI-generated requirements, user stories, and design proposals must be reviewed by accountable product and engineering stakeholders.
- Teams must confirm that non-functional requirements, security expectations, and compliance obligations are not omitted because of AI summarization or simplification.

### 9.2. Implementation Stage

- Developers may use AI to accelerate implementation, but they remain responsible for understanding the submitted code.
- Code authors must be able to explain the logic, dependencies, and risks of AI-assisted changes they propose for merge.
- Large or high-risk AI-assisted changes should be broken into reviewable units where practical.

### 9.3. Testing and Validation Stage

- AI-assisted changes must pass the tests, checks, and quality gates appropriate to the repository and change type.
- Additional validation is required when the AI-generated output affects authentication, authorization, cryptography, payments, personal data handling, infrastructure, or production safety.

### 9.4. Review and Approval Stage

- Human reviewers must review AI-assisted changes according to the same or stricter standards as other changes.
- Reviewers should challenge unclear logic, unverifiable claims, weak tests, unexplained dependencies, and suspicious code patterns regardless of whether the author used AI assistance.
- Required approvals must come from authorized humans, not from an AI-generated recommendation alone.

### 9.5. Deployment and Post-Deployment Stage

- AI-assisted releases must follow existing release management and deployment controls.
- Teams must retain clear rollback plans and ownership for changes materially influenced by AI output.
- Post-deployment issues linked to AI-assisted work must be documented and fed back into tool usage guidance, approval conditions, or team practices.

## 10. Responsibilities

### 10.1. Employees and Individual Contributors

Employees and contributors who use AI tools for software development must:

- Use only approved tools and approved integration paths.
- Understand the limitations of the AI capability they are using.
- Protect company and customer data when preparing prompts, files, logs, or repository context.
- Review, test, and validate AI-generated outputs before relying on them.
- Report suspicious, unsafe, or unexpected AI behavior.
- Escalate when a task appears to exceed the approved use boundaries of a tool.

### 10.2. Engineering Teams

Engineering teams must:

- Define practical team-level guidance for approved AI use in their repositories and workflows.
- Maintain code review, testing, and release discipline for AI-assisted changes.
- Implement guardrails that restrict unapproved integrations and unsafe automation paths.
- Monitor recurring quality or security issues associated with AI usage and address them.

### 10.3. Engineering Managers and Technical Leads

Engineering managers and technical leads must:

- Ensure team members understand this policy and the approved tooling model.
- Decide when additional review, pair validation, or specialist approval is needed for higher-risk AI-assisted work.
- Balance productivity goals against engineering quality and operational risk.

### 10.4. Governance Group

The governance group must:

- Maintain the approval framework and evaluation criteria for AI tools.
- Review requests for tools, Skills, MCP servers, and related integrations.
- Maintain the official approved registry and associated usage restrictions.
- Periodically reassess approved tools based on evolving risk, legal, and security considerations.
- Advise on secure use patterns, threat scenarios, and required controls.
- Monitor for misuse, anomalous behavior, or policy violations where monitoring is in scope.
- Support investigation and remediation when AI-assisted activity contributes to a security event.

## 11. Enforcement

Violations of this policy may result in one or more of the following actions, subject to applicable company procedures:

- Removal or restriction of access to AI tools or connected systems.
- Mandatory remediation steps, retraining, or increased review requirements.
- Security or compliance investigation.
- Revocation of approval for a tool, integration, or use case.
- Disciplinary action consistent with company policy and contractual obligations.

## 12. Review and Updates

This policy must be reviewed at least annually and whenever a material change occurs in the company AI operating model, including:

- Introduction of new AI-enabled engineering workflows.
- Significant changes in security threats or attack techniques.
- Regulatory, contractual, or legal changes affecting AI usage.
- Material incidents, audit findings, or recurring control failures related to AI-assisted development.

Policy updates must preserve section numbering, structural consistency, and repository reference integrity in accordance with the repository governance instructions.
