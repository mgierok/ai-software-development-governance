# AI Software Development Governance

## 1. Purpose

This repository stores governance-style Markdown artifacts for AI-assisted software development, including the policy document and the acknowledgement template used to confirm that Users have read and accepted a released policy revision.

## 2. Repository Contents

- `ai-engineering-policy-draft.md`: The current policy source document.
- `ai-engineering-policy-acknowledgement-template.md`: The template used to prepare a revision-specific acknowledgement register.

## 3. Policy Release and Acknowledgement Procedure

### 3.1. Release a New Policy Revision

The AI Governance Function releases each new version of the policy and assigns it a revision identifier in the format `rev-YYYYMMDD`.

### 3.2. Create the Revision Directory

For each released revision, a new repository directory named with the revision identifier must be created.

### 3.3. Copy the Revision Files

The revision directory must contain:

- A copy of the updated policy file for the released revision, renamed to remove the `draft` suffix from the source filename.
- A copy of the acknowledgement template for that same revision, renamed to remove the `template` suffix from the source filename.

### 3.4. Prepare the Acknowledgement File

Before the revision is announced for confirmation, the acknowledgement file must be completed with the required metadata for the released policy version, including the correct policy reference, version details, modification date, and checksums.

### 3.5. User Review and Confirmation

Each User is required to read the released policy revision and confirm that review in the revision-specific acknowledgement file by adding their entry to the confirmation register.

### 3.6. User Commit and Push Requirement

Each User must record their own confirmation through a repository change created by that User. After adding their entry to the acknowledgement file, the User must commit and push that change to the repository.
