# Tuples

Basically arrays.

Can have multiple data types in single tuple.

Negative index - -1 will give the last element. -2 will be the element before that and so on.

Slicing - First three elements would be tuple[0:3] where the second index is one larger than the last element you want. 

`len` command to find length of the tuple.

Tuples are immutable - can't be changed after being assigned. You can't change an item after assigning a tuple by simply doing tuple[0] = 5 for example. You gotta assign the entire tuple again.

Sort tuples - `sorted(tuple)`

Nesting - tuples can contain tuples themselves. ^ce7886

# Lists

They are like tuples but they are **mutable**. Can change individual elements.

Gotta use square brackets instead of regular ones to initialize it.

You can nest lists. 

- **Concatenation** works same as it does w/ strings - [[Strings#^concat]]
- **Extending** also concatenates lists. `L.extend("new", 10, 'list')`. This adds the list specified as arguments to the existing list 'L'.
- **Appending** adds the new list as a single element to the existing list ([[Tuples & Lists#^ce7886]]). 

Can convert strings into a list by doing `"example string".split()`. The arguments in the brackets following the word split can have the separator to split the string on. The default separator is a whitespace. It can also be a comma - `"example,string".split(",")`.
The separator in Python is called a **delimiter**.

**Aliasing**
If you assign a list as equal to another list then modifying the first list will make modification to the other list too.
For example - 
```python title:Example
A = [10, 5, 9, 11]
B = A

A[0] = 12

print(B)

Output: [12, 5, 9, 11]
```

**Cloning**
Changes made to the original list doesn't make changes to the other list.
```python title:Example
A = [10, 5, 9, 11]
B = A[:]

A[0] = 12

print(B)

Output: [10, 5, 9, 11]
```
