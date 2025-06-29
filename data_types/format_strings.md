# Printing variables
To print variables in a print statement, %d works but the variable name within curly brackets is better.

```python title:Example 
age = 30
name = "John"

print(f"My name is {name} and I am {age} years old.")
```

``` title:Output
My name is John and I am 30 years old.
```

Also, print something right after a string as so:

```python 
str = "sentence, lololol"
print("This is my sentence:", str)
```

``` title:Output
This is my sentence: sentence, lololol
```

And print raw strings by doing `print(r' ')`. This will take characters like `\n` as literally "\n".
## Alternatives

### str.format()

```python 
name = "John"
age = 30

print("My name is {} and I am {} years old.".format(name,age))
```

### % operator

```python
name = "John"
age = 30

print("My name is %s and I am %d years old."%(name,age))
```

`%(name,age)` is called a "Tuple".