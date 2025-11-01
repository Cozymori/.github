# Contributing to RepublicOfGamja Projects

Thank you for your interest in contributing to RepublicOfGamja! We welcome contributions from everyone. By participating in our projects, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

## Getting Started

### Prerequisites

Before contributing, please ensure you have:
- A GitHub account
- Git installed on your local machine
- Basic understanding of Git and GitHub workflow
- Familiarity with the project's technology stack

### Setting Up Your Development Environment

1. Fork the repository to your GitHub account
2. Clone your fork locally:
```bash
   git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME.git
   cd REPOSITORY-NAME
```
3. Add the original repository as an upstream remote:
```bash
   git remote add upstream https://github.com/RepublicOfGamja/REPOSITORY-NAME.git
```
4. Create a new branch for your work:
```bash
   git checkout -b feature/your-feature-name
```

## How to Contribute

### Reporting Issues

Before creating an issue:
- Search existing issues to avoid duplicates
- Use the issue templates if available
- Provide clear and detailed information

When reporting bugs, include:
- Description of the bug
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots (if applicable)
- Environment details (OS, browser, version, etc.)

For feature requests, describe:
- The problem you're trying to solve
- Your proposed solution
- Alternative solutions you've considered

### Code Contributions

#### Code Style

- Follow the existing code style in the project
- Use meaningful variable and function names
- Write self-documenting code where possible
- Add comments for complex logic
- Keep functions small and focused
- Follow language-specific conventions

#### Testing

- Write tests for new features
- Ensure all existing tests pass
- Update tests when modifying existing functionality
- Aim for good test coverage

## Git Commit Message Guide

### Commit Message Format
```
<type>(<scope>): <subject>
```
- **type**: Type of commit (required)
- **scope**: Scope of changes (optional)
- **subject**: Brief description (required)

### Commit Types

#### feat: New feature
```bash
feat: Add new feature
feat(auth): Add user signup API endpoint
```

#### fix: Bug fix
```bash
fix: Fix bug
fix(parser): Fix null pointer exception
```

#### docs: Documentation changes
```bash
docs: Update documentation
docs(readme): Update installation guidelines
```

#### style: Code style changes (no functional changes)
```bash
style: Change code formatting
style(api): Apply Prettier formatting
```

#### refactor: Code refactoring (no functional changes)
```bash
refactor: Improve code structure
refactor(user): Simplify UserService logic
```

#### test: Test code changes
```bash
test: Add or modify tests
test(auth): Add test cases for login failures
```

#### chore: Build, configuration, and other miscellaneous tasks
```bash
chore: Update build configuration
chore: Add *.log to .gitignore
```

#### perf: Performance improvements
```bash
perf: Improve performance
perf(api): Optimize database query
```

#### ci: CI/CD configuration changes
```bash
ci: Update CI pipeline
ci: Add GitHub Actions workflow
```

#### build: Build system changes
```bash
build: Update dependencies
build: Update webpack configuration
```

#### revert: Revert previous commit
```bash
revert: Revert "feat: Add new feature"
```

### Best Practices

#### 1. Use imperative mood

✅ Good:
```bash
feat(auth): Add user login functionality
fix(api): Resolve CORS issue
docs: Update API documentation
```

❌ Bad:
```bash
feat(auth): Added user login functionality
fix(api): Resolved CORS issue
docs: Updated API documentation
```

#### 2. Keep subject line under 50 characters
```bash
✅ feat(auth): Add OAuth2 authentication
❌ feat(auth): Add OAuth2 authentication with Google, Facebook, and Twitter providers
```

#### 3. Capitalize the subject line
```bash
✅ feat: Add new feature
❌ feat: add new feature
```

#### 4. Don't end with a period
```bash
✅ feat: Add user authentication
❌ feat: Add user authentication.
```

#### 5. Use scope to specify the area of change
```bash
feat(auth): Add login endpoint
feat(user): Add profile page
feat(api): Add rate limiting
fix(database): Fix connection pool leak
```

### Advanced Usage

#### Breaking Changes
```bash
feat(api)!: Change authentication method to OAuth2

BREAKING CHANGE: JWT authentication is replaced with OAuth2.
Users need to update their authentication flow.
```

