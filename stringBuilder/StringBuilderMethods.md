# StringBuilder

Mutable string manipulation class in Java for efficient string operations.

## 📖 Overview

StringBuilder is a mutable sequence of characters. Unlike String (which is immutable), StringBuilder allows modification without creating new objects, making it more efficient for string manipulation.

## ⚙️ Key Characteristics

- **Mutability**: Mutable (can be modified)
- **Thread-Safe**: No (use StringBuffer for thread safety)
- **Performance**: Much faster than String concatenation in loops
- **Memory**: More efficient for multiple modifications
- **Time Complexity**: 
  - Append: Amortized O(1)
  - Insert/Delete: O(n)

## 📝 Methods Reference

For detailed methods and usage, see **[StringBuilderMethods.md](./StringBuilderMethods.md)**

### Quick Reference

- `append(x)` - Add to end
- `insert(index, x)` - Insert at specific position
- `delete(start, end)` - Delete range [start, end)
- `deleteCharAt(i)` - Delete character at index i
- `reverse()` - Reverse the entire string
- `setCharAt(i, c)` - Replace character at index i
- `length()` - Get current length
- `toString()` - Convert to String

## 🔄 String vs StringBuilder

### When to use String:
- Small number of modifications
- String won't change
- Thread safety with immutability needed

### When to use StringBuilder:
- ✅ Many string modifications
- ✅ Building strings in loops
- ✅ Complex string manipulations
- ✅ Performance is critical

## 💡 Common Use Cases

- Building strings in loops
- Reversing strings
- String manipulation in place
- Concatenating many strings
- Parsing and formatting
- Token building
- Dynamic string construction

## 📊 Performance Example

```java
// ❌ Inefficient - Creates many String objects
String result = "";
for (int i = 0; i < 1000; i++) {
    result += i;  // O(n²) time
}

// ✅ Efficient - Single StringBuilder object
StringBuilder sb = new StringBuilder();
for (int i = 0; i < 1000; i++) {
    sb.append(i);  // O(n) time
}
String result = sb.toString();
```

## 🔗 Related Topics

- String (immutable)
- StringBuffer (thread-safe mutable)
- Character arrays
