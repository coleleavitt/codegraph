```markdown
# codegraph Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `codegraph` TypeScript codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to write and run tests. This guide is designed to help you contribute code that fits seamlessly with the existing project style.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myComponent.ts`, `dataFetcher.test.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In dataFetcher.ts
    export function fetchData() { ... }
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use `fix` as the prefix for bug fixes.
  - Example:
    ```
    fix: resolve issue with data parsing in fetchData
    ```

## Workflows

### Writing and Running Tests
**Trigger:** When adding or modifying functionality
**Command:** `/run-tests`

1. Create a test file alongside the code file, using the pattern `*.test.ts`.
2. Write tests using the project's (unknown) testing framework.
3. Run the test suite to ensure all tests pass.

#### Example Test File
```typescript
// dataFetcher.test.ts
import { fetchData } from './dataFetcher';

describe('fetchData', () => {
  it('should return expected data', () => {
    // test implementation
  });
});
```

## Testing Patterns

- Test files use the pattern `*.test.ts`.
- Place test files next to the files they test.
- Testing framework is not specified; follow standard TypeScript testing practices.
- Example test file:
  ```typescript
  // exampleFunction.test.ts
  import { exampleFunction } from './exampleFunction';

  describe('exampleFunction', () => {
    it('should behave as expected', () => {
      // test logic here
    });
  });
  ```

## Commands
| Command     | Purpose                                    |
|-------------|--------------------------------------------|
| /run-tests  | Run all test files matching `*.test.ts`    |
```
