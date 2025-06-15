
# 🧱 Building the Header Component

Now that we understand how Angular content ends up on the screen  
and how the `AppComponent` is loaded, it's time to start working on the **demo application**.

We'll learn more about Angular by **building components**,  
starting with the **Header component**.

---

## 🔧 Analyzing the UI

Looking at the final demo application, we can break the UI into multiple components:

- **Header** at the top
- **Sidebar** with elements (each can be a separate component)
- **Main content area** on the right
- **Dialog box** for "Add Task" – also a potential component

> 🧩 Angular is all about building reusable building blocks (components)  
> and composing them together to form the complete user interface.

---

## 🛠️ Creating a New Component

We already have one component — `AppComponent`.  
This component is built using **three separate files**, and that’s the standard approach in Angular.

To create a new component, such as the **Header**, we typically:

- Create a file like: `header.component.ts`
- Optionally follow the **new Angular 20 pattern**: `header.ts`
- The name doesn’t affect functionality — it's purely **conventional**

### 📄 Naming Convention

Traditional pattern:

```
<component-name>.component.ts
```

New Angular 20 recommendation:

```
<component-name>.ts
```

> 📌 Both are valid. Choose the one that fits your project or team conventions.

---

## ✍️ Creating the Component Class

To define the `HeaderComponent`, we:

1. Create the file: `header.component.ts`
2. Inside the file, define the component class:

```ts
export class HeaderComponent {
  // Empty for now
}
```

- The class **must be exported** so it can be imported elsewhere
- Naming is flexible but conventionally:
  - Starts with what the component does (`Header`)
  - Ends with `Component` to clarify it's a component

---

## 🧩 Adding the Decorator

Angular uses **decorators** to tell Angular how to treat a class.

### Steps:

1. Import the `Component` decorator:

```ts
import { Component } from '@angular/core';
```

2. Use the decorator above the class:

```ts
@Component({
  selector: 'app-header',
  templateUrl: './header.component.html',
  styleUrls: ['./header.component.css']
})
export class HeaderComponent {
  // Component logic here
}
```

- `selector`: the HTML tag you’ll use to insert this component
- `templateUrl`: path to the HTML file for this component
- `styleUrls`: path to the CSS file (optional)

> This is the exact pattern we’ll follow to build all components  
> in the Angular application.

---

✅ With that, we’re ready to start building the `HeaderComponent`  
as the **first building block** of our demo app!
