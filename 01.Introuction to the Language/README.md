# Introduction to C++

C++ was created in 1979 by Bjarne Stroustrup as an extension of the C programming language - C with classes. Like C, it is a low-level, high-performance programming language, but with additional features such as: classes, objects, and exceptions.

## Basics of C++ Programming

Below are the basics concepts and components needed to get started with C++ programming:

### Including Libraries

In C++ code, you'll often see the `#include` directive at the top of files. This is used to include code written somewhere else, be it external libraries or header files. 

Using the `#include` directive, we can reuse code written by other people, such as `std::cout` from the standard input/output library - `<iostream>` - for displaying output to the terminal.

    #include <iostream>

    int main() {
        std::cout << "Hello, World!";

        return 0;
    }

### Main Function

Every C++ starts from the `main` function, as a results, every C++ ***must*** have a main function:

    int main() {
        // some code
        return 0;
    }

### Input/Output

One of the first things you'll want to do when you start writing C++ programs is take in user input and display an output to the terminal. To do this, C++ has two in-built objects, `std::cin` for taking input and `std::cout` for output. (*These are from the `<iostream>` library, so be sure to include it!*)

In the following example program, a user can input an integer and that value is displayed:

    #include <iostream>

    int main() {
        int number;
        std::cout << "Enter an integer: ";
        std::cin >> number;
        std::cout << "You entered: " << number << std::endl;
    }

(*Here `std::endl` essentially acts like a newline operator, with a bit more going on. It's also from the `<iostream>` library*)

### Variables and Data Types

In C++, like many programming languages, we can define variables which get assigned values and are used in various ways. A variable has a type, which tells us what values it can have. In C++ there are several basic, built-in types, such as:

- `int`: **32 bit** integer value
- `float`: **32 bit/single-precision** floating point value
- `double`: **64 bit/double-precision** floating point value
- `char`: single **8 bit** character

C++ is a strongly-typed language, meaning that a variable needs to be given a type at it's declaration, before it's used:

    int x;
    float y;
    double z;
    char c;

### Control Structures

In C++ the flow of code can be controlled via conditional execution or iteration, using `if`, `else`, `while`, `for`, and `switch` statements.

#### If-Else Statement

    if (condition1) {
        // Execute code if condition1 is true
    } else if (condition2) {
        // Execute code if condition1 is not 
        // true, but condition2 is true
    } else {
        // Execute code if condition1 and
        // condition2 are false
    }

#### While Loop

    while (condition) {
        // Execute code iteratively while
        // condition is true
    }

#### For Loop

    for (initialization; condition; update) {
        // Execute code iteratively while
        // condition is true
    }

#### Switch Statement

    switch (variable) {
        case value1:
            // Execute code if variable == value1
            break; // be sure to break,
                      otherwise code will flow into
                      next case
        case value2:
            // Execute code if variable == value1
            break;

        // More cases...

        default:
            // Execute code if variable doesn't
            // match any case value
    }

### Functions

If you write a section of code to perform a job, you shouldn't write it again; it could lead to typos and difficulty maintaining/updating the code. But what if you need to use that same logic elsewhere in your code? How do you do this without writing it again?

The answer to th above is functions. In C++, like many other programming languages, you can create blocks of code - known as functions - which perform a specific task and can be reused.

Functions have a:
- name (which is used to call the code at different places in your code)
- parameter list (things your function needs to perform its logic)
- function body (the code logic)
- return type (the type of the result returned by the function)

    ReturnType functionName (ParamType1 param1, ParamType2 param2) {
        // Function body
        // ...
        return returnValue;
    }

Below is an example of how a function can be used to reuse logic that adds two integers:

    int add(int a, int b) {
        return a + b;
    }

    int main() {
        int result = add(3, 4);
        std::cout << "3 + 4 = " << result << std::endl;

        int newResult = add(5, 2);
        std::cout << "5 + 2 = " << result << std::endl;
    }
