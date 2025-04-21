# 🧠 C Programming Viva Preparation Guide - Answers

## 🔹 Core Basics

### Q: What is the history of C language and its features?

**A:** C was developed in 1972 by Dennis Ritchie at Bell Labs. It was created to rewrite the Unix OS. Key features:

- Procedural language
- Low-level memory access
- Fast execution
- Rich set of operators
- Portable code

### Q: Structure of a C program

**A:** A basic C program includes:

1. Preprocessor directives
2. Global declarations
3. `main()` function
4. Function definitions

```c
#include<stdio.h>
int main() {
    printf("Hello, World!\n");
    return 0;
}
```

### Q: Compilation process

**A:**

1. **Preprocessor**: Handles `#include`, `#define`
2. **Compiler**: Converts code to assembly
3. **Assembler**: Converts assembly to object code
4. **Linker**: Combines object files and libraries
5. **Loader**: Loads executable into memory

### Q: Difference between Compiler and Interpreter

**A:**

- **Compiler**: Converts entire code to machine code before execution (e.g., C)
- **Interpreter**: Converts line by line during execution (e.g., Python)

---

## 🔹 Data Types and Variables

### Q: Primitive data types

**A:** `int`, `char`, `float`, `double`

- int Size: 4 bytes (can vary by system).
- char Size: 1 byte
- float Size: 4 byte
- double Size: 8 byte

### Q: Derived data types

**A:** Arrays, pointers, structures, unions

### Q: Type casting

- **Implicit**: `int a = 5.5;` → automatically converts to int
- **Explicit**: `int a = (int)5.5;`

### Q: Keywords

- `const`: Immutable variable
- `volatile`: Value may change unexpectedly
- `static`: Retains value across function calls
- `extern`: Refers to a global variable
- `register`: Requests CPU register storage

---

## 🔹 Operators and Expressions

### Q: Types of operators

- Arithmetic: `+ - * / %`
- Relational: `== != > < >= <=`
- Logical: `&& || !`
- Bitwise: `& | ^ ~ << >>`
- Assignment: `= += -= *=`
- Ternary: `condition ? true : false`
- `sizeof`: Returns size in bytes

### Q: Operator precedence

**A:** Defines evaluation order. E.g., `* /` have higher precedence than `+ -`.

# Operator Precedence in C

Operator precedence determines the order in which operators are evaluated in expressions.

## Highest to Lowest Precedence

| Precedence Level | Operators                                   | Description                        | Associativity         |
|------------------|---------------------------------------------|------------------------------------|------------------------|
| 1                | `()` `[]` `.` `->`                          | Function call, array, member access| Left to Right          |
| 2                | `++` `--` `+` `-` `!` `~` `*` `&` `sizeof`   | Unary operators                    | Right to Left          |
| 3                | `*` `/` `%`                                 | Multiplication, Division, Modulus | Left to Right          |
| 4                | `+` `-`                                     | Addition, Subtraction              | Left to Right          |
| 5                | `<<` `>>`                                   | Bitwise shift                      | Left to Right          |
| 6                | `<` `<=` `>` `>=`                           | Relational                         | Left to Right          |
| 7                | `==` `!=`                                   | Equality                           | Left to Right          |
| 8                | `&`                                         | Bitwise AND                        | Left to Right          |
| 9                | `^`                                         | Bitwise XOR                        | Left to Right          |
| 10               | `|`                                         | Bitwise OR                         | Left to Right          |
| 11               | `&&`                                        | Logical AND                        | Left to Right          |
| 12               | `||`                                        | Logical OR                         | Left to Right          |
| 13               | `?:`                                        | Ternary conditional                | Right to Left          |
| 14               | `=` `+=` `-=` `*=` `/=` `%=` `<<=` `>>=` etc| Assignment                         | Right to Left          |
| 15               | `,`                                         | Comma                              | Left to Right          |

> 💡 Use parentheses `()` to make the evaluation order explicit and avoid confusion.



---

## 🔹 Control Flow Statements

### Q: Conditional Statements

- `if`, `else if`, `else`, `switch-case`

