# Functional Programming Reflection – Cameron Long, Jenny LaFlair, Julian Davis, Kaylie Marshall

## Will your custom language support functional features (e.g., pure functions, immutability)?
Yes, our custom language will support selected functional programming features, specifically **pure functions** and **immutability**. 

- **Pure functions** will ensure that functions always produce the same output for the same input and do not cause side effects. This improves predictability and simplifies debugging.
- **Immutability** will prevent variables from being modified after assignment, reducing unintended state changes and increasing program safety.

These features will enhance **code clarity**, **maintainability**, and **reusability**, while still allowing integration with imperative constructs for flexibility.

---

## What challenges exist in implementing functional concepts?
Implementing functional programming features introduces several challenges:

- **Performance overhead**: Recursion can lead to increased memory usage due to call stacks, especially without tail-call optimization.
- **Learning curve**: Developers familiar with imperative or object-oriented programming may find functional concepts harder to understand.
- **Syntax complexity**: Designing clean and intuitive syntax for higher-order functions and immutability can be difficult.
- **Debugging difficulty**: While pure functions simplify logic, debugging recursive or heavily abstracted code can be harder.
- **Implemation complexity**:  Supporting immutability requires careful memory management and may impact performance.
  
Despite these challenges, incorporating functional features provides strong benefits in reliability and code quality.

---

## Give an example of a problem that could benefit from recursion or higher-order functions


```pseudo
A classic example is calculating the factorial of a number using recursion:
function factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

An example of a higher-order function is applying a function to each element in a list:
function map(func, list):
    result = []
    for item in list:
        result.append(func(item))
    return result

function square(x):
    return x * x

map(square, [1, 2, 3, 4])  // returns [1, 4, 9, 16]
