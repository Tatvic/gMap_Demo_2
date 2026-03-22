# Contributing to gMap_Demo_2

Thank you for your interest in contributing! This document provides guidelines and standards for contributing to this project.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Branch Strategy](#branch-strategy)
- [Commit Standards](#commit-standards)
- [Pull Request Process](#pull-request-process)
- [Code Review Guidelines](#code-review-guidelines)
- [Testing Requirements](#testing-requirements)
- [Style Guide](#style-guide)

## 📜 Code of Conduct

We are committed to providing a welcoming and inclusive experience. All contributors are expected to:

- Be respectful and inclusive
- Provide constructive feedback
- Focus on what is best for the project
- Accept responsibility for mistakes

## 🚀 Getting Started

### Prerequisites

1. Ensure you have access to the repository
2. Set up your development environment (see README.md)
3. Familiarize yourself with the project structure

### First-Time Setup

```bash
# Clone the repository
git clone https://github.com/Tatvic/gMap_Demo_2.git
cd gMap_Demo_2

# Install dependencies
{{INSTALL_COMMAND}}

# Set up pre-commit hooks (if applicable)
{{SETUP_HOOKS_COMMAND}}
```

## 🔄 Development Workflow

### 1. Pick a Task

- Check the project board or issue tracker
- Assign yourself to the task
- Move task to "In Progress"

### 2. Create a Branch

```bash
# Always start from dev
git checkout dev
git pull origin dev

# Create your feature branch
git checkout -b feature/TICKET-123-short-description
```

### 3. Make Changes

- Write clean, documented code
- Follow our style guide
- Add/update tests as needed

### 4. Commit Changes

```bash
# Stage changes
git add .

# Commit with conventional format
git commit -m "feat(auth): add Google OAuth integration"
```

### 5. Push and Create PR

```bash
git push origin feature/TICKET-123-short-description
```

Then create a Pull Request via GitHub.

## 🌿 Branch Strategy

We follow a structured branch hierarchy:

```
main ← Production deployments only
  │
  └── qa ← Staging/QA testing
       │
       └── dev ← Active development
            │
            ├── feature/*  ← New features
            ├── bugfix/*   ← Bug fixes
            └── hotfix/*   ← Urgent production fixes
```

### Branch Naming Convention

| Type | Pattern | Example |
|------|---------|---------|
| Feature | `feature/TICKET-###-description` | `feature/PROJ-123-add-login` |
| Bugfix | `bugfix/TICKET-###-description` | `bugfix/PROJ-456-fix-header` |
| Hotfix | `hotfix/TICKET-###-description` | `hotfix/PROJ-789-fix-crash` |

### Rules

- **feature/** branches → PR to `dev`
- **bugfix/** branches → PR to `dev` (or `qa` for staging bugs)
- **hotfix/** branches → PR to `main` (critical production fixes)

## 📝 Commit Standards

We use [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

### Types

| Type | Description |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation changes |
| `style` | Code style (formatting, semicolons, etc.) |
| `refactor` | Code refactoring |
| `perf` | Performance improvements |
| `test` | Adding/updating tests |
| `build` | Build system changes |
| `ci` | CI/CD changes |
| `chore` | Maintenance tasks |
| `revert` | Reverting changes |

### Examples

```bash
# Feature commit
git commit -m "feat(auth): add password reset functionality"

# Bug fix with issue reference
git commit -m "fix(api): resolve null pointer in user service

Fixes #123"

# Breaking change
git commit -m "feat(api)!: change response format

BREAKING CHANGE: Response now returns array instead of object"
```

### Commit Best Practices

- ✅ Write clear, descriptive messages
- ✅ Keep commits focused and atomic
- ✅ Reference ticket numbers
- ❌ Don't commit secrets or credentials
- ❌ Avoid "WIP" or "temp" commits

## 🔀 Pull Request Process

### Before Creating a PR

1. [ ] Ensure all tests pass locally
2. [ ] Run linter and fix issues
3. [ ] Update documentation if needed
4. [ ] Rebase on latest target branch

### PR Creation Checklist

Use this template when creating PRs:

```markdown
## What

Brief description of the changes.

## Why

Motivation and context for the changes.

## How

Technical approach taken.

## Testing

How was this tested?

## Checklist

- [ ] Tests added/updated
- [ ] Documentation updated
- [ ] No breaking changes (or noted in description)
- [ ] Reviewed my own code
```

### PR Size Guidelines

| Size | Lines Changed | Target |
|------|--------------|--------|
| **Small** | < 200 | Ideal |
| **Medium** | 200-400 | Acceptable |
| **Large** | 400-800 | Split if possible |
| **XL** | > 800 | Must split |

### Review Timeline

| PR Size | Expected Review Time |
|---------|---------------------|
| Small/Medium | 4-8 hours |
| Large | 24 hours |
| Critical/Hotfix | 2 hours |

## 👀 Code Review Guidelines

### For Authors

- Respond to feedback promptly
- Explain decisions when asked
- Make requested changes or explain why not
- Keep discussions professional

### For Reviewers

- Review within the expected timeline
- Be constructive and specific
- Approve when satisfied
- Use appropriate review actions:
  - **Comment**: Suggestions, questions
  - **Request Changes**: Must be addressed
  - **Approve**: Good to merge

### Review Focus Areas

1. **Functionality**: Does it work as intended?
2. **Code Quality**: Is it clean and maintainable?
3. **Tests**: Are there sufficient tests?
4. **Security**: Any security concerns?
5. **Performance**: Any performance issues?

## 🧪 Testing Requirements

### Minimum Requirements

- Unit test coverage: **80%+**
- All existing tests pass
- New features have tests
- Bug fixes include regression tests

### Running Tests

```bash
# Run all tests
{{TEST_COMMAND}}

# Run with coverage
{{COVERAGE_COMMAND}}

# Run specific tests
{{SPECIFIC_TEST_COMMAND}}
```

## 🎨 Style Guide

### Code Formatting

- Use project-configured formatter
- Run before committing: `{{FORMAT_COMMAND}}`

### Naming Conventions

| Element | Convention | Example |
|---------|------------|---------|
| Variables | camelCase | `userName` |
| Functions | camelCase | `getUserName()` |
| Classes | PascalCase | `UserService` |
| Constants | UPPER_SNAKE | `MAX_RETRIES` |
| Files | kebab-case | `user-service.js` |

### Documentation

- Add JSDoc/docstrings to public functions
- Update README for new features
- Keep inline comments minimal but meaningful

---

## Questions?

If you have questions about contributing, reach out to:

- **Tech Lead**: {{TECH_LEAD_EMAIL}}
- **Team Channel**: #{{TEAM_SLACK_CHANNEL}}

Thank you for contributing! 🙏
