# Object-Oriented Design Reflection – Cameron Long, Jenny LaFlair, Julian Davis, Kaylie Marshall

## Overview

Object-oriented programming (OOP) concepts play an important role in the design of our custom programming language because they help organize code into reusable, modular, and maintainable structures. While our language may not be fully object-oriented like Java or C++, we plan to incorporate selected OOP principles that improve readability and simplify program design.

## Which OOP features do you plan to include, modify, or exclude, and why?

### Include

- Classes and objects
- Methods
- Basic encapsulation
- Single inheritance
- Method overriding
  
### Modify

- Inheritance syntax will be simplified using the keyword inherits
- Access modifiers may only include public and private to reduce complexity

### Exclude

- Multiple inheritance
- Complex interfaces
- Operator overloading

These exclusions keep the language easier for beginners and reduce compiler complexity.

## What challenges did you encounter in modeling OOP concepts in language design?

One challenge is balancing power with simplicity. Full OOP systems can become difficult to learn and implement. Adding inheritance and polymorphism requires extra semantic rules, method lookup behavior, and memory handling.

Another challenge is deciding whether everything should be object-based. Some tasks are easier in procedural or functional styles, so our language may support mixed paradigms instead of forcing everything into classes.

## How OOP Concepts Apply to Our Custom Language

### Inheritance

Inheritance may be included in a simplified form so one class can reuse another class’s properties and methods. This reduces repeated code and supports logical hierarchies.

### Polymorphism

Polymorphism will allow the same method name to behave differently depending on the object type.

### Encapsulation

Encapsulation will allow data and methods to be grouped into a single structure, such as an object or module. This helps protect internal values from direct modification and encourages controlled interaction through public methods.

Example: Encapsulation, Inheritance, Polymorphism

```mlang
class BankAccount {
    private balance = 0

    method deposit(amount) {
        balance = balance + amount
    }

    method getBalance() {
        return balance
    }
}

```mlang
class Animal {
    method speak() {
        print("Sound")
    }
}

class Dog inherits Animal {
    method speak() {
        print("Bark")
    }
}

```mlang
pet = Dog()
pet.speak()   # Bark
