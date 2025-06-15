# 🧱 Why We Need an Angular Project Setup

Now, in order to get started writing Angular code and learning Angular, we need a proper Angular project where we can write, run, and test our code.

You **cannot** just create an empty folder and add an `index.html` or `app.js` file like in vanilla JavaScript. That’s because Angular uses:

- Nonstandard HTML syntax  
- TypeScript (which must be compiled to JavaScript)  
- Additional tools for building, optimizing, and compiling code

---

## 🛠 Why Angular Needs a Project Setup

Angular relies on features that **don't work in the browser out of the box**, such as:

- Template syntax like `*ngIf`, `[(ngModel)]`, etc.  
- TypeScript instead of plain JavaScript  
- Module and component architecture

To handle this, Angular projects need **build tools** that:
- Compile TypeScript → JavaScript
- Optimize and bundle the code
- Serve it via a dev server

---

## 🧰 Angular CLI (Command-Line Interface)

To make setup easier, the Angular team provides the **Angular CLI**, a command-line tool that:
- Generates Angular projects  
- Starts a development server  
- Builds the app for production  
- Compiles and optimizes code

You’ll use the Angular CLI all the time, even though most of its work happens behind the scenes.

---

## 🌐 Installing Prerequisites

Before installing the Angular CLI, you need another tool first:

### ✅ Install Node.js + NPM

[Node.js](https://nodejs.org) is a JavaScript runtime used by the CLI. You won’t write Node code, but Angular CLI depends on it.

> 🔹 Download the **LTS version** from [https://nodejs.org](https://nodejs.org) and follow the setup wizard (macOS/Windows/Linux supported).

Once installed, you’ll have:
- Node.js runtime  
- NPM (Node Package Manager)

---

### 📦 Install Angular CLI

Use your system terminal or command prompt:

```bash
npm install -g @angular/cli
# 🚀 Getting Started with Angular: Project Setup Guide

## 📌 Why We Need a Project Setup

To start writing Angular code, we need a **proper Angular project structure**. Unlike plain HTML/JS apps, Angular relies on:
- Custom syntax in HTML templates
- TypeScript (which must be compiled to JavaScript)
- Build tools to process and optimize your code

Because of this, we **cannot just use an empty folder with an HTML file**. We need tooling that transforms Angular code into browser-compatible code.

---

## 💪 What Tools Do We Need?

### 1. **Node.js + NPM**
Angular CLI relies on [Node.js](https://nodejs.org/) and **npm**:
- Node.js is a JavaScript runtime (not required for Angular itself, but required for tooling).
- NPM is a package manager that comes with Node.js.

> ✅ Download the **LTS version** of Node.js from [nodejs.org](https://nodejs.org), and install it by following the setup wizard.

---

### 2. **Angular CLI**

Angular CLI is a command-line tool that:
- Creates Angular projects
- Compiles TypeScript → JavaScript
- Runs the dev server
- Builds the app for production
- Performs code optimization

#### 🔽 Install it globally via terminal:
```bash
npm install -g @angular/cli
```

> 💡 On **macOS/Linux**, you may need to prefix with `sudo`:
```bash
sudo npm install -g @angular/cli
```

---

## 🚧 Creating Your First Angular Project

Once the CLI is installed:

### 1. Open your terminal and move to your desired folder:
```bash
cd path/to/your/folder
```

### 2. Run the following to create a new project:
```bash
ng new first-angular-app
```

### 3. Answer the prompts:
Depending on the CLI version, you may see questions like:

| Prompt | Recommended Answer |
|--------|--------------------|
| Zoneless Angular? | `No` (for now) |
| Stylesheet format | `CSS` (or `SCSS`, your choice) |
| Enable SSR/SSG? | `No` |

> ✅ You can always hit `Enter` to accept the defaults.

> 🔒 **Project name tips:**
- Use lowercase only
- No spaces
- Use `-` between words (e.g. `my-angular-app`)

---

## ✅ After Setup

After setup completes:

```bash
cd first-angular-app
ng serve
```

Then open your browser and go to:

```
http://localhost:4200
```

You’ll see the default Angular welcome page — you're now ready to build!

---

## 🧑‍💻 Recommended Code Editor

To work on that project and write your Angular code, you’ll need a code editor.

### 🎯 Recommended: Visual Studio Code

If you don’t have a clear preference, Visual Studio Code is:
- Free
- Cross-platform
- Highly extensible

> Download it from: [https://code.visualstudio.com](https://code.visualstudio.com)

Once installed:
- Open **Visual Studio Code**
- Use **File > Open Folder** to open your Angular project folder you created with `ng new`

You should now see a list of files and folders in the **Explorer** pane. These may change over time, but we’ll cover what they mean in the next section. They are automatically generated because Angular requires configuration and compilation setup.

---

## 🔌 Recommended VS Code Extensions for Angular

Before diving into the code or testing it locally:

1. Open the **Extensions** panel in VS Code
2. Search for and install:

### 🔹 Angular Language Service
- Better Angular code support
- Code completion
- Syntax highlighting
- Error checking

### 🔹 Angular Essentials (optional)
- Bundles a few useful Angular-related extensions

Once installed, you're fully ready to work with Angular in VS Code.

---

## 🚀 Run Your Angular Project in VS Code

To preview and test your Angular app locally:

1. Open **Terminal > New Terminal** from the VS Code menu
2. Make sure the terminal is inside your project folder
3. Run:
```bash
npm start
```

This starts a development server and watches your code for changes.

Open your browser and go to:
```
http://localhost:4200
```
You should see a default Angular starter page. It may look different over time, but this means everything works correctly.

> ⚙️ Keep the terminal open while working. The dev server auto-reloads your app as you make changes.

When done for the day:
- Stop the server with `Ctrl + C`
- Restart it anytime with:
```bash
npm start
```

---

## 💬 Next Steps
- Learn Angular syntax (components, modules, bindings, etc.)
- Explore CLI features (e.g., `ng generate`)
- Build and test your components

We’ll start that in the next section! 💡
