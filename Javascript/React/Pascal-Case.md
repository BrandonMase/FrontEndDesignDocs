# React Components MUST Be Named in `PasalCase`

1. **Consistency and Clarity**:
   - `PascalCase` is a naming convention where each word in a compound name starts with an uppercase letter (e.g., `MyComponent`).
   - Using `PascalCase` consistently for React components ensures clarity and consistency throughout your codebase.
   - It distinguishes components from regular HTML elements (which use lowercase) and other variables.

2. **JavaScript Class Convention**:
   - React components are essentially JavaScript functions.
   - `PascalCase` aligns with the common JavaScript naming convention for classes.
   - When you create a component, you're essentially defining a class, so it makes sense to follow this convention.

3. **Avoiding Collisions with HTML Elements**:
   - React components are often rendered as HTML elements.
   - If you use lowercase names (e.g., `myComponent`), they might clash with existing HTML tags (e.g., `<myComponent>`).
   - PascalCase ensures that your custom components won't accidentally collide with native HTML elements.

4. **Tooling and Linting Benefits**:
   - Many tools and linters (such as ESLint) enforce naming conventions.
   - By using `PascalCase`, you'll receive warnings if you accidentally use incorrect casing for your components.
   - This helps catch errors early and maintain code quality.

5. **Readability and Maintainability**:
   - `PascalCase` makes your code more readable.
   - When someone else reads your code, they can immediately recognize that a capitalized name refers to a component.
   - It also aids in searching for components within your project.

6. **Consistent File Naming**:
   - When you create a new component file, naming it in `PascalCase` (e.g., `MyComponent.component.tsx`) ensures consistency.
   - The filename reflects the content of the file, making it easier to locate specific components.

## Example
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
This component is named in `camelCase`. When a developer is looking through the code, it isn't immedately clear whether this is a regular function or a React component.

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

## Conclusion
In summary, adopting `PascalCase` for React components enhances code clarity, prevents collisions, aligns with JavaScript conventions, and improves overall maintainability.