### Q: Loops

- `for`, `while`, `do-while`

### Q: Loop control

- `break`: Exit loop
- `continue`: Skip to next iteration
- `goto`: Jump to label (not recommended)

---

## 🔹 Functions

### Q: Function declaration vs definition

- **Declaration**: Prototype, e.g., `int sum(int, int);`
- **Definition**: Actual body

### Q: Parameter passing

- **Call by value**: Copy passed
- **Call by reference**: Address passed (via pointer)

### Q: Recursion

**A:** Function calling itself

```c
int factorial(int n) {
    if(n == 0) return 1;
    return n * factorial(n - 1);
}
```

### Q: Scope and lifetime

- **Scope**: Visibility
- **Lifetime**: Duration of existence

---

## 🔹 Arrays and Strings

### Q: 1D and 2D arrays

```c
int arr[10];
int matrix[3][3];
```

### Q: Common string functions

- `strlen()`: Length
- `strcpy()`: Copy
- `strcat()`: Concatenate
- `strcmp()`: Compare

### Q: Character array vs string

# Character Array vs String in C

## 🧵 Basic Difference

| Feature                  | Character Array                           | String (Null-Terminated Character Array) |
|--------------------------|--------------------------------------------|-------------------------------------------|
| **Definition**           | An array of characters                    | A character array ending with `\0`        |
| **Null Terminator (`\0`)**| Not necessarily included                 | Always ends with `\0`                     |
| **Example**              | `char arr[] = {'H', 'e', 'l', 'l', 'o'};` | `char str[] = "Hello";`                   |
| **Size**                 | 5                                         | 6 (5 letters + 1 null character)          |
| **Library Support**      | Can't use string functions like `strlen` | Works with string functions (`strlen`, `strcpy`, etc.) |
| **Printing with `%s`**   | May print garbage after characters        | Safe to print with `%s`                   |

---

## 🔍 Example Code

```c
#include <stdio.h>
#include <string.h>

int main() {
    char arr[] = {'H', 'e', 'l', 'l', 'o'};
    char str[] = "Hello";

    printf("arr: ");
    for (int i = 0; i < 5; i++) {
        printf("%c", arr[i]);
    }

    printf("\nstr: %s", str); // Safe with %s
    return 0;
}

```
---

## 🔹 Pointers

### Q: Declaration and usage

```c
int a = 5;
int *p = &a;


### Q: Pointers and arrays

- Array name is a pointer to the first element

### Q: Pointers and functions

- Pass pointer to allow modification of actual data

### Q: Pointer to pointer

```c
int **pp;
```

I apologize for the confusion earlier! Here's the **complete content in one copyable Markdown block** without any interruptions:

```md
# 🔹 Pointers in C

Pointers are variables that store the **memory addresses** of other variables. They are powerful tools in C that allow dynamic memory management, efficient array handling, and more.

---

## 📌 Declaration and Usage

### 🔹 Declaration

```c
int *ptr;      // pointer to an integer
char *cptr;    // pointer to a character
float *fptr;   // pointer to a float
```

### 🔹 Usage

```c
int x = 10;
int *ptr = &x;

printf("Address of x: %p\n", ptr);
printf("Value of x: %d\n", *ptr);  // Dereferencing the pointer
```

---

## 📦 Pointers and Arrays

An array name in C is actually a pointer to its first element.

```c
int arr[5] = {1, 2, 3, 4, 5};
int *p = arr;

printf("%d\n", *(p + 2));  // Output: 3
```

You can use pointers to traverse arrays efficiently using pointer arithmetic.

---

## 🧩 Pointers and Functions

Pointers allow **pass-by-reference**, which means you can modify actual variables from within a function.

### 🔹 Example: Swapping two numbers

```c
#include <stdio.h>

void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 5, y = 10;
    swap(&x, &y);
    printf("x = %d, y = %d\n", x, y);
    return 0;
}
```

---

## 🔁 Pointer to Pointer

You can have pointers that store the address of other pointers.

