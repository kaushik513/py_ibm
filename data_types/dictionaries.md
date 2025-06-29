Denoted by curly brackets, anchored by keys in a list/tuple.

# Keys and Values

Keys are sually characters, act as addresses. Similar to elements in a list - they contain information.

The values in a key are followed by a colon.
Key and value pairs are separated by commas.

Print all the keys in a dictionary - `DICT.keys()`
Print all the values in a dictionary - `DICT.values()`

# Entries

A new entry to the dictionary can be made by doing something like `DICT['Key1']='201'` and an entry can be deleted by doing something like `del(DICT['Key1'])`.

Verify if an entry is in a dictionary - `'Key1' in DICT`. "in" being a function that checks whether there's an entry with the specified key "Key1" in the dictionary "DICT".

```python title=Example
dict = {"Sales":21, "Customers":25, "Profit Margin":1000}

dict["Losses"]="2008"
del(dict['Sales'])

print(dict)
print("Sales" in dict)
```
```python title=Output
{'Customers': 25, 'Profit Margin': 1000, 'Losses': '2008'}
False
```