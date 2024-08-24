## Python tips

### Primitive Data Types

#### Chars
- Use `ord()` to get the integer value of a character and `chr()` to convert it back

#### Arrays
- Instantiate a new array of a fixed size: `arr = [0]*26`
- Use `any(arr)` or `all(arr)` to check whether any or every value in an iterable are true
  - Works for sets and dicts too, but note that it checks the **keys**

#### Queues
- Queue data structure in Python (i.e. O(1) dequeue operation):
 - You can simulate this with a regular array and using `pop(0)`.
```python
from collections import deque
q = deque()
q.append('a')
q.popleft()
```

#### Variable definitions
- Can define multiple variables in one line with comma notation:
```
prev, curr = ListNode(-1), head
```