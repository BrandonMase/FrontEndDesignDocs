# Front End Design Docs
* Regularly remove unused code unless there is a reason for the code to be there. [Why?](./Javascript/Unused-Code.md)
* Prefer Strict Equality (`===`) over Loose Equality (`==`). [Why?](./Javascript/Strict-Equals.md)
## Interfaces/Types
  * Use `I` at the begining of `interfaces` and `T` at the beginning of `types`. [Why?](./Javascript/Interfaces/Interface-Naming.md)
## Variables
  * Choose variable names that are descriptive and convey the purpose of the variable. [Why?](./Javascript/Variables/Descriptive-Names.md)
  * `Boolean` variables should start with `is`,`has`,`did`,`does`, or `was`.
  * Use `let` and `const` over `var`. [Why?](./Javascript/Let-Over-Var.md)
  * Avoid the use of `any` type. [Why?](./Javascript/Any-TS.md)
  * Use `enum` types for limited and well-defined options. [Why?](./Javascript/Enums.md)
  * Prefer destructuring over explict variable declarations. [Why?](./Javascript/Variables/Destructoring.md)
  * Prefer template literals over string concatenation. [Why?](./Javascript/Variables/Template-Literals.md)
  * Prefer the nullish coalescing operator for defaults. [Why?](./Javascript/Variables/Nullish.md)

  **Non-Constants**
  * Use `camelCase` for `let` variables.
  * Use `let` for mutable variables.

  **Constants**
  * Use `const` for immuatable variables.
  * Use `UPPER_SNAKE_CASE` for `const` variables. [Why?](./Javascript/Constants/Upper-Snake-Case.md)
  * Use `camelCase` for `const` functions/React components.
  * Use `Object.freeze` for constant pass-by-reference variables that need to be completely immutable. [Why?](./Javascript/Constants/Freezing.md)

## Functions
  * Use a verb-noun naming convention. [Why?](./Javascript/Functions/Noun-Verb.md)
  * Prefer Arrow functions (ES6) over ES5 functions. [Why?](./Javascript/Functions/Arrow-Functions.md)
  * Explicitly type out parameters and returns where they can't be infered. [Why?](./Javascript/Functions/Explict-Parameter-Types.md)
  * Keep functions simple. Each function should be under 25 lines of functionality with a clear defined task. [Why?](./Javascript/Functions/Simple-Functions.md)
  * Use `<method name><API name>_API` naming convention for functions that call APIs. [Why?](./Javascript/Functions/API-Function-Naming.md)
  * Functions should be self-explanatory. [Why?](./Javascript/Functions/Self-Explain.md)
  * Prefer `async/await` over callbacks and `Promises`. [Why?](./Javascript/Functions/Prefer-Async.md)
  * Callers and Callees should be in close proximity to each other. [Why?](./Javascript/Functions/Proximity.md)
  * Avoid negative conditionals. [Why?](./Javascript/Functions/Negative-Conditionals.md)
  * Documentation over comments. [Why?](./Javascript/Functions/Documentation.md)

  ## React
  * Prefer seperation of business logic and presentional layers for larger components. [Why?](./Javascript/React/MVC.md)
  * Avoid inline styles. [Why?](./Javascript/React/Inline-Styles.md)
  * Use functional components over class components. [Why?](./Javascript/React/Functional-Components.md)
  * Don't over optimize code before it's needed. [Why?](./Javascript/React/Premature-Optimization.md)