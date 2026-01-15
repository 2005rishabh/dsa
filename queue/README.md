# Queue

First-In-First-Out (FIFO) data structure implementations in Java.

## 📖 Overview

Queue is a linear data structure that follows the FIFO principle - the first element added is the first one to be removed. Think of it like a line of people waiting.

## ⚙️ Key Characteristics

- **Principle**: FIFO (First In, First Out)
- **Time Complexity**: O(1) for enqueue and dequeue
- **Implementation**: LinkedList or ArrayDeque
- **Space Complexity**: O(n)

## 📝 Methods Reference

This folder contains two comprehensive guides:

- **[QueueMethods.md](./QueueMethods.md)** - Standard Queue operations
- **[DequeueMethods.md](./DequeueMethods.md)** - Double-ended Queue (Deque) operations

## 🔧 Queue Types

### 1. Standard Queue
```java
Queue<Integer> q = new LinkedList<>();
```

**Quick Reference:**
- `add(x)` / `offer(x)` - Add element to rear
- `poll()` - Remove and return front element (returns null if empty)
- `remove()` - Remove and return front element (throws exception if empty)
- `peek()` - View front element without removing
- `isEmpty()` - Check if queue is empty
- `size()` - Get number of elements

### 2. Deque (Double-Ended Queue)
```java
Deque<Integer> dq = new ArrayDeque<>();
```

**Advantages:**
- Can act as both Stack and Queue
- Faster than Stack and LinkedList
- Operations at both ends

**Quick Reference:**
- `addFirst(x)` / `addLast(x)` - Add at front/rear
- `pollFirst()` / `pollLast()` - Remove from front/rear
- `peekFirst()` / `peekLast()` - View front/rear element

## 💡 Common Use Cases

- **Queue:**
  - Breadth-First Search (BFS)
  - Task scheduling
  - Print queue
  - CPU scheduling
  - Level order traversal
  
- **Deque:**
  - Sliding window maximum/minimum
  - Palindrome checking
  - Browser navigation (forward/backward)
  - Undo/Redo with peek

## 🔗 Related Topics

- Stack (LIFO counterpart)
- Priority Queue (Heap)
- Circular Queue
