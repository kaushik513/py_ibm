
They're a type of collection like lists and tuples but they are unordered which means that they don't record the position of the elements.

They can only have unique elements.

# Defining a set

Use curly brackets. If you define multiple of the same values the resultant set will simply take them out.

A list can be converted into a set by using `set(list)` - typecasting

```python title=Example
album_list = ["Dark Side of the Moon", "Thriller", "Thriller", 1982]
album_set = set(album_list)

album_set
```
```python title=Output
{'Dark Side of the Moon', 'Thriller', 1982}
```

# Set Operations

- Adding an item - `set_name.add('Element')`

- Removing an item - `set_name.remove('Element')`

- Verifying if an item is in a set - `'Element' in set_name`. Returns True or False.

- Intersection of two sets can be taken by using the '&' operator - `set1 & set2`

- You can find all the elements only in one set but not the other by doing the difference operator - `set1.difference(set2)` or `set2.difference(set1)`

- Union of two sets (which contains all items from both sets) - `set1.union(set2)`

- Checking if a set is a subset - `set2.issubset(set_1)`. Returns True or False.
- Checking if a set is a superset - `set2.issuperset(set1)`


