# Naming Convention for React Components: `PascalCase`

This documentation underscores the importance of consistently naming React components in `PascalCase`. This naming convention enhances code clarity, aligns with JavaScript class conventions, avoids collisions with HTML elements, and facilitates maintainability.

### 1. **Definitions**
   - **PascalCase** `PascalCase` involves starting each word in a compound name with an uppercase letter (e.g., `MyComponent`)

### 2. **Benefits**

   - **Consistency:** 
   Ensuring consistent use of `PascalCase` for React components promotes clarity and consistency within the codebase.

   - **JavaScript Class Convention:** 
   React components are essentially JavaScript classes. PascalCase` aligns with the common JavaScript naming convention for classes, reinforcing the component-as-class concept in React. 

   - **Avoiding Collisions with HTML Elements:** 
   React components are often rendered as HTML elements. `PascalCase` minimizes the risk of collisions with native HTML tags, ensuring that custom components are easily distinguishable from standard HTML elements.

   -  **Tooling and Linting Benefits:** 
   Any tools and linters enforce naming conventions. Adopting `PascalCase` enables early error detection through tools like ESLint, contributing to overall code quality and consistency.

   - **Readability and Maintainability:** 
   `PascalCase` improves code readability, aiding developers in quickly identifying components. This convention contributes to better maintainability and comprehension, especially when working collaboratively on a codebase.

   - **Consistent File Naming:** 
   Naming React component files in `PascalCase` ensures consistency between component names and file names (e.g., `MyComponent.component.tsx`). The filename becomes a reflection of the file's content, making it easier to locate and manage specific components.

### 3. **Drawbacks**
*N/A*
### 4. **Best Practices**
   - Name each React component with `PascalCase` eg. (`MyComponent`).

### 5. **When To Break The Standard**
*N/A*

### 6. **Examples**

### Bad
```tsx
const myComponent = (props: IMyComponentProps) => {
  //...
}

// some render somewhere.
<div>
  <myComponent>
</div>

```
In this example, the component is named in `camelCase`, causing ambiguity and making it less clear that it's a React component.

### Good
```tsx
const MyComponent = (props: IMyComponentProps) => {
  //...
}

// some render somewhere.
<div>
  <MyComponent>
</div>
```