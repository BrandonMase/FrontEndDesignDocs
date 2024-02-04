# Avoid Negative Conditionals

This highlights the best practices and considerations associated with avoiding negative conditionals in software development. It discusses the benefits of positive conditionals, provides examples, and outlines guidelines to improve code readability and maintainability.

## Key Concepts

### 1. **Definition:**
   - **Negative Conditionals:** Refers to conditional statements or expressions that use negation (e.g., `!==`, `!`) to check for the absence of a certain condition.

### 2. **Benefits of Positive Conditionals:**
   - **Readability:**
     - **Advantage:** Positive conditionals, where the emphasis is on the presence of a condition, often result in more readable and natural language expressions.

   - **Simpler Logic:**
     - **Advantage:** Positive conditionals typically lead to simpler and more straightforward logic, making it easier for developers to understand the intended behavior.

### 3. **Examples:**

#### Negative Conditional:

```javascript
if (error !== null) {
  // Handle error case
} else {
  // Process successful scenario
}
```

#### Positive Conditional (Preferred):

```javascript
if (error === null) {
  // Process successful scenario
} else {
  // Handle error case
}
```

In the positive conditional example, the emphasis is on the presence of a successful scenario, leading to more straightforward logic.

### 4. **Best Practices:**
   - **Use Positive Language:**
     - **Guideline:** Formulate conditionals using positive language that emphasizes the presence of a condition rather than its absence. This often leads to clearer and more intuitive code.

   - **Simplify Logic:**
     - **Guideline:** When possible, express conditions directly without negations. This simplifies logic and reduces cognitive load for developers reading the code.

   - **Avoid Double Negations:**
     - **Guideline:** Avoid double negations (`!!`) in conditionals, as they can add unnecessary complexity and decrease code readability.

### 5. **Considerations:**
   - **Refactoring Existing Code:**
     - **Consideration:** When refactoring existing code, assess whether converting negative conditionals to positive ones improves readability without introducing unintended side effects.


### Example: Positive Conditionals for Readability

```javascript
// Negative Conditional
const processResult = (data: Array<any>) => {
  if (data !== undefined && data !== null && data.length !== 0) {
    // Process data when it's not undefined, not null, and not an empty array
    processData(data);
  } else {
    // Handle the case when data is undefined, null, or an empty array
    handleEmptyData();
  }
}
```

In this example, the negative conditional checks for the absence of a condition, making the logic less intuitive. Now, let's refactor it using positive conditionals:

```javascript
// Positive Conditional (Preferred)
const processResult = (data: Array<any>) => {
  const DOES_DATA_EXIST = Array.isArray(data) && data.length > 0;

  if (DOES_DATA_EXIST) {
    // Process data when it's an array with at least one element
    processData(data);
  } else {
    // Handle the case when data is not an array or is an empty array
    handleEmptyData();
  }
}
```

In the refactored version, positive conditionals are used, making the logic more straightforward. The emphasis is on the presence of a non-empty array, which enhances readability and reduces the need for multiple negation checks. This approach results in cleaner and more intuitive code.

## When to break the rules

While positive conditionals are generally encouraged for improved readability, there are situations where breaking this rule and using negative conditionals can lead to simplified and more concise logic.

### 1. **Scenario Justification:**
   - **Simplified Logic:**
     - **Advantage:** Negative conditionals can be employed when only the absence of a condition needs to be considered, leading to more straightforward and concise logic.

### 2. **Example:**

```typescript
// Using Negative Conditional for Simplified Logic
const addUserToDatabase = (user: User) => {
  const DOES_USER_EXIST = database.getUser(user.id);

  if (!DOES_USER_EXIST) {
    // Add the user only if it doesn't already exist in the database
    database.addUser(user);
  }
};
```

In this example, the negative conditional `!DOES_USER_EXIST` is used to check if a user does not exist in the database. Since there is no additional logic for the case when the user does exist, a negative conditional simplifies the code.

## Conclusion

Avoiding negative conditionals in favor of positive ones contributes to code readability and simplifies logical expressions. By emphasizing the presence of conditions rather than their absence, developers can create more intuitive and straightforward code. Consistent use of positive conditionals, combined with contextual appropriateness, enhances the overall readability and maintainability of the codebase.