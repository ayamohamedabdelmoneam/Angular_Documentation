# Angular Essentials

In this section, we're going to dive into the **crucial Angular Essentials**,  
the core concepts every Angular developer must know —  
and we'll do so by **building a complete demo application** from the ground up.

---

## 🧱 What You'll Learn While Building the Demo App:

### 🔹 Project Structure  
- Understand how Angular projects are structured  
- Explore what the different files and folders do  

### 🔹 Components  
- Learn the concept of working with components  
- Understand how to break your UI into reusable pieces  

### 🔹 TypeScript & Declarative Code  
- Write Angular code using TypeScript  
- Learn how to write declarative templates  

### 🔹 Handling User Events  
- React to user events like `click`, `input`, etc.  
- Connect user interactions to application logic  

### 🔹 Dynamic User Interfaces  
- Learn how Angular renders and updates the UI  
- Build dynamic interfaces that change in response to data or events  

---

By the **end of this section**, you'll be able to:

✅ Build dynamic web applications on your own  
✅ Understand and use Angular’s most important features with confidence  
✅ Apply all of this knowledge while building a real-world **demo application**

---

Let’s get started and **bring Angular to life!**

# Getting Started with the Demo Project

To dive into all the **Angular essentials** and build our demo project,  
I've prepared a **starting Angular project**, and you’ll find a link to it attached.  
I highly recommend using it so we all start from the **same base**.

This project was created with the **Angular CLI**,  
so it includes essential configuration files and an `src` folder  
which contains additional folders and files.

---

## 🔍 Differences in CLI Versions

Depending on the **Angular CLI version** you're using,  
you might notice slight differences in the generated structure.

For example:

- Some versions may include a `public/` folder with a `favicon.ico`.
- In the provided starting project, the `favicon.ico` is inside the `src/` folder.

These are just minor differences.  
👉 **The Angular code you write remains the same**, regardless of such structural changes.

---

## 🗂 Project Overview

Let’s walk through the key files and folders.

### 📁 Root-Level Files

These are mostly **configuration files**:

- **TypeScript Configs** (`tsconfig.json`, etc.):  
  Controls how TypeScript is compiled into JavaScript.  
  > 💡 Don’t edit unless you know what you’re doing — the defaults work fine.

- **`package.json` & `package-lock.json`**:  
  Manage your project dependencies (like Angular packages).

- **`angular.json`**:  
  Configuration for Angular CLI tools.  
  Again, no need to modify it unless necessary.

- **`.editorconfig`**:  
  Contains formatting rules for the code editor.

- **`.gitignore`**:  
  Specifies which files Git should ignore if you’re using version control.

---

### 📁 `src/` Folder

This is the **main working directory** — where you'll build your app.

#### 📁 `app/`

- You’ll spend most of your time here.
- This is where you’ll write and organize your **components**.

#### 🔸 Component Naming

> Depending on Angular version:
> 
> - Older versions use `app.component.ts`
> - Newer Angular (v20+) might use `app.ts`

You can name your files however you like.  
Just know that `.component` is a convention and doesn’t affect Angular behavior.

---

### 📄 Other Important Files in `src/`

- **`styles.css`**: Global styles for the entire app.
- **`index.html`**: Main HTML file loaded by the browser.
- **`favicon.ico`**: The browser icon for the app.
- **`main.ts`**:  
  - The *entry point* of the application.
  - Contains the **first TypeScript code** executed when the app loads.

- **`assets/` folder**:  
  For storing static assets like images (e.g. logo, icons, etc.)

---

## 🚀 Installing Dependencies

After downloading the starter project:

1. Open your terminal or command prompt.
2. Navigate into the project folder.
3. Run the following command:

```bash
npm install
