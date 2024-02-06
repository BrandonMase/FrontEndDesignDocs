# Front End Design Docs

The uppercased bolded key words (**MUST**, **SHOULD**, **SHOULD NOT**, etc.) have specific meaning as defined in [RFC2119](https://www.rfc-editor.org/rfc/rfc2119.html).

## Quick Rundown
- **MUST**: This word, or the terms **REQUIRED** or **SHALL**, mean that the
   definition is an absolute requirement of the specification.
- **MUST NOT**: This phrase, or the phrase **SHALL NOT**, mean that the
   definition is an absolute prohibition of the specification.
- **SHOULD**: This word, or the adjective **RECOMMENDED**, mean that there
   may exist valid reasons in particular circumstances to ignore a
   particular item, but the full implications must be understood and
   carefully weighed before choosing a different course. 
   - If a requirement has **SHOULD**, there **MUST** be example(s) in the documentation where ignoring the requirement is acceptable.
- **SHOULD NOT**: This phrase, or the phrase **NOT RECOMMENDED** mean that
   there may exist valid reasons in particular circumstances when the
   particular behavior is acceptable or even useful, but the full
   implications should be understood and the case carefully weighed
   before implementing any behavior described with this label. 
   - If a requirement has **SHOULD NOT**, there **MUST** be example(s) in the documentation where ignoring the requirement is acceptable.
-  **MAY** : This word, or the adjective **OPTIONAL**, mean that an item is
   truly optional.  One vendor may choose to include the item because a
   particular marketplace requires it or because the vendor feels that
   it enhances the product while another vendor may omit the same item.
   An implementation which does not include a particular option **MUST** be
   prepared to interoperate with another implementation which does
   include the option, though perhaps with reduced functionality. In the
   same vein an implementation which does include a particular option
   **MUST** be prepared to interoperate with another implementation which
   does not include the option (except, of course, for the feature the
   option provides.)

## Relative Terms
Sometimes, you may encounter a naming convention that uses angle brackets (`<>`) with a word in between, enclosed in code tags (e.g., `<method name>`). This convention serves to explain a **relative term** within the document. For instance, if we specify that a variable should be named with `<method name><API name>`, both the method name and API name are contextually relevant to what we are discussing. For example, you might have a variable named `getUserData`.

# Requirements
* **SHOULD** regularly remove unused code unless there is a reason for the code to be there. [Why?](./Javascript/Unused-Code.md)
* **MUST** use Strict Equality (`===`) over Loose Equality (`==`). [Why?](./Javascript/Strict-Equals.md)
## Interfaces/Types
  * **MUST** use `I` at the begining of `interfaces` and `T` at the beginning of `types`. [Why?](./Javascript/Interfaces/Interface-Naming.md)
## Variables
  * **MUST** choose variable names that are descriptive and convey the purpose of the variable. [Why?](./Javascript/Variables/Descriptive-Names.md)
  * `Boolean` variables **SHOULD** start with `is`,`has`,`did`,`does`, or `was`.
  * **MUST** use `let` and `const` over `var`. [Why?](./Javascript/Let-Over-Var.md)
  * **SHOULD NOT** use unneeded context in object keys. [Why?](./Javascript/Variables/Unneeded-Context-Object-Names.md)
  * **SHOULD** **NOT** use the `any` type. [Why?](./Javascript/Any-TS.md)
  * **SHOULD** use `enum` types for limited and well-defined options. [Why?](./Javascript/Enums.md)
  * **SHOULD** use destructuring over explict variable declarations. [Why?](./Javascript/Variables/Destructoring.md)
  * **SHOULD** use template literals over string concatenation. [Why?](./Javascript/Variables/Template-Literals.md)
  * **SHOULD** use the nullish coalescing operator for defaults. [Why?](./Javascript/Variables/Nullish.md)

  **Non-Constants**
  * **MUST** use `camelCase` for `let` variables.
  * **MUST** use `let` for mutable variables.

  **Constants**
  * **MUST** use `const` for immuatable variables.
  * **MUST** use `UPPER_SNAKE_CASE` for `const` variables. [Why?](./Javascript/Constants/Upper-Snake-Case.md)
  * **MUST** use `camelCase` for `const` functions.
  * **MUST** use `PascalCase` for `const` React components.
  * **MUST** use `Object.freeze` for constant pass-by-reference variables that need to be completely immutable. [Why?](./Javascript/Constants/Freezing.md)

## Functions
  * **MUST** use a verb-noun naming convention for functions. [Why?](./Javascript/Functions/Noun-Verb.md)
  * **SHOULD** use Arrow functions (ES6) over ES5 functions. [Why?](./Javascript/Functions/Arrow-Functions.md)
  * **MUST** explicitly type out parameters and returns where they can't be infered. [Why?](./Javascript/Functions/Explict-Parameter-Types.md)
  * **SHOULD** keep functions simple. Each function should be under 25 lines of functionality with a clear defined task. [Why?](./Javascript/Functions/Simple-Functions.md)
  * **MUST** use `<method name><API name>_API` naming convention for functions that call APIs. [Why?](./Javascript/Functions/API-Function-Naming.md)
  * Functions **SHOULD** be self-explanatory. [Why?](./Javascript/Functions/Self-Explain.md)
  * **SHOULD** use `async/await` over callbacks and `Promises`. [Why?](./Javascript/Functions/Prefer-Async.md)
  * Callers and Callees **SHOULD** be in close proximity to each other. [Why?](./Javascript/Functions/Proximity.md)
  * **SHOULD NOT** negative conditionals. [Why?](./Javascript/Functions/Negative-Conditionals.md)
  * **SHOULD** use documentation over comments. [Why?](./Javascript/Functions/Documentation.md)

  ## React
  * **SHOULD** seperate business logic and presentional components for larger components. [Why?](./Javascript/React/MVC.md)
  * **SHOULD** avoid inline styles. [Why?](./Javascript/React/Inline-Styles.md)
  * **MUST** use functional components over class components. [Why?](./Javascript/React/Functional-Components.md)
  * **SHOULD NOT** over optimize code before it's needed. [Why?](./Javascript/React/Premature-Optimization.md)
  * **MUST** use the `PascalCase` naming convention for React components. [Why?](./Javascript/React/Pascal-Case.md)
  * **MUST** use `const` for React components.
  * **MUST** name React component files `<component name>.component.tsx`.
  * **MUST** name React hook files `<hook name>.hook.tsx`
  * Components **MUST** always be a Arrow (ES6) function.
  * Component props **MUST** have the interface naming convertion of `I<component name>Props`.
