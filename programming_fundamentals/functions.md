# Python's built-in functions

- `len()` - returns length of a type sequence like a dictionary, list, set, tuple, string etc.
- `sum()` - takes the elements and returns the sum of all of them
- `sorted(list_name)` - returns a sorted list
- `sort(list_name)` - sorts the list you input as its argument instead of returning one

# User defined functions

So the format in C was something like
```c
int function(int var, char c)
{
.....
return another_variable;
}
```
which is defined outside the main function. 

But in python it's like 
```python
def function(input):
	output = input + 1
	return output
```
You don't gotta do allat defining outside the main function stuff

**If your function has no return statement** - 
```python
def MJ():
	print('Michael Jackson')
```

**Note:** Python doesn't allow to a function to not have any body so you could just put "pass" in there to fulfill the purpose of it being empty inside (like me). 

## Adding documentation to functions

Encase them in triple quotes
```python
def add1(a):
	"""
	add 1 to a
	"""
	b=a+1
	return b
```

## Variadic Parameters

It means that you can give a variable number of parameters to a function.
```python title=Example
def ArtistNames(*names):
	for name in names:
	print(name)
```

## Scope of a Variable

If a variable is defined outside a function then it has global scope. If it's defined inside then its scope is limited to that function itself.
```python title=Example
def Thriller():
	date = 1982
	return(date)

date=2017

print(Thriller()) 
print(date)
```
``` title=Output
1982
2017
```
When calling `Thriller()`, the date being used has local scope so we're printing its local value but when printing it normally, we're printing its global value.

**However,** if we use the keyword `global` before defining a variable in the function, that variable will have global scope.