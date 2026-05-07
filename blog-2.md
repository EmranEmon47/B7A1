# Four Pillars of OOP in TypeScript

## Introduction

OOP (Object-Oriented Programming) helps organize code in large projects.  
The four main pillars of OOP are:

- Inheritance
- Polymorphism
- Abstraction
- Encapsulation

These concepts help reduce complexity and make code easier to manage.

---

## 1. Inheritance

Inheritance allows one class to use properties and methods from another class.

```ts
class Animal {
  sound() {
    console.log("Animal sound");
  }
}

class Dog extends Animal {}

const dog = new Dog();
dog.sound();
```

This reduces duplicate code and improves reusability.

---

## 2. Polymorphism

Polymorphism means the same method can behave differently.

```ts
class Animal {
  sound() {
    console.log("Animal sound");
  }
}

class Cat extends Animal {
  sound() {
    console.log("Meow");
  }
}
```

This makes code flexible and easier to extend.

---

## 3. Abstraction

Abstraction hides unnecessary details and shows only important parts.

```ts
abstract class Vehicle {
  abstract start(): void;
}

class Car extends Vehicle {
  start() {
    console.log("Car started");
  }
}
```

This keeps the system simple and organized.

---

## 4. Encapsulation

Encapsulation protects data from direct access.

```ts
class User {
  private password = "1234";

  getPassword() {
    return this.password;
  }
}
```

This improves security and prevents unwanted changes.

---

## Conclusion

The four pillars of OOP help developers:

- Reuse code
- Keep projects organized
- Reduce complexity
- Improve maintainability

That is why OOP is very useful in large TypeScript projects.
