# Choose `UPPER_SNAKE_CASE` for Constants
This outlines the rationale and best practices for using `UPPER_SNAKE_CASE` when naming constants in JavaScript. Adopting this naming convention for constants provides clarity, improves code readability, and enhances maintainability in large codebases.

## Key Concepts
**Conventional Significance**

**Definition:** ``UPPER_SNAKE_CASE`` refers to writing constant names in all capital letters with underscores (_) separating words.

**Significance:** This naming convention signals that a variable is a constant and distinguishes it from variables that can be reassigned.

## Visibility and Readability
**Advantage:** Constants in `UPPER_SNAKE_CASE` are immediately recognizable and stand out in code, improving visibility and making it clear that their values should not be changed.

## Consistency Across Codebase
**Best Practice:** Adopting a consistent naming convention promotes uniformity and reduces cognitive load for developers working on a shared codebase.

**Constant Naming Convention**
```ts
const MAX_LENGTH = 100;
const API_KEY = 'xyz123';
const PI_VALUE = 3.14;
```

**Non-Constant Naming Convention**
```ts
let maxLength = 100;  // Not immediately recognizable as a constant
const apiKey = 'xyz123';  // Unclear indication of a constant
const PiValue = 3.14;  // Inconsistent and less readable
```

## Best Practices
**Use `UPPER_SNAKE_CASE` for Constants**

Always use `UPPER_SNAKE_CASE` when naming constants to provide a visual cue to developers that these values should remain constant.

**Avoid Reassignment**

Constants, by definition, should not be reassigned. Following `UPPER_SNAKE_CASE` helps reinforce this rule and prevents accidental reassignment.

**Differentiate Constants from Variables**

Consistent use of `UPPER_SNAKE_CASE` differentiates constants from variables, making the codebase more understandable and maintainable.

Adopting the `UPPER_SNAKE_CASE` naming convention for constants in JavaScript is a best practice that contributes to code clarity, readability, and maintainability. By providing a visual cue that a variable is a constant and adhering to community standards, developers can create more robust and easily understandable codebases. Consistency in naming conventions enhances collaboration and reduces the likelihood of errors related to constant reassignment.