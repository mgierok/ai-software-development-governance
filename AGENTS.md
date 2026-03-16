# Markdown Governance Instructions

## 1. Editing Workflow

- For every update, agents must review the existing section structure before editing and determine whether the intended change can be absorbed into an existing section.
- Agents must preserve numbering, heading hierarchy, formatting consistency, and terminology consistency across the full document after every change.
- If an edit changes headings, section numbering, file names, or document structure, agents must complete the reference maintenance required by Section 2 in the same change set.

## 2. Repository Reference Maintenance

- Whenever a file is renamed or moved, agents must update inbound references to that file across the repository in the same change set. Completed PRD and TASK artifacts are excluded from this requirement.
- Agents must treat `ai-engineering-policy-draft.md` as the primary source of truth for policy assumptions and definitions. When updating related governance documents, agents must keep dependent content aligned with that file and preserve terminology consistency with it.
- Whenever `ai-engineering-policy-draft.md`, `ai-engineering-policy-acknowledgement-template.md`, or `ai-governance-approved-tools-appendix.md` is updated, agents must review the repository root `README.md` for affected descriptions, procedures, and references and update `README.md` in the same change set whenever needed to preserve cross-document consistency.
- Whenever a Markdown heading changes, including a title change or a numeric prefix change, agents must update inbound heading references across the repository in the same change set.
- This requirement applies to Markdown links, text references, tables of contents, and any other repository content that points readers to the changed file or heading.

## 3. Consolidation and Anti-Duplication

- Before adding a new rule, agents must locate existing rules that cover the same intent and update, merge, or generalize them first.
- Agents must add a new rule only when the intent cannot be absorbed safely into an existing section.
- If two rules overlap, agents must unify them into one clearer rule.
- When related guidance already exists elsewhere in the same file, agents must reference the relevant section instead of restating the same instruction.

## 4. Document Structure and Section Design

- Markdown headings must use stable levels (`#`, `##`, `###`) and a predictable hierarchy.
- Sections must remain numbered, and numeric heading prefixes must stay sequential and consistent after edits.
- Section titles must be explicit and topic-oriented or action-oriented.
- Each section must address one operational question or one tightly related group of operational questions.
- Agents should prefer expanding the most relevant existing section over creating a shallow or overlapping section.

## 5. Formatting and Terminology Consistency

- Equivalent structures within a file must use consistent formatting, including heading style, list style, lead-in punctuation, capitalization, and terminology.
- Equivalent concepts must use the same terms throughout the file unless a terminology change is applied consistently across all affected content.
- This consistency is required to improve scanability and reduce interpretation errors.

## 6. Language, Purpose, and Scope

- All content written or updated under this workflow must be in English.
- These instructions define how agents must create, revise, and maintain governance-style Markdown documentation in this repository.
- This workflow applies only to governance-style Markdown content in this repository.
- Repository content must remain generic and reusable, without binding guidance, examples, or policies to any specific company or individual.
- When a document requires an organization, team, owner, approver, or similar concrete actor, agents must use clear placeholders that downstream adopters can replace for their own environment.
