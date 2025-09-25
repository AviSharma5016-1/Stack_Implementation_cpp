# Stack Implementation in C++

### Aim  
To implement a **simple stack data structure using arrays in C++**, with support for push, pop, and display operations via an interactive menu.

***

### Theory  

A **stack** is a linear data structure that follows the **LIFO (Last In, First Out)** principle, meaning the most recently added element is removed first. It is commonly used in function calls, expression evaluation, and undo mechanisms.

#### Major Operations in a Stack

| Operation | Purpose               | Example                                |
|-----------|-----------------------|----------------------------------------|
| **Push**  | Inserts an element on top  | Push 10, then push 15 → Top is 15     |
| **Pop**   | Removes the top element    | Pop → Removes 15, Top becomes 10      |
| **Display** | Shows all elements, top first | Stack: 15 10 (top to bottom)         |
| **Overflow** | Stack is full (cannot push) | After 5 pushes, sixth triggers overflow |
| **Underflow** | Stack is empty (cannot pop) | Pop on empty stack triggers underflow |

#### Array Representation in Stack

- **arr[MAX]**: Array to store stack elements.
- **top**: Index of current top element (starts at -1).

| State        | Stack Elements (Top to Bottom) | Value of "top" |
|--------------|-------------------------------|----------------|
| Empty        | —                             | -1             |
| After push(23) | 23                            | 0              |
| After push(45) | 45 23                         | 1              |
| After pop()    | 23                            | 0              |
| Full           | 88 77 66 45 23                | 4              |

Stacks have fixed size based on MAX (here, MAX=5). Overflow occurs if trying to push when top == MAX-1. Underflow occurs if trying to pop when top == -1.

***

### Algorithm  

- **Initialization**
  - Set `top = -1`.
- **Push(val)**
  - If `top == MAX-1`, print Stack Overflow.
  - Else, increment `top` and assign `arr[top] = val`. Print confirmation.
- **Pop()**
  - If `top == -1`, print Stack Underflow.
  - Else, print `arr[top]` and decrement `top`.
- **Display()**
  - If `top == -1`, print Stack is empty.
  - Else, print elements from `top` down to `0`.
- **User Menu**
  - Loop: Prompt user for operation (Push, Pop, Display, Exit).
  - Invoke matching stack operation.

***

### Conclusion  

This program presents a clear demonstration of the **stack data structure using arrays** in C++ . The interactive menu enables users to test all fundamental stack operations, with robust handling of overflow and underflow cases. While this stack has a static size, the principles remain the same for dynamic and linked-list-based stacks. A strong understanding of stacks underlies many systems and applications in computing.

---
