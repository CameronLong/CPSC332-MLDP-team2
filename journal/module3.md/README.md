# Imperative Programming Reflection – Cameron Long, Jenny LaFlair, Julian Davis, Kaylie Marshall

## What imperative constructs do you plan to include in your language?

Our language will include the main imperative programming constructs that make it easy to control program behavior step by step. These constructs include:

- Variable declarations and assignment
- Sequential statements
- Conditional statements such as `if`, `else if`, and `else`
- Looping structures such as `while` and `for`
- Functions with parameters and return values
- Basic input and output commands

These features are important because imperative languages focus on giving the computer a sequence of commands to execute in order. By including conditionals and loops, our language can make decisions and repeat actions when needed. Variables and functions also make the language more organized and practical for solving problems.

## How do those constructs manage state and memory?

Our language will manage state through variables. When a variable is declared, memory is set aside to store its value. As the program runs, assignment statements can update that value, which changes the current state of the program.

For example, if a variable named `count` starts at `0` and later changes to `count = count + 1`, the program state has changed because the value stored in memory is different. This reflects one of the key ideas of imperative programming: a program works by modifying stored values over time.

Memory use in our language will be simple and beginner-friendly. Variables created inside functions will be local, meaning they only exist while that function is running. Variables declared outside functions can be global and remain available throughout the program. This makes it easier to understand how data is stored, changed, and removed during execution.

## How does your syntax support sequential logic or control flow?

The syntax of our language will support sequential logic by reading from top to bottom, one statement at a time. Each instruction will clearly show what happens next. Blocks of code will be grouped using braces so the beginning and end of conditionals, loops, and functions are easy to identify.

For example:

- Assignment statements show direct state changes  
- `if` statements allow the program to choose between paths  
- `while` and `for` loops repeat actions until a condition changes  
- Functions organize tasks into reusable steps  

This structure makes the control flow predictable and easy to follow. A programmer can read the code in order and understand exactly how the program moves from one instruction to the next.

## Simple “main” program in our language

```md
func main() {
    let x = 0;
    let total = 0;

    while (x < 5) {
        total = total + x;
        x = x + 1;
    }

    if (total > 5) {
        print("Total is greater than 5");
    } else {
        print("Total is 5 or less");
    }

    print(total);
}
