
# Range

**Syntax:**

`range(N)`
	Generates a list from 0 to N-1

`range(N1,N2)`
	Generates a list from N1 to N2-1

Basically goes from i=0 to i< N or i=N1 to i< N2
# For loops

**Syntax:**
```python title=Example
for i in range(0,5):
	value[i]="zero"
```

Can also just do it without a loop counter altogether:
```python title=Example
squares = ["yellow", "red", "blue"]

for square in squares:
	square
```

Here, the "square" in `for square in squares:` is the placeholder that each value of the list gets assigned to.

**Enumerate function** - `enumerate(list)`
It returns pairs of indices and corresponding values.

```python title=Example
fruits = ["banana", "apple", "orange"]

for i,fruit in enumerate(fruits):
	print(i, fruit)
```

```python title=Output
0 banana
1 apple
2 orange
```

The `i,fruit` specifies which variable will contain the indices and which will contain the corresponding value.

# While loop

```python title=Example
squares = ['orange', 'orange', 'yellow', 'blue']

newsquares=[]
i=0

while(squares[i]=='orange')
	newsquares.append(squares[i])
	i+=1
```