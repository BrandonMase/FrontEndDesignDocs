# Nullish Coalescing Operator (`??`)

This documentation provides an in-depth exploration of the [nullish coalescing operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing) (`??`) in JavaScript. The nullish coalescing operator is a powerful addition to the language, offering a concise and expressive way to handle default values for variables that may be `null` or `undefined`.

## Key Concepts

### 1. **Definition of Nullish Coalescing Operator:**
   - **Definition:** The nullish coalescing operator (`??`) is a binary operator that returns the right-hand operand when the left-hand operand is `null` or `undefined`. Unlike the logical OR operator (`||`), it does not consider falsy values such as `0` or an empty string as triggering the default value.

   ```javascript
   // Nullish Coalescing Operator
   const RESULT = someValue ?? defaultValue;
   ```

### 2. **Distinguishing Nullish from Falsy:**
   - **Advantage:** The nullish coalescing operator specifically checks for `null` or `undefined`, making it suitable for scenarios where falsy values are considered valid data and should not trigger the default value.

   ```javascript
   // Example with Falsy Value (Logical OR)
   const VALUE = 0;
   const RESULT = value || defaultValue; // Incorrect if 0 is a valid value

   // Nullish Coalescing Operator (Preferred)
   const RESULT = value ?? defaultValue; // Correct, considering 0 as a valid value
   ```

### 3. **Use Cases for Nullish Coalescing:**
   - **Advantage:** Nullish coalescing is particularly useful for providing default values when dealing with variables that might be explicitly set to `null` or `undefined`.

   ```javascript
   // Using Nullish Coalescing for Default Value
   const USERNAME = inputUsername ?? 'Guest';
   ```

### 4. **Chaining Nullish Coalescing:**
   - **Advantage:** Nullish coalescing can be chained to provide fallback values for multiple variables in a concise and readable manner.

   ```javascript
   // Chaining Nullish Coalescing
   const RESULT = value1 ?? value2 ?? value3 ?? defaultValue;
   ```

## Best Practices

### 1. **Prefer Nullish Coalescing for Defaults:**
   - **Recommendation:** When setting default values for variables, prefer using the nullish coalescing operator over the logical OR operator to ensure that only `null` or `undefined` trigger the default.

   ```javascript
   // Good: Using Nullish Coalescing for Default Value
   const USERNAME = inputUsername ?? 'Guest';
   ```

### 2. **Understand the Distinction from Logical OR:**
   - **Recommendation:** Be aware of the distinction between the nullish coalescing operator and the logical OR operator. Understand when to use each based on the specific requirements of the code.

   ```javascript
   // Logical OR (Considered Incorrect in Some Cases)
   const USERNAME = inputUsername || 'Guest';

   // Nullish Coalescing (Preferred)
   const USERNAME = inputUsername ?? 'Guest';
   ```

### 3. **Combine with Optional Chaining:**
   - **Best Practice:** Combine nullish coalescing with optional chaining (`?.`) when dealing with nested properties to gracefully handle scenarios where intermediate properties might be `null` or `undefined`.

   ```javascript
   // Combining Nullish Coalescing with Optional Chaining
   const RESULT = object?.property1?.property2 ?? defaultValue;
   ```

## Conclusion

The nullish coalescing operator (`??`) in JavaScript provides a concise and effective way to handle default values for variables that may be `null` or `undefined`. By distinguishing nullish values from falsy values, it ensures a more precise approach to setting defaults in various scenarios. Developers are encouraged to leverage the nullish coalescing operator for cleaner and more robust code, especially when dealing with variables that may explicitly be set to `null` or `undefined`. Understanding its nuances and combining it with optional chaining leads to more expressive and resilient code in modern JavaScript applications.