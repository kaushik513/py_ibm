An object is an instance of a particular type.

Example: Everytime we create an integer, we're creating an instance of the type "int". Or, we're creating an object of the type int. If we're creating a list, we're creating an object of the type "list". 

To find type of an object - `type()`.

### Classes

```python title=Example
class Circle(object):  -> Class definition

	def __init__(self, radius, colour):
		self.radius = radius
		self.colour = colour
```

- `__init__` is a constructor. It tells python you're making a new class.
- `self` here is an instance of the class - "self parameter"
- `radius, color` are parameters of the class.
- We can also add default values for the parameters by initializing it in the parameters themselves like so - `def __init__(self, radius=5, colour="pink"):`

### Defining an object of a class

```python title=Example
C1 = Circle(10, "red")
```

This creates an object `C1` of the class `Circle` with its parameters as 10 and red corresponding to its radius and colour from the previous example.

### Creating a method inside a class

Building off of previous code:

```python title=Example
class Circle(object):  -> Class definition

	def __init__(self, radius, colour):
		self.radius = radius
		self.colour = colour
	def add_radius(self, radius)
		self.radius = self.radius + r
```

Using this method:

```python title=Example
C1 = Circle(2, "red")
C1.add_radius(5)
```

This changes the radius to 2+5 = 7.