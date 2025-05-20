## Java Tips

### Primitive Data Types

#### Chars
- Defined with single quotes and can be used as integer values
- Character is a wrapper class that encapsulates the primitive char data type and provides helpful utilities like: `Character.isLetterOrDigit(c)` or `Character.toLowerCase(c)`

#### Strings
- Use `toCharArray()` to convert a string to an array of characters (`char[]`)
- Use `charAt()` to get the character at a specific index
- Use `equals()` or `equalsIgnoreCase()` to compare strings since they are objects
- Use `length()` to get the length of the string

#### Arrays
- Define an array in place: `int[] array = {1, 2, 3, 4, 5};`
  - When using this notation in the return statement, it looks like `return new int[] {1, 2};`
- Define an array of a specific size `int[] array = new int[size];`
- Enable the stream API with `Arrays.stream()`: `Arrays.stream(array).sum()`
- Convert to String using `Arrays.toString()`
- Properties:
  - `.length`

### Collections
- Only need to define types on the lefthand side of the assignment operator, Java can infer the type on the righthand: `Map<String,List<String>> map = new HashMap<>();`
- Common methods (does not apply to HashMaps):
  - `add(element)`
  - `addAll(collection)`
  - `contains(element)`
  - `size()` - does work for HashMaps too

#### Hashmaps
- Methods:
  - `put(K key, V value)`
  - `putIfAbsent(K key, V value)`, e.g. `map.putIfAbsent(key, new ArrayList<String>());`
  - `remove(Object key)`
  - `containsKey(Object key)`
  - `values()` to return a Collection of its values, may need to wrap in new `ArrayList<>();` if a List is required
  - `keySet()` to return a set of keys

#### Stacks
```
Stack<Character> stack = new Stack<>();
```

- Methods:
  - `push(element)`
  - `pop()`
  - `peek()` - preview last element

### Loops
- for:
```
for (int i = 0; i < 5; i++) {
    System.out.println("Basic for loop: " + i);
}
```

- for-each:
```
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    System.out.println("For-each loop: " + num);
}
```