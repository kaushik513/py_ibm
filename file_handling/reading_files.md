# File Object

```python 
file1 = open("/resources/data/Example1.txt", "r")
```

Here, open is the function that sets file1 as the object for the file specified in the first parameter of the function. "r" is the mode in which we are opening the file. Here, we are opening in read mode. There is also write mode (w) and append mode (a).

Now we can use file1 to get information about the file. 

For example, we can use `.name` to get the name of the file, `.mode` to find out what mode the object is in. 

We should always close the file object using the method `.close` because this frees up resources and ensures consistency across different python versions. 

However, since this can get tedious, we can instead use the "with" function.

```python
with open("Example.txt", "r") as file1:
    file_stuff = file1.read()
    print(file_stuff)

print(file1.closed)
print(file_stuff)
```

This code runs everything in the indented block and then closes the file.

`.read` stores the values of the file in the variable `file_stuff` as a string.

`file1.closed` would show whether the file is closed or not.

# Reading 

To store the information of the file as separate elements under a variable, we can use `.readline()` instead of `.read()`. Note that `.readline()` can only read one line at a time. Hence, each time it's used on a file it'll read the next line. 

The argument to `.read()` and `.readline()` represents the number of elements to be read and stored. For example if we used `.readline(4)`, it would read the first 4 characters of that line. The difference is that `readline` cannot go past the line it's reading, but `read` can. 

`.readlines()` will read the entire file and store each line as separate elements in the provided variable.