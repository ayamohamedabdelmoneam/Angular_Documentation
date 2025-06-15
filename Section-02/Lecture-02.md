
# 🔄 How Angular Renders Content to the Screen

So how does the content actually end up on the screen?

In the previous section, we mentioned that the `index.html` file  
inside the `src/` folder is the one loaded by the browser  
when a visitor opens your Angular website.

But if you inspect that file, you’ll notice it's **almost empty**.

It contains just:

```html
<body>
  <app-root></app-root>
</body>
```

> 🧩 `app-root` is not a standard HTML tag.  
> The browser on its own doesn’t recognize it.

---

## 💡 This Is Where Angular Comes In

When the browser loads the app, it **executes the code** in `main.ts`,  
which is located in `src/main.ts`.

Surprisingly, the `index.html` file doesn't contain any `<script>` tags.  
So how is the code loaded?

### ✅ Angular CLI to the Rescue

When you run:

```bash
npm start
```

It executes `ng serve` under the hood, and Angular CLI:

- Compiles the TypeScript code into JavaScript
- Injects the generated `<script>` tags into the HTML **automatically**

So, the `main.ts` file gets executed when the browser loads the site,  
but as **compiled JavaScript** (because browsers can’t run `.ts` files directly).

---

## 🚀 Bootstrapping the App

In `main.ts`, the following function is called:

```ts
bootstrapApplication(AppComponent)
```

- This `bootstrapApplication` function is provided by Angular.
- It **needs an Angular Component** to start the app.
- In our case, we provide it with the `AppComponent`.

```ts
import { AppComponent } from './app/app.component';
```

This tells Angular to **load and render** the `AppComponent`.

---

## 🧱 Understanding AppComponent

Inside `app/app.component.ts`, we find:

```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  // Component logic here
}
```

### 🏷️ `@Component` Decorator

- This is a **TypeScript decorator** that adds metadata to the class.
- It turns the `AppComponent` class into a **real Angular Component**.
- It comes from the Angular framework:

```ts
import { Component } from '@angular/core';
```

---

## 📌 Key Properties of the Component

### 🔹 `selector`

- This tells Angular:  
  _“Replace every `<app-root>` in the HTML with this component’s template.”_

### 🔹 `templateUrl`

- Specifies the file where the **HTML markup** for this component is written.  
  In this case: `app.component.html`.

### 🔹 `styleUrls`

- Contains **CSS styles** that apply **only to this component**,  
  ensuring styles don’t leak or clash.

---

## 🧠 The Rendering Flow in Summary

1. Browser loads `index.html`
2. Angular CLI injects the necessary JS files
3. The `main.ts` file is executed
4. `AppComponent` is passed to `bootstrapApplication`
5. Angular looks for the tag `<app-root>` (defined in `selector`)
6. Angular replaces `<app-root>` with the HTML from `app.component.html`
7. Styles from `app.component.css` are applied
8. You see the content (title, subtitle, image, etc.) **on screen**

---

This is how Angular **takes control** and renders dynamic content  
from components — by replacing custom tags with your component templates.

It’s the foundation of every Angular app. 💡
