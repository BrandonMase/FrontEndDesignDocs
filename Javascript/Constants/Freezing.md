# Preventing Mutation in Pass-by-Reference Variables
In JavaScript, objects and other pass-by-reference variables can be inadvertently mutated, leading to unexpected behavior. This documentation highlights the potential risks and introduces the use of Object.freeze to prevent unintended mutations in pass-by-reference variables, emphasizing the importance of maintaining immutability when necessary.

## Pass-by-Reference Variables
Objects, arrays, and functions are examples of pass-by-reference variables in JavaScript.
When these variables are assigned to another variable or passed as function arguments, the reference to the original variable is shared.

```ts
const ORIGINAL_OBJECT = { key: 'value' };
const REFERENCE_OBJECT = ORIGINAL_OBJECT;

REFERENCE_OBJECT.key = 'modified value';

console.log(ORIGINAL_OBJECT.key); // Outputs: 'modified value'
```

## Implications
Modifying the reference variable also affects the original variable, leading to unintended mutations.

## `Object.freeze` Method
[`Object.freeze`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/freeze) is a method in JavaScript that prevents modifications to an object, making it immutable.

```ts
const ORIGINAL_OBJECT = { key: 'value' };
const FROZEN_OBJECT = Object.freeze(ORIGINAL_OBJECT);

// Attempt to modify the frozen object
FROZEN_OBJECT.key = 'modified value';

console.log(ORIGINAL_OBJECT.key); // Outputs: 'value' (unchanged)
```

## Advantages
`Object.freeze` ensures that the object and its properties cannot be modified, providing a safeguard against unintended mutations.

## Limitations
`Object.freeze` is shallow, meaning it only freezes the top-level object and its immediate properties. Nested objects must be frozen separately for complete immutability.

## Best Practices
**Immutability for Critical Variables**

Identify pass-by-reference variables that should remain immutable and use `Object.freeze` to prevent unintentional mutations.

**Complete Freezing for Deep Objects**

When dealing with nested objects, ensure complete immutability by recursively applying `Object.freeze` to all nested objects.


Preventing mutation in pass-by-reference variables is crucial to maintaining code predictability and preventing unexpected side effects. By using `Object.freeze` selectively on objects that should remain immutable, developers can enhance the robustness of their code and reduce the risk of unintended modifications. It is important to apply freezing consistently and consider the depth of objects to ensure comprehensive immutability when necessary.