# Variables and assignment

## What
Python variables are references to objects, not containers.

## Why
Understanding this helps avoid unexpected side effects
when working with mutable objects.

## Example
```python
a = [1, 2, 3]
b = a
b.append(4)
print(a)  # [1, 2, 3, 4]
```

## Notes
- Assignment copies references, not values
- Use `copy()` or `deepcopy()` when necessary
