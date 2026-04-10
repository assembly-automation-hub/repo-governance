# Repository Labels Guide

This document outlines the standard labels used in this repository for categorizing issues and pull requests.

## 1. Severity Labels
These labels operate on a 7-level scale and are utilized by the automated AI analysis script to assess the impact of changes.
* **severity: critical** (Color: `B60205`): Indicates production-breaking changes, security vulnerabilities, or data loss risks. This applies to exposed secrets, SQL injection, XSS, CSRF, broken authentication, or changes causing service outages.
* **severity: high** (Color: `D93F0B`): Represents core logic changes, API modifications, or breaking changes. It is used for significant logic updates affecting core functionality, permission and access control modifications, or database schema changes.
* **severity: elevated** (Color: `E36209`): Used for new features, modules, large refactors, or external integrations. It also covers modifications to data processing pipelines, error handling, or retry logic.
* **severity: medium** (Color: `E4E669`): Denotes new helpers, CI/CD changes, config changes, and dependency updates. This includes structural reorganization of existing code and adding files with meaningful functionality.
* **severity: moderate** (Color: `B4D455`): Marks minor feature additions, validation improvements, and small behavioral changes. It is applied when improving logging, updating environment variables, or adding new issue templates.
* **severity: low** (Color: `0E8A16`): Applies to documentation updates, cosmetic changes, and formatting fixes. It covers UI cosmetic updates without behavior impact, renaming, or updating editor configs.
* **severity: informational** (Color: `C5DEF5`): Used for trivial changes such as typos, whitespace, and comment rewording. This includes non-critical version bumps and adding blank lines.

## 2. Type Labels
These provide standard classification for issues and pull requests.
* **bug** (Color: `D73A4A`): Applied when something isn't working as expected.
* **enhancement** (Color: `A2EEEF`): Identifies a new feature or request.
* **documentation** (Color: `0075CA`): Indicates improvements or additions to project documentation.
* **security** (Color: `E11D48`): Highlights a security vulnerability or an audit finding.
* **performance** (Color: `F9D0C4`): Relates to a performance or optimization issue.
* **refactor** (Color: `D4C5F9`): Used for code quality or structural improvements.
* **dependencies** (Color: `0366D6`): Flags a dependency update, whether performed manually or automatically by Dependabot.

## 3. Workflow Labels
These labels manage the lifecycle and routing of tasks.
* **ai-generated** (Color: `6F42C1`): Marks items automatically created by the AI Issue Generator workflow.
* **needs triage** (Color: `FBCA04`): Shows that an item is awaiting its first review and classification.
* **wontfix** (Color: `FFFFFF`): Denotes that the issue or request will not be worked on.
* **duplicate** (Color: `CFD3D7`): Indicates that this issue or pull request already exists elsewhere.
* **good first issue** (Color: `7057FF`): Identifies tasks that are well-suited for newcomers to the project.
* **help wanted** (Color: `008672`): Signals that extra attention or external contribution is needed to resolve the task.
