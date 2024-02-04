## Prefer `let` and `const` over `var`

This outlines the advantages of using `let` and `const` declarations over the legacy var keyword in JavaScript. The introduction of `let` and `const` in ECMAScript 6 (ES6) provides developers with more predictable and block-scoped variable declarations, addressing several issues associated with the use of `var`.

### Function-scoped vs block-scoped variables

#### Function-scoped variables (`var`)
Variables declared using the `var` keyword are function-scoped. Function-scoped variables are accessible throughout the entire function in which they are defined.

```ts
const exampleFunction = () => {
    if (true) {
        var functionScopedVar = 'I am function-scoped';
    }

    console.log(functionScopedVar); // Accessible here
}
```

**Implications**
* Variables are [hoisted](https://www.w3schools.com/js/js_hoisting.asp) to the top of their containing function, potentially leading to unexpected behavior.
* Limited in terms of encapsulation, making it challenging to create variables with a scope limited to specific blocks.

#### Block-scoped variables (`let` & `const`)
Variables declared using `let` and `const` are block-scoped.
Block-scoped variables are confined to the block in which they are defined, including statements like if, for, and while.

```ts
const exampleFunction = () => {
    if (true) {
        let blockScopedVar = 'I am block-scoped';
        const CONSTANT_VAR = 'I am also block-scoped';
    }

    console.log(blockScopedVar); // ReferenceError: blockScopedVar is not defined
    console.log(constantVar); // ReferenceError: constantVar is not defined
}

```

### Advantages of Block Scoping

**Predictable Hoisting**

Block-scoped variables exhibit more predictable hoisting behavior compared to function-scoped variables, leading to clearer code semantics.

**Enhanced Encapsulation**

Block-scoping allows developers to encapsulate variables within specific blocks, promoting better code organization and reducing the risk of unintended variable access.

**Temporal Dead Zone (TDZ)**

Block-scoped variables are subject to the [Temporal Dead Zone (TDZ)](https://www.freecodecamp.org/news/what-is-the-temporal-dead-zone/), providing clear error messages when trying to access variables before their declaration.

**Improved Code Maintainability**

Block-scoping contributes to better code maintainability by limiting the scope of variables to the relevant block, making it easier to reason about the code.

While function-scoped variables using `var` have been a traditional part of JavaScript, the introduction of block-scoped variables with `let` and `const` in ES6 significantly improves code predictability and maintainability. Adopting block-scoping is recommended for modern JavaScript development to leverage its advantages and align with best practices.

### Best Practices

**Use `const` for Constants**

Prefer using `const` for values that should not be reassigned, promoting a more declarative and immutable coding style. See more about the usage of constants [here](../README.md#variables).

**Prefer `let` for Mutable Variables**

Use `let` for variables that need to be reassigned, providing flexibility while still benefiting from block scoping.

**Avoid Using `var`**

In modern JavaScript development, avoid using `var` unless working with legacy code. Opt for `let` and `const` for improved code quality and maintainability.