# Why Use Angular?

Now that you know what Angular is, the next question is:

> **Why would you use Angular instead of just JavaScript?**

---

## 🧩 When You Might Not Need Angular

For **basic** or **trivial** web applications, a full framework like Angular may be overkill. In such cases, plain **Vanilla JavaScript** might suffice.

However, as your app becomes **larger** and more **interactive**, Angular starts to **shine**.

---

## 🌟 Benefits of Using Angular

Angular simplifies the process of building **complex**, **highly interactive web user interfaces** through a set of **features**, **concepts**, and **rules**. The four core benefits are:

---

### 1. 🧾 Declarative Code (vs Imperative)

**Vanilla JavaScript** requires:
- Writing **step-by-step** instructions.
- Manually interacting with the **DOM**.
- Handling logic and UI updates explicitly.

**Angular**, on the other hand, allows:
- Writing **declarative code**, where:
  - You define **what the UI should look like** in various states.
  - Angular handles the **how** of updating the DOM.
- Markup enhanced with Angular-specific syntax.

📝 **Example**: Instead of manually checking a condition and updating the DOM, you declare the UI state in HTML using Angular directives like `*ngIf`, `*ngFor`, etc.

---

### 2. 🧱 Component-Based Architecture

Angular embraces the **Component** concept:
- A component is a combination of:
  - **HTML (Template)**
  - **CSS (Styles)**
  - **TypeScript (Logic)**

**Benefits:**
- Separation of concerns
- Reusability of components
- Easier testing and maintenance
- **Team collaboration**: Different team members can work on different components independently.

---

### 3. 🧠 Embraces Object-Oriented Programming Principles

Angular supports some **OOP concepts** such as:
- **Classes**
- **Encapsulation**
- **Dependency Injection**

🔍 **Dependency Injection** is a powerful pattern that:
- Helps with modularity
- Simplifies testing
- Allows for loose coupling between services and components

---

### 4. ⌨️ TypeScript Support

Angular uses **TypeScript** instead of JavaScript.

#### What is TypeScript?
> TypeScript = JavaScript + Strong Typing

**Advantages:**
- Early detection of errors
- Better tooling (autocomplete, refactoring, type hints)
- More robust and maintainable code
- Enforces better coding practices

🛑 Example of TypeScript catching issues:
```ts
function greet(name: string) {
  console.log("Hello, " + name);
}

greet(42); // ❌ Error: Argument of type 'number' is not assignable to parameter of type 'string'.
