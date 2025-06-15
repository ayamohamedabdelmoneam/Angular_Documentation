
# 🧱 Defining the Header Component in Angular

Now that we've started creating the `HeaderComponent`,  
we need to configure it properly using Angular’s `@Component` decorator.

---

## ⚙️ Adding the Component Configuration

Just like with `AppComponent`, we use the `@Component()` decorator  
and pass a configuration object.

### 🏷️ Selector

Defines the custom HTML tag this component will replace.

```ts
selector: 'app-header'
```

> ✅ Convention: use **two words** separated by a dash (e.g., `app-header`)  
> to avoid name collisions with built-in HTML elements like `<header>`.  
> `app` is a common prefix, but you can use any name.

---

## 🧾 Defining the Template

There are **two ways** to define the HTML template for a component:

### 1. Inline Template (Not Recommended for Larger UIs)

```ts
template: '<h1>Easy Task</h1>'
```

Use only for **very short templates** (1–3 lines).

---

### 2. External Template (Recommended)

```ts
templateUrl: './header.component.html'
```

- Store your markup in a separate `.html` file
- Follows same base name as the `.ts` file: `header.component.html`
- Keep file in the **same folder** for easy reference

### Example Template (in `header.component.html`):

```html
<header>
  <h1>Easy Task</h1>
</header>
```

---

## 🎨 Styles (Optional)

You can also define `styleUrls` to include component-specific styles:

```ts
styleUrls: ['./header.component.css']
```

---

## 🧷 Standalone Component

Newer Angular versions support **Standalone Components**:

```ts
standalone: true
```

### When to Use?

- Angular **v19 and above**: standalone is `true` by default
- Angular **v18 or lower**: must **explicitly set** `standalone: true`

### Why Use Standalone?

- Easier to manage and reuse
- No need to declare in NgModules
- Recommended by Angular for modern development

---

## ✅ Complete Component Setup

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-header',
  templateUrl: './header.component.html',
  standalone: true
})
export class HeaderComponent {
  // Logic here (empty for now)
}
```

---

## 📌 Summary

- Define a selector using kebab-case with a prefix (`app-header`)
- Use external HTML for better structure
- Mark the component as `standalone: true` for modern Angular
- Now you're ready to **use this component in your UI**

In the next step, we’ll see **how to use this component** in the application.