#### Multiple paragraphs
```bash
feat(auth): Add two-factor authentication

Implement TOTP-based 2FA using Google Authenticator.
Users can enable 2FA in their account settings.

Closes #123
```

#### Linking issues
```bash
fix(parser): Fix null pointer exception

Fixes #456
Closes #789
Related to #234
```

#### Revert commits
```bash
revert: Revert "feat(auth): Add OAuth2 support"

This reverts commit a1b2c3d4e5f6.
Reason: OAuth2 implementation caused performance issues.
```

### Complete Examples

**Example 1: New Feature**
```bash
feat(auth): Add user signup API endpoint
```

**Example 2: Bug Fix**
```bash
fix(parser): Fix null pointer exception in data parsing
```

**Example 3: Documentation**
```bash
docs(readme): Update installation guidelines
```

**Example 4: Style Change**
```bash
style(api): Apply Prettier formatting
```

**Example 5: Refactoring**
```bash
refactor(user): Simplify UserService logic
```

**Example 6: Test**
```bash
test(auth): Add test cases for login failures
```

**Example 7: Chore**
```bash
chore: Add *.log to .gitignore
```

**Example 8: Performance**
```bash
perf(database): Add index to user_id column
```

**Example 9: CI/CD**
```bash
ci: Add automated testing workflow
```

**Example 10: Breaking Change**
```bash
feat(api)!: Change response format to REST standard

BREAKING CHANGE: API responses now follow REST conventions.
Update client code to handle new response structure.
```

### Quick Reference

| Type     | Purpose        | Example                    |
|----------|----------------|----------------------------|
| feat     | New feature    | feat(auth): Add login      |
| fix      | Bug fix        | fix(api): Fix CORS         |
| docs     | Documentation  | docs: Update README        |
| style    | Formatting     | style: Apply linter        |
| refactor | Refactoring    | refactor: Clean up code    |
| test     | Testing        | test: Add unit tests       |
| chore    | Maintenance    | chore: Update deps         |
| perf     | Performance    | perf: Optimize query       |
| ci       | CI/CD          | ci: Add workflow           |
| build    | Build system   | build: Update config       |
| revert   | Revert         | revert: Revert commit      |

### Tips

- **Be specific**: Include scope when possible
- **Be concise**: Keep subject line short and clear
- **Be consistent**: Follow team conventions
- **Be descriptive**: Explain what and why, not how
- **Use body**: Add details for complex changes

### Common Scopes

- **auth**: Authentication/Authorization
- **api**: API endpoints
- **ui**: User interface
- **database**: Database changes
- **config**: Configuration
- **deps**: Dependencies
- **security**: Security-related
- **i18n**: Internationalization
- **a11y**: Accessibility
- **seo**: SEO-related

## Pull Request Process

### Before Submitting a PR

1. Ensure your code follows the project's style guidelines
2. Update documentation if you're changing functionality
3. Add or update tests as needed
4. Run the test suite locally
5. Rebase your branch on the latest upstream main/master
6. Squash commits if necessary to maintain a clean history

### Submitting a PR

1. Push your changes to your fork
2. Create a Pull Request from your branch to the upstream repository
3. Fill out the PR template completely
4. Link any related issues
5. Request reviews from maintainers if needed

### During Review

- Respond to feedback promptly
- Make requested changes in new commits
- Push changes to the same branch
- Re-request review after addressing feedback
- Be patient and respectful during the review process

### After Merge

- Delete your local branch
- Pull the latest changes from upstream
- Keep your fork synchronized

## Community

### Getting Help

- Check the documentation first
- Search existing issues and discussions
- Ask questions in discussions or appropriate channels
- Be clear and provide context when asking for help

### Recognition

We value all contributions, including:
- Code contributions
- Documentation improvements
- Bug reports
- Feature suggestions
- Helping others in the community
- Spreading the word about our projects

Contributors will be recognized in our projects' README files and release notes.

## License

By contributing to RepublicOfGamja projects, you agree that your contributions will be licensed under the same license as the project.

## 🌏 Translations

- [한국어 (Korean)](https://github.com/RepublicOfGamja/.github/blob/main/docs/ko/CONTRIBUTING.md)

Thank you for contributing to RepublicOfGamja! 🎉