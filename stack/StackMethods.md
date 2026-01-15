# Stack

Last-In-First-Out (LIFO) data structure implementation in Java.

## 📖 Overview

Stack is a linear data structure that follows the LIFO principle - the last element added is the first one to be removed. Think of it like a stack of plates.

## ⚙️ Key Characteristics

- **Principle**: LIFO (Last In, First Out)
- **Time Complexity**: O(1) for push, pop, peek
- **Implementation**: Java's Stack class (legacy) or ArrayDeque (recommended)
- **Space Complexity**: O(n)

## 📝 Methods Reference

For detailed methods and usage, see **[StackMethods.md](./StackMethods.md)**

### Quick Reference

- `push(x)` - Add element to top
- `pop()` - Remove and return top element
- `peek()` - View top element without removing
- `isEmpty()` - Check if stack is empty
- `size()` - Get number of elements
- `search(x)` - Find position of element from top

## ⚠️ Important Notes

- `pop()` and `peek()` throw EmptyStackException if stack is empty
- **Modern Alternative**: Use `ArrayDeque` instead of `Stack` for better performance
  ```java
  Deque<Integer> stack = new ArrayDeque<>();
  ```

## 💡 Common Use Cases

- Parentheses matching/validation
- Expression evaluation (infix, postfix, prefix)
- Backtracking problems
- Function call stack (recursion)
- Undo/Redo operations
- Browser history
- Depth-First Search (DFS)

## 🔗 Related Topics

- Queue (FIFO counterpart)
- Deque (double-ended queue)
- Recursion
