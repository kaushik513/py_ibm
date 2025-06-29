
**try...except...else...finally statement**

```python title=Example/Syntax
try:
	getfile=open("myfile", "r")
	getfile.write("My file for exception handling")
except IOError:
	print("Unable to open or read the data in the file.")
else:
	print("The file was written successfully.")
finally:
	getfile.close()
	print("The file is now closed.")
```

Here, the `try` statements are the ones that are attempted to be carried out. If there is an error, the `except` statement comes into the play, which can have the type of error specified. 
If the `except` statement gets skipped over i.e., there was no error (or at least no specified one) then we can add an `else` statement to show that it was successful.
Generally, it isn't good practice to put an `except` statement without specifying the type of error because then you could be debugging for hours trying to figure out what error caused that statement to occur and where.
The `finally` statement is run regardless of the end result. In this case, the file is closed regardless of whether there was an error or not.

# Examples of exceptions/errors

- **ZeroDivisionError:** When a number is made to divide by zero.
- **Value Error:** Occurs when an inappropriate value is used in the code. 
	Example: Trying to convert a non-numeric string to an integer - `num - int("abc")`
	This would raise a ValueError.
- **FileNotFoundError:** When an attempt is made to access a file that doesn't exist.
- **IndexError:** When an index is used to access an element in a list that is outside the valid index range.
- **KeyError:** When an attempt is made to access a non-existent key in a dictionary.
- **TypeError:** When an object is used in an incompatible manner. 
	Example: Trying to concatenate a string and an integer - `result = "hello" + 5`
- **AttributeError:** When an attribute or method is accessed to an object that doesn't possess that specific attribute or method.
	Example: `text = "hello"` `text.append("world")`. Here, text is a string and append is used for lists, not strings, which would raise an AttributeError.
- **ImportError:** When an attempt is made to import a module that is unavailable/non-existent.