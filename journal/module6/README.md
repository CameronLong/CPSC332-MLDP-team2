# Type Systems and Memory Reflection – Cameron Long, Jenny LaFlair, Julian Davis, Kaylie Marshall

## Overview
In this activity, your team will reflect on how your custom programming language will handle **type systems** and **memory management**—two critical aspects that influence performance, safety, and correctness. You’ll decide whether your language will use a static or dynamic type system (and whether it will be strongly or weakly typed) and how it will manage memory, either through manual allocation (like C) or automatic management (like Java or Python). Your team will also include a simple visual model to illustrate how memory is structured or how your type system will work.

## Type System

Our custom programming language will use a **statically typed, strongly typed** system. Types will be checked at compile time to catch errors early and improve reliability. Strong typing ensures that operations are only performed on compatible data types, reducing unexpected behavior. To maintain usability, the language will support **type inference**, allowing developers to omit explicit type declarations when the type can be clearly determined by the compiler.

## Memory Management

The language will use **automatic memory management** through a garbage collection system to handle memory allocation and deallocation. This approach reduces the risk of common errors such as memory leaks and dangling pointers, improving overall safety and reliability. Additionally, the language will provide **optional low-level control** for advanced users, allowing manual memory management in performance-critical sections when needed. This hybrid approach balances safety with efficiency.
