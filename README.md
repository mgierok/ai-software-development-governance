# AI Software Development Governance

## 1. Purpose

This repository stores governance-style Markdown artifacts for AI-assisted software development, including the policy document and the acknowledgement template used to confirm that Users have read and accepted a released policy revision.

## 2. Repository Contents

- `ai-engineering-policy-draft.md`: The current policy source document.
- `ai-engineering-policy-acknowledgement-template.md`: The template used to prepare a revision-specific acknowledgement register.
- `ai-governance-approved-tools-appendix.md`: The appendix used to maintain the AI tool decision register under the policy framework.

## 3. Organization Policy Onboarding Procedure

This procedure defines how an adopting organization should prepare its policy baseline before issuing the first internal revision.

### 3.1. Fork the Repository

An adopting organization should begin by creating its own fork of this repository. The fork becomes the organization-managed workspace in which the policy draft, revision files, and acknowledgement records are maintained.

### 3.2. Review and Complete the Policy Draft

Before publishing any internal revision, the adopting organization should review `ai-engineering-policy-draft.md` in full and replace all organization-specific placeholders with values appropriate for its own environment.

At minimum, the organization should complete:

- The organization name placeholder.
- The governance, engineering, management, technical leadership, legal, executive, and security role placeholders used throughout the policy.
- Any approval quorum, review function, or equivalent operating model details needed to make the policy actionable.

### 3.3. Confirm Policy Readiness

Before creating the first revision, the adopting organization should confirm that the completed policy is internally consistent in terminology, ownership model, and approval workflow, and that organization-specific placeholders have been replaced where needed for operational use.

### 3.4. Issue the First Internal Revision

After the policy draft has been completed for the adopting organization, the first internal release should be issued using the policy release and acknowledgement procedure defined in Section 4.

## 4. Policy Release and Acknowledgement Procedure

This procedure applies after the onboarding workflow in Section 3 and governs both the first internal revision and all subsequent revisions.

### 4.1. Release a New Policy Revision

The AI Governance Function releases each new version of the policy and assigns it a revision identifier in the format `rev-YYYYMMDD`.

### 4.2. Create the Revision Directory

For each released revision, a new repository directory named with the revision identifier must be created.

### 4.3. Copy the Revision Files

The revision directory must contain:

- A copy of the updated policy file for the released revision, renamed to remove the `draft` suffix from the source filename.
- A copy of the acknowledgement template for that same revision, renamed to remove the `template` suffix from the source filename.

### 4.4. Replace Organization-Specific Placeholders in the Acknowledgement File

Before the revision is announced for confirmation, the acknowledgement file must be updated to replace any organization-specific placeholders carried forward from the template, including the `[Organization]` placeholder in the acknowledgement statement.

### 4.5. Prepare the Acknowledgement Metadata

Before the revision is announced for confirmation, the acknowledgement file must be completed with the required metadata for the released policy version, including the correct policy reference, revision identifier, modification date, and checksums.

### 4.6. User Review and Confirmation

Each User is required to read the released policy revision and confirm that review in the revision-specific acknowledgement file by adding their entry to the confirmation register.

### 4.7. User Commit and Push Requirement

Each User must record their own confirmation through a repository change created by that User. After adding their entry to the acknowledgement file, the User must commit and push that change to the repository.

## 5. License

This repository is distributed under the MIT License.

The current license permits private use, commercial use, copying, modification, distribution, sublicensing, and sale, provided that the copyright notice and license notice are retained in copies or substantial portions of the repository.