```c
int x = 10;
int *p = &x;
int **pp = &p;

printf("Value of x: %d\n", **pp);
```

---

## 💾 Dynamic Memory Allocation

C provides functions in `<stdlib.h>` for runtime memory management.

### 🔹 `malloc()`

Allocates a single block of memory.

```c
int *arr = (int *)malloc(5 * sizeof(int));
```

### 🔹 `calloc()`

Allocates multiple blocks and initializes them to zero.

```c
int *arr = (int *)calloc(5, sizeof(int));
```

### 🔹 `realloc()`

Changes the size of previously allocated memory.

```c
arr = (int *)realloc(arr, 10 * sizeof(int));
```

### 🔹 `free()`

Frees allocated memory.

```c
free(arr);
```

> ⚠️ Always `free()` dynamically allocated memory to avoid memory leaks.

---

## ✅ Summary

- Use `*` to declare and dereference pointers.
- Pointers can point to arrays, functions, and other pointers.
- Enable pass-by-reference using pointers in functions.
- Dynamic memory functions: `malloc`, `calloc`, `realloc`, `free`.


### Q: Dynamic memory allocation

- `malloc()`, `calloc()`, `realloc()`, `free()`

---

## 🔹 Structures and Unions

### Q: Define struct and union

```c
struct Student {
    int id;
    char name[20];
};
union Data {
    int i;
    float f;
};
```

### Q: Difference

- **Struct**: All members have separate memory
- **Union**: Shared memory for all members

### Q: Nesting

- Structures can contain other structures

### Q: `typedef` and `enum`

```c
typedef struct Student Stud;
enum Days {Mon, Tue};
```

---

## 🔹 File Handling

### Q: File operations

```c
FILE *fp = fopen("file.txt", "r");
fclose(fp);
```

- `fprintf()`, `fscanf()`
- `fread()`, `fwrite()`
- `fseek()`, `ftell()`

### Q: File modes

- `r`, `w`, `a`, `r+`, `w+`, `a+`

---

## 🔹 Preprocessor Directives

### Q: Directives

- `#define`, `#include`, `#ifdef`, `#ifndef`, `#endif`, `#undef`

### Q: Macros vs functions

- Macros: Text substitution
- Functions: Actual code, better for debugging


# 🔹 Preprocessor Directives in C

Preprocessor directives are instructions that are processed by the preprocessor before the actual compilation begins. They modify the source code or provide information for the compiler.

---

## 📌 Common Preprocessor Directives

### 1. `#define`

Defines a macro or constant.

```c
#define PI 3.14
#define MAX(a, b) ((a) > (b) ? (a) : (b))
```

- `PI` is a constant that holds the value `3.14`.
- `MAX(a, b)` is a macro to find the maximum of two values.

### 2. `#include`

Includes header files into the program. This can be a standard library header or a custom header file.

```c
#include <stdio.h>    // Standard library header
#include "myheader.h"  // Custom header file
```

- `<stdio.h>` is for input and output operations.
- `"myheader.h"` is a user-defined header file.

### 3. `#ifdef`, `#ifndef`, `#endif`

Conditional compilation directives. Used to include/exclude code based on whether a macro is defined or not.

```c
#ifdef DEBUG
    printf("Debugging enabled.\n");
#endif
```

- `#ifdef` checks if a macro is defined.
- `#ifndef` checks if a macro is **not** defined.

### 4. `#if`, `#else`, `#elif`

Used to check conditions during preprocessing.

```c
#if defined(WINDOWS)
    printf("Windows OS\n");
#elif defined(LINUX)
    printf("Linux OS\n");
#else
    printf("Unknown OS\n");
#endif
```

- `#if` evaluates a condition.
- `#else` provides an alternative if the condition is false.
- `#elif` provides an "else if" condition.

### 5. `#undef`

Undefines a macro previously defined with `#define`.

```c
#define PI 3.14
#undef PI
```

- After `#undef`, `PI` is no longer available.

---

## 📌 Macros vs Functions

### 🔹 Macros

