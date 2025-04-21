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

int Size: 4 bytes (can vary by system).
char Size: 1 byte
float Size: 4 byte
double Size: 8 byte

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

- Char array: Holds characters
- String: Null-terminated char array

---

## 🔹 Pointers

### Q: Declaration and usage

```c
int a = 5;
int *p = &a;
```

### Q: Pointers and arrays

- Array name is a pointer to the first element

### Q: Pointers and functions

- Pass pointer to allow modification of actual data

### Q: Pointer to pointer

```c
int **pp;
```

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
