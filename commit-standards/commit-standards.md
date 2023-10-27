# Commit Standards
## Introduction
Having a consistent commit standard is crucial for maintaining a readable and understandable history of your repository. By following a set of conventions, team members can easily understand the changes just by looking at the commit messages. This guide outlines the best practices for commit standards.

## Commit Message Structure
A commit message should be structured as follows:
```bash
    <type>(<scope>): <subject>
    <BLANK LINE>
    <body>
    <BLANK LINE>
    <footer>
```

1. **Type**: Describes the nature of the change.
2. **Scope:** The component or part of the project affected by the change.
3. **Subject:** A brief summary of the change.
4. **Body:** A more detailed explanation of the change.
5. **Footer:** Any additional metadata, such as issue references.

## Common Commit Types
1. **feat:** A new feature.
2. **fix:** A bug fix.
3. **docs:** Documentation changes.
4. **style:** Code style changes (formatting, missing semi-colons, etc.).
5. **refactor:** Refactoring code.
6. **test:** Adding or updating tests.
7. **chore:** Maintenance tasks, such as dependencies updates.

## Commit Message Guidelines
1. **Use Imperative Tone:** Your commit message should be phrased in the imperative, present tense. For example, use "add" instead of "added" or "adds".
2. **Keep it Concise:** The subject line should be concise, typically under 50 characters.
3. **Provide a Detailed Body:** If the commit warrants it, provide a detailed body explaining the context of the change, why it was made, and the approach taken.
4. **Reference Issues:** If the commit relates to an issue in your issue tracker, reference it in the footer.
5. **Avoid Vague Messages:** Commit messages like "fixes bug" or "updates files" are not helpful. Be descriptive without being overly verbose.

## Example Commit Messages
* Correctly formatted:
```bash
feat(auth): add two-factor authentication
```
* With a body:
```csharp
refactor(database): switch to PostgreSQL from SQLite

SQLite was not scaling well with our increased traffic. PostgreSQL offers improved performance and scalability.
```

* Referencing an issue:
```makefile
fix(cart): resolve issue where items wouldn't update

Closes #123
```
## Conclusion
Commit standards are a crucial part of any collaborative development process. They ensure clarity and understanding across the team. By following these conventions, your team will benefit from a clear, structured, and readable commit history.
