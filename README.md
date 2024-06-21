
### `map` Function

The `map` function applies a given function to each item of an iterable (like a list) and returns a map object (which is an iterator). You can convert it to a list or other data types if needed.

**Syntax**:
```python
map(function, iterable)
```

- `function`: A function that takes one argument.
- `iterable`: An iterable (e.g., list, tuple).

**Example**:
```python
# Define a function to square a number
def square(x):
    return x * x

# Use map to apply the square function to each item in the list
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(square, numbers))

print(squared_numbers)  # Output: [1, 4, 9, 16, 25]
```

Using a lambda function with `map`:
```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x * x, numbers))

print(squared_numbers)  # Output: [1, 4, 9, 16, 25]
```

### `filter` Function

The `filter` function constructs an iterator from elements of an iterable for which a function returns true. In other words, it filters the iterable based on a function.

**Syntax**:
```python
filter(function, iterable)
```

- `function`: A function that returns a boolean value.
- `iterable`: An iterable (e.g., list, tuple).

**Example**:
```python
# Define a function to check if a number is even
def is_even(x):
    return x % 2 == 0

# Use filter to get only even numbers from the list
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(is_even, numbers))

print(even_numbers)  # Output: [2, 4, 6]
```

Using a lambda function with `filter`:
```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))

print(even_numbers)  # Output: [2, 4, 6]
```

### `sorted` Function

The `sorted` function returns a new sorted list from the elements of any iterable.

**Syntax**:
```python
sorted(iterable, key=None, reverse=False)
```

- `iterable`: An iterable (e.g., list, tuple).
- `key`: A function that serves as a key for the sort comparison. (Optional)
- `reverse`: A boolean. If `True`, the sorted list is reversed (or sorted in descending order).

**Example**:
```python
# Sort a list of numbers in ascending order
numbers = [5, 2, 9, 1, 5, 6]
sorted_numbers = sorted(numbers)

print(sorted_numbers)  # Output: [1, 2, 5, 5, 6, 9]
```

Sorting with a custom key function:
```python
# List of tuples
pairs = [(1, 2), (3, 1), (5, 4), (2, 3)]

# Sort pairs by the second element in each tuple
sorted_pairs = sorted(pairs, key=lambda pair: pair[1])

print(sorted_pairs)  # Output: [(3, 1), (1, 2), (2, 3), (5, 4)]
```

Sorting in reverse order:
```python
# Sort numbers in descending order
sorted_numbers_desc = sorted(numbers, reverse=True)

print(sorted_numbers_desc)  # Output: [9, 6, 5, 5, 2, 1]
```

### Summary

- **`map`**: Applies a function to all items in an iterable and returns a map object.
- **`filter`**: Filters elements in an iterable based on a function that returns true or false.
- **`sorted`**: Returns a new list containing all items from the iterable in ascending or descending order.

These functions are powerful tools for working with iterables in Python and can make your code more concise and readable. If you have more questions or need further examples, feel free to ask!
