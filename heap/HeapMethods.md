# Heap (Priority Queue)

Binary heap implementation using Java's PriorityQueue for efficient priority-based operations.

## 📖 Overview

A heap is a complete binary tree that satisfies the heap property. Java's PriorityQueue implements a min-heap by default, but can be configured as a max-heap.

## ⚙️ Key Characteristics

- **Time Complexity**: 
  - Insert: O(log n)
  - Remove Min/Max: O(log n)
  - Peek: O(1)
- **Structure**: Complete binary tree
- **Default**: Min-heap (smallest element at top)
- **Space Complexity**: O(n)

## 📝 Methods Reference

For detailed methods and usage, see **[HeapMethods.md](./HeapMethods.md)**

### Quick Reference

- `add(x)` / `offer(x)` - Insert element
- `peek()` - View top element without removing
- `poll()` - Remove and return top element
- `remove(x)` - Remove specific element
- `size()` - Get number of elements
- `isEmpty()` - Check if heap is empty

## 🔧 Heap Types

### Min Heap
```java
PriorityQueue<Integer> minHeap = new PriorityQueue<>();
```

### Max Heap
```java
PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());
```

## 💡 Common Use Cases

- K largest/smallest elements
- Median finding
- Merge K sorted lists
- Dijkstra's algorithm
- Huffman coding
- Task scheduling

## 🔗 Related Topics

- Binary Tree
- Heap Sort
- Priority Queue ADT