- **Definition**: Macros are preprocessor directives that perform text substitution before the code is compiled.
- **Syntax**: Defined using `#define`.
- **Evaluation**: Macros are evaluated at the preprocessing stage, not during runtime.
- **No type checking**: Macros do not perform type checking or error checking.
- **Performance**: Macros may provide faster execution as they avoid function calls.

#### Example: Macro

```c
#define SQUARE(x) ((x) * (x))

int main() {
    int result = SQUARE(5);  // Expands to ((5) * (5)) during preprocessing
    printf("Square: %d\n", result);
    return 0;
}
```

**Advantages**:
- No function call overhead, faster execution in simple cases.
- Simple syntax for mathematical operations.

**Disadvantages**:
- Lack of type safety.
- Potential side effects from multiple evaluations.

---

### 🔹 Functions

- **Definition**: Functions are blocks of code that perform specific tasks and can be reused.
- **Syntax**: Defined with `return_type function_name(parameters) { }`.
- **Evaluation**: Functions are evaluated during runtime.
- **Type checking**: Functions perform type checking and error checking at compile time.
- **Performance**: Function calls introduce a slight overhead due to the stack management.

#### Example: Function

```c
int square(int x) {
    return x * x;
}

int main() {
    int result = square(5);  // Function call at runtime
    printf("Square: %d\n", result);
    return 0;
}
```

**Advantages**:
- Type-safe and error-checked.
- Easier to debug and maintain.
- Supports recursion and complex operations.

**Disadvantages**:
- Function call overhead, slower than macros in simple cases.

---

## ✅ Summary

| Directive     | Description                                           |
|---------------|-------------------------------------------------------|
| `#define`     | Defines constants or macros                            |
| `#include`    | Includes header files                                  |
| `#ifdef`      | Checks if a macro is defined                           |
| `#ifndef`     | Checks if a macro is not defined                       |
| `#if`         | Evaluates a condition                                  |
| `#else`       | Provides an alternative block if the condition is false|
| `#elif`       | Provides an "else if" condition                        |
| `#endif`      | Ends a conditional block                               |
| `#undef`      | Undefines a macro                                      |

---

| Feature       | Macros                                    | Functions                                |
|---------------|-------------------------------------------|------------------------------------------|
| **Syntax**    | `#define MACRO_NAME(...)`                 | `return_type function_name(...){}`       |
| **Evaluation**| Preprocessing (before compilation)       | Runtime (during execution)               |
| **Type Safety**| No type checking                        | Type-safe with error checking            |
| **Performance**| Faster (no overhead)                    | Slight overhead due to function calls    |
| **Use cases** | Simple tasks, mathematical operations    | Complex logic, error handling, recursion |

---

Macros are generally faster due to the lack of function call overhead but can cause issues due to lack of type checking. Functions provide better safety and debugging support but can introduce slight performance overhead.

---
## 🔹 Common Coding Questions

### Factorial using recursion

```c
int factorial(int n) {
    return (n <= 1) ? 1 : n * factorial(n - 1);
}
```

### Fibonacci series

```c
int fib(int n) {
    if(n <= 1) return n;
    return fib(n-1) + fib(n-2);
}
```

### Prime number check

```c
int isPrime(int n) {
    for(int i = 2; i <= n/2; i++)
        if(n % i == 0) return 0;
    return 1;
}
```

### Palindrome check (string)

```c
int isPalindrome(char str[]) {
    int i = 0, j = strlen(str) - 1;
    while(i < j)
        if(str[i++] != str[j--]) return 0;
    return 1;
}
```

### String reversal

```c
void reverse(char str[]) {
    int i = 0, j = strlen(str) - 1;
    while(i < j) {
        char temp = str[i];
        str[i++] = str[j];
        str[j--] = temp;
    }
}
```

### Sorting algorithms

- **Bubble**: Compare adjacent
- **Insertion**: Insert in sorted part
- **Selection**: Select min and swap

### Swapping using pointers

```c
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
```

### Matrix operations

- Addition, subtraction, multiplication using nested loops

---

> 📌 **Tip**: Explain your logic clearly, use diagrams or examples when needed. Stay calm and confident!
