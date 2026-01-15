# Miscellaneous

Common pitfalls and important notes for various data structures in Java.

## 📖 Overview

This section contains important tips, common mistakes, and best practices to avoid when working with data structures in Java. Learning what NOT to do is just as important as learning what to do!

## 📝 Reference

For detailed pitfalls, see **[CommonPitfalls.md](./CommonPitfalls.md)**

## ⚠️ Common Pitfalls Summary

### HashMap
- ❌ Forgetting to use `getOrDefault()` and getting NullPointerException
- ❌ Modifying map while iterating (ConcurrentModificationException)

### Stack
- ❌ Calling `pop()` or `peek()` on empty stack → EmptyStackException
- ❌ Using legacy `Stack` class instead of `ArrayDeque` in production code

### Queue
- ❌ Confusing `poll()` (returns null) vs `remove()` (throws exception)
- ❌ Assuming queue has a fixed size

### StringBuilder
- ❌ Forgetting to convert to String using `toString()`
- ❌ Using String concatenation in loops instead of StringBuilder

### Heap (PriorityQueue)
- ❌ Forgetting that PriorityQueue is a **MIN heap by default**
- ❌ Using `remove(x)` expecting O(log n) - it's actually O(n)

## 💡 Best Practices

### 1. Always Check for Empty
```java
// Good
if (!stack.isEmpty()) {
    int top = stack.pop();
}

// Bad - may throw exception
int top = stack.pop();
```

### 2. Use getOrDefault
```java
// Good
map.put(key, map.getOrDefault(key, 0) + 1);

// Bad - may throw NullPointerException
map.put(key, map.get(key) + 1);
```

### 3. Choose Right Data Structure
```java
// For stack operations - use Deque
Deque<Integer> stack = new ArrayDeque<>();

// Not Stack class
Stack<Integer> stack = new Stack<>(); // Legacy, slower
```

### 4. StringBuilder in Loops
```java
// Good - O(n)
StringBuilder sb = new StringBuilder();
for (String s : list) {
    sb.append(s);
}

// Bad - O(n²)
String result = "";
for (String s : list) {
    result += s;
}
```

## 🔍 Debugging Tips

- Print data structure state before operations
- Use debugger to inspect internal state
- Check boundary conditions (empty, single element, full)
- Verify time complexity assumptions with large datasets

## 🔗 Additional Resources

- Java Collections Framework Documentation
- Effective Java by Joshua Bloch
- Algorithm Analysis and Design
