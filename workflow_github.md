# **WORKFLOW GITHUB**

This document describes the structure of the project Idyie, its organization into submodules, and the Git workflow policy we follow, including commit conventions and pull request (PR) practices.

## 🗂️ Project Structure

The project's main repository is the [Epitech repository](https://github.com/EpitechPromo2026/G-EIP-700-NCE-7-1-eip-corentin.levet), which contains the four following submodules located in the [Idyie](https://github.com/IdyieOrg) organisation:
- [IdyieAPI](https://github.com/IdyieOrg/IdyieAPI): The backend API service that handles requests and responses.
- [IdyieFormatter](https://github.com/IdyieOrg/IdyieFormatter): The service responsible for formatting and processing data.
- [IdyieLLM](https://github.com/IdyieOrg/IdyieLLM): The service that manages interactions with the language model.
- [IdyieWeb](https://github.com/IdyieOrg/IdyieWeb): The web interface for users to interact with the system.

## 🔁 Git Workflow

We follow a simplified **GitHub Flow**:

1. **Main Branches**:
  - `main`: Stable, production-ready code
  - `prod`: Only present on IdyieWeb, it is used to put on the [Idyie website](https://idyie.site/login)

2. **Feature/Bugfix Branches**:
  - Branch from: `main`
    - Naming convention: The branch name should be clear and descriptive
    - Utilization: For developing new features, bug fixes, or improvements, once the work is done, it should be merged into `main` via a pull request and deleted.

## ✍️ Commit Message Convention

Commit messages should be clear, concise and written in English. They must have the following symbol at the beginning to indicate their type:
- `[+]`: new features
- `[~]`: bug fixes or improvements of existing features
- `[-]`: removals or deprecations

## 🔀 Pull Request Guidelines

- Add a clear title and comment explaining the changes made.
- Select the appropriate labels for the PR.
- Ensure the PR is based on the latest `main` branch.
- Once approved, merge the PR into `main` and delete the branch.
- PRs should:
  -  Be small and focused (1 feature or fix max)
  -  Include tests if applicable
  -  Pass all CI checks before review
  -  Be reviewed by at least one team member before merging

## ✅ CI/CD Integration
Our GitHub Actions CI runs on:
- push to `main`
- pull_request targeting `main`

CI steps include:
- Linting
- Build
- Unit tests
- Optional deployment steps on `prod` branch for IdyieWeb

Workflows of each submodule are defined in their respective `.github/workflows/` directories.
