# Contributing to this Project

First off, thank you for considering contributing! All contributions are welcome.

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

1. Check existing issues first — someone might have already reported it
2. Use the [bug report template](.github/ISSUE_TEMPLATE/bug_report.yml)
3. Include:
   - Clear title and description
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots if applicable
   - Environment details (OS, version, etc.)

### Suggesting Enhancements

1. Use the [feature request template](.github/ISSUE_TEMPLATE/feature_request.yml)
2. Explain why this enhancement would be useful
3. Consider how it aligns with the project's goals

### Pull Requests

1. Fork the repository and create your branch from `main`
2. Make sure pre-commit hooks pass: `pre-commit run --all-files`
3. Add tests for new functionality
4. Update documentation as needed
5. Follow [Conventional Commits](https://www.conventionalcommits.org/) format
6. Ensure CI passes before requesting review

## Development Setup

### Prerequisites

- Python 3.11+ or Node.js 20+ (depending on project type)
- Git
- A code editor with appropriate language extensions

### Setting Up the Development Environment

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/repo.git
cd repo

# Set up pre-commit hooks
pre-commit install

# Install dependencies
pip install -e ".[dev]"  # Python projects
# or
npm install              # JS/TS projects

# Run tests
pytest --cov             # Python
npm test                 # JS/TS
```

## Commit Message Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(optional scope): <description>

[optional body]

[optional footer(s)]
```

### Types

| Type      | Description                                          |
|-----------|------------------------------------------------------|
| feat:     | A new feature                                        |
| fix:      | A bug fix                                            |
| docs:     | Documentation only changes                           |
| style:    | Code style (formatting, missing semicolons, etc.)   |
| refactor: | Code change that neither fixes a bug nor adds a feat |
| test:     | Adding or updating tests                             |
| chore:    | Maintenance tasks                                    |
| ci:       | CI configuration changes                             |
| perf:     | Performance improvements                             |
| security: | Security updates                                     |

### Examples

```
feat(auth): add OAuth2 login support
fix(api): resolve timeout on large payloads
docs(readme): update installation instructions
refactor(db): simplify connection pooling logic
test(utils): add edge cases for string utilities
```

## Code Style Guidelines

- **Python:** Follow [PEP 8](https://peps.python.org/pep-0008/) (enforced by ruff)
- **JavaScript/TypeScript:** Follow [Airbnb Style Guide](https://github.com/airbnb/javascript) (enforced by eslint)
- **General:** Keep functions focused and under 50 lines; use meaningful names

## Code Review Process

1. All PRs require at least one review
2. Address all review comments before merging
3. Use [Draft PRs](https://github.blog/2019-02-14-introducing-draft-pull-requests/) for work-in-progress
4. Keep PRs small and focused (max ~400 lines changed)

## License

By contributing, you agree that your contributions will be licensed under the project's [MIT License](LICENSE).
