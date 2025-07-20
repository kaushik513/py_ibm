# Write mode

```python
file1 = open("/resources/data/Example.txt", "w")
```

OR

```python
with open("/resources/data/Example.txt") as file1:
    file1.write("This is line A\n")
    file1.write("This is line B\n")
```
OR
```python
Lines = ["This line A\n", "This is line B\n", "This is line C\n"]

for line in Lines:
    file1.write(line)
```

# Copying one file into another

First, we read the file we want to copy and then open the file we want to copy it into in write mode and then write it.

```python
with open("/resources/data/Example1.txt", "r") as readfile:
    with open("/resources/data/Example2.txt", "w") as writefile:
        for line in readfile:
            writefile.write(line)
```

**Note:** Setting a file to write mode overwrites all existing data in the file. We can instead open the file in *append* mode to add to the existing data.

# Append mode

```python
with open('/Example.txt', 'w') as writefile:
    writefile.write("Sample text\n")

with open('/Example.txt', 'a') as appendfile:
    appendfile.write("This is line C\n")
    appendfile.write("This is line D\n")
    appendfile.write("This is line E\n")

with open('/Example.txt', 'r') as readfile:
    print(readfile.read())
```

The output of this would be:

```
Sample text
This is line C
This is line D
This is line E
```

# A+ mode

Since switching modes each time is inefficient, one can use `a+` mode. However, something to understand about append is that it takes you to the bottom part of the file. Something like moving the cursor to the bottom. 

So if you try to read the file then it'll read nothing cause the cursor is at the bottom. So, in order to read the file from a desired location, we can use `.seek(offset,from)` which changes the position by _offset_ with respect to _from_.

```python
with open('/Example2.txt', 'a+') as testwritefile:
    print("Initial Location: {}".format(testwritefile.tell()))
    
    testwritefile.seek(0,0) # move 0 bytes from beginning.
    
    print("\nNew Location : {}".format(testwritefile.tell()))
    
    data = testwritefile.read()
    print(data)
    print("Location after read: {}".format(testwritefile.tell()) )
```

Output:

```
Initial Location: 70

New Location : 0
Overwrite
This is line C
This is line D
This is line E
This is line E

Location after read: 70
```

# Additional modes

Both `w+` and `r+` allow access to read and write methods but `w+` overwrites all existing data upon opening a file.

The `.truncate()` method deletes everything after a certain point in the file.