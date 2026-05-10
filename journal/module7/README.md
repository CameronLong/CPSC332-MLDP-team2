# Procedures and Scope Reflection – Cameron Long, Jenny LaFlair, Julian Davis, Kaylie Marshall

## How will procedures and functions be designed in your custom language?
In our language, functions will follow a style similar to C. In the example below, the function declaration includes a data type and uses curly
braces to denote the start and end of the function body. We decided to make our functions this style because it is easier to read with functions s
tarting and ending clearly, while having a specific data type to help with readability and usability.

### Function Example
```
func int square(int n){
  return n * n;
}
```

## How will variable scope (static or dynamic) be handled?
Variables will use static scoping since it is easier to read, debug, and optimize. Static scoping also helps with program security
since a variable cannot be accessed outside of the scope it is defined in. Static scoping was also selected because this allows us to use multiple
variables with the same name, such as i for loop conditions, throughout the code without conflicts.

## How will parameter passing (by value, by reference, by name) work?
Parameter passing can be done either by value or by reference, since both methods serve a distinct purpose. In our language we want to
have the option to either pass parameters by value for smaller types like integers or booleans and by reference for pointers, arrays, and
vectors. Having both in the language will allow the language to be versatile and used in multiple applications. 
