# HashMap

Hash table implementation in Java for key-value pair storage with constant-time average performance.

## 📖 Overview

HashMap is a data structure that implements the Map interface using a hash table. It stores key-value pairs and provides fast access, insertion, and deletion operations.

## ⚙️ Key Characteristics

- **Average Time Complexity**: O(1) for get, put, remove
- **Order**: Not guaranteed (unordered)
- **Null Keys**: Allows one null key
- **Null Values**: Allows multiple null values
- **Thread-Safe**: No (use ConcurrentHashMap for thread safety)

## 📝 Methods Reference

For detailed methods and usage, see **[HashMapMethods.md](./HashMapMethods.md)**

### Quick Reference

- `put(key, value)` - Insert/update key-value pair
- `get(key)` - Retrieve value for given key
- `getOrDefault(key, default)` - Get value or default if key doesn't exist
- `containsKey(key)` - Check if key exists
- `remove(key)` - Remove key-value pair
- `size()` - Get number of entries
- `isEmpty()` - Check if map is empty
- `clear()` - Remove all entries

## 💡 Common Use Cases

- Frequency counting
- Caching/memoization
- Two-sum type problems
- Anagram grouping
- First unique character

## 🔗 Related Topics

- HashSet (only keys, no values)
- LinkedHashMap (maintains insertion order)
- TreeMap (sorted order)
