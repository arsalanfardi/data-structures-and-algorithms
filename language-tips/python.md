## Python tips

### Primitive Data Types

#### Chars
- Use `ord()` to get the integer value of a character and `chr()` to convert it back

#### Arrays
- Instantiate a new array of a fixed size: `arr = [0]*26`
- Use `any(arr)` or `all(arr)` to check whether any or every value in an iterable are true
  - Works for sets and dicts too, but note that it checks the **keys**
