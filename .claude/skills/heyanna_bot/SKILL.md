```markdown
# heyanna_bot Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `heyanna_bot` repository, a Python project built with the Flask framework. You'll learn about file organization, code style, commit message conventions, and how to structure and run tests. This guide will help you contribute code that aligns with the project's established standards.

## Coding Conventions

### File Naming
- Use **snake_case** for all filenames.
  - Example: `message_handler.py`, `user_service.py`

### Import Style
- Use **relative imports** within the package.
  - Example:
    ```python
    from .utils import parse_message
    from ..models import User
    ```

### Export Style
- Use **named exports** (explicitly listing what is exported from a module).
  - Example:
    ```python
    __all__ = ['parse_message', 'format_response']
    ```

### Commit Messages
- Follow **conventional commits** with the `fix` prefix for bug fixes.
- Keep commit messages concise (average 76 characters).
  - Example:
    ```
    fix: handle empty user input in message parser
    ```

## Workflows

### Adding a New Feature
**Trigger:** When you need to introduce new functionality.
**Command:** `/add-feature`

1. Create a new Python file using snake_case if needed.
2. Use relative imports to reference other modules.
3. Export new functions or classes using `__all__`.
4. Write or update tests in a corresponding `*.test.*` file.
5. Commit your changes using a conventional commit message.

### Fixing a Bug
**Trigger:** When you identify and resolve a bug.
**Command:** `/fix-bug`

1. Locate the relevant code and apply the fix.
2. Update or add tests to cover the bug scenario.
3. Use a commit message starting with `fix:` and a concise description.
4. Run all tests to confirm the fix.

### Writing and Running Tests
**Trigger:** When you need to verify code correctness.
**Command:** `/run-tests`

1. Write tests in files matching the `*.test.*` pattern (e.g., `message_handler.test.py`).
2. Use the project's preferred testing framework (unspecified; check project docs or ask a maintainer).
3. Run tests using the appropriate command for the chosen framework.

## Testing Patterns

- Test files are named with the pattern `*.test.*` (e.g., `bot_logic.test.py`).
- The testing framework is not specified; consult project documentation or maintainers for details.
- Place tests alongside the code they verify or in a dedicated tests directory.

## Commands
| Command      | Purpose                                   |
|--------------|-------------------------------------------|
| /add-feature | Start the workflow for adding new features |
| /fix-bug     | Begin the bug fixing workflow             |
| /run-tests   | Run all test suites                       |
```