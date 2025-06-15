
# 📚 [Optional] JavaScript Refresher: Classes, Properties & More

Angular makes heavy use of **classes** — a feature supported by vanilla JavaScript  
and **extended by TypeScript** (which adds extra features, as you'll see).

---

## 🧱 What is a Class?

A **class** is essentially a **blueprint for objects**.  
Any properties and methods defined in the class will exist on all objects created from it.

### Example in Vanilla JavaScript:

```js
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log('Hi, I am ' + this.name);
  }
}
```

### Creating Instances:

```js
const person1 = new Person('Max', 35);
const person2 = new Person('Anna', 32);
```

### Using Properties and Methods:

```js
console.log(person1.age); // 35
person2.greet(); // Hi, I am Anna
```

---

## 💡 Classes in Angular

When using Angular, you’ll often define **classes that you never instantiate manually**.

For example:

```ts
@Component({})
class SomeComponent {}
```

> Components are defined as **classes**,  
> but Angular is responsible for **instantiating** them —  
> you never call `new SomeComponent()` yourself.

---

## ✨ TypeScript Enhancements

Since Angular uses **TypeScript**, you get extra features like:

### 🔹 Decorators

Decorators like `@Component` are used to add **metadata & configuration** to classes.

```ts
@Component({
  selector: 'app-example',
  templateUrl: './example.component.html'
})
class ExampleComponent {}
```

### 🔹 Access Modifiers

You can control access to class members:

- `public`: accessible from anywhere (default)
- `private`: accessible only within the class
- `protected`: accessible within the class and subclasses

```ts
class Car {
  private engine: string;

  constructor(engine: string) {
    this.engine = engine;
  }
}
```

---

## 📘 Further Learning

You can learn more about:

- [JavaScript Classes (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [TypeScript Classes](https://www.typescriptlang.org/docs/handbook/classes.html)
- [Access Modifiers in TypeScript](https://www.typescriptlang.org/docs/handbook/2/classes.html#member-visibility)

---

## ✅ Summary

- Classes are **blueprints for objects**
- Angular defines most building blocks as **classes**
- TypeScript adds powerful enhancements (decorators, access modifiers)
- You’ll see classes in action **throughout the course**

> No need to dive too deep now — you’ll learn by doing!
