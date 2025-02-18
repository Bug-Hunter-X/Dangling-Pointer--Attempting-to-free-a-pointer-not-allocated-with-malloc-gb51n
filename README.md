# Dangling Pointer Bug in C

This repository demonstrates a common C programming error: attempting to free a pointer that was not dynamically allocated using `malloc`, `calloc`, or similar functions. This leads to undefined behavior and can cause crashes or other unpredictable problems.

## Bug Description
The `bug.c` file contains a program that assigns an integer variable's address to a pointer and then attempts to free the pointer using `free()`. This is incorrect because `free()` should only be used on pointers obtained from memory allocation functions like `malloc()`.

## Solution
The `bugSolution.c` file demonstrates the corrected code.  It removes the erroneous `free(ptr)` call, since the pointer `ptr` doesn't point to dynamically allocated memory.  

## How to Reproduce
1. Clone this repository.
2. Compile `bug.c` using a C compiler (e.g., gcc):  `gcc bug.c -o bug`
3. Run the compiled executable: `./bug`
4. Observe the undefined behavior or potential crash.
5. Repeat steps 2-4 with `bugSolution.c` to see the corrected version.