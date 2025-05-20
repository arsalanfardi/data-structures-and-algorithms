## Python tips

### Primitive Data Types

#### Chars
- Use `ord()` to get the integer value of a character and `chr()` to convert it back

#### Strings
- Use `sorted(s)` to sort strings

#### Arrays
- Instantiate a new array of a fixed size: `arr = [0]*26`
- Use `any(arr)` or `all(arr)` to check whether any or every value in an iterable are true
  - Works for sets and dicts too, but note that it checks the **keys**

### Collections

#### Queues
- Queue data structure in Python (i.e. O(1) dequeue operation):
 - You can simulate this with a regular array and using `pop(0)`.
```python
from collections import deque
q = deque()
q.append('a')
q.popleft()
```

#### Sets
```
seen = set([1, 2, 3])
# Add an element
seen.add(4)
# Remove an element, raises KeyError if not found
seen.remove(1)
# Remove an element, will not raise an error if key doesn't exist
seen.discard(5)
# Check if element exists
if 3 in seen:
  ...
```

#### Dictionaries
- Use `.values()` to return a list of values
- A tuple is hashable as a key, but a list is not
- Default dictionaries provide default values
```
from collections import defaultdict

# Create a defaultdict with a default empty list
d = defaultdict(list)
d[i].append(1)

# Create a defaultdict with a default 0 integer
d = defaultdict(int)
d[i] += 1
```

### Misc.

#### Variable definitions
- Can define multiple variables in one line with comma notation:
```
prev, curr = ListNode(-1), head
```