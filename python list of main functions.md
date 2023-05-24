
1. index():
```python
text = "Hello, World!"
index = text.index("W")
print(index)  # Output: 7
```

2. split():
```python
text = "Hello, World!"
split_text = text.split(", ")
print(split_text)  # Output: ['Hello', 'World!']
```

3. replace():
```python
text = "Hello, World!"
new_text = text.replace("Hello", "Hi")
print(new_text)  # Output: Hi, World!
```

4. sorted():
```python
numbers = [4, 2, 6, 1, 3]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # Output: [1, 2, 3, 4, 6]
```

5. strip():
```python
text = "   Hello, World!   "
stripped_text = text.strip()
print(stripped_text)  # Output: "Hello, World!"
```

6. join():
```python
words = ["Hello", "World!"]
joined_text = ", ".join(words)
print(joined_text)  # Output: "Hello, World!"
```

7. * (asterisk):
```python
numbers = [1, 2, 3]
expanded_numbers = [*numbers]
print(expanded_numbers)  # Output: [1, 2, 3]
```

8. np.unique():
```python
import numpy as np

numbers = [1, 2, 2, 3, 3, 3]
unique_numbers = np.unique(numbers)
print(unique_numbers)  # Output: [1 2 3]
```

9. set():
```python
x = {'hetero', 'set'}
print(x)  # Output: {'set', 'hetero'}
```

10. np.argsort():
```python
import numpy as np

arr = np.array([3, 1, 4, 2])
sorted_indices = np.argsort(arr)
print(sorted_indices)  # Output: [1 3 0 2]
```

11. np.bincount():
```python
import numpy as np

arr = np.array([0, 1, 1, 3, 2, 1, 2])
counts = np.bincount(arr)
print(counts)  # Output: [1 3 2 1]
```

12. np.where():
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
condition = (arr > 3)
result = np.where(condition, arr, '-')
print(result)  # Output: ['-' '-' '-' 4 5]
```

13. shape:
```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
shape = arr.shape
print(shape)  # Output: (2, 3)
```

14. repeat():
```python
import numpy as np

arr = np.array([1, 2, 3])
repeated_arr = np.repeat(arr, 2)
print(repeated_arr)  # Output: [1 1 2 2 3 3]
```

15. reshape():
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6])
reshaped_arr = np.reshape(arr, (2, 3))
print(reshaped_arr)  # Output: [[1 2 3]
                     #          [

4 5 6]]
```

16. item:
```python
import numpy as np

arr = np.array([1, 2, 3])
first_item = arr.item()
print(first_item)  # Output: 1
```

17. ndim:
```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
dimensions = arr.ndim
print(dimensions)  # Output: 2
```

18. diagonal:
```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
diagonal_elements = arr.diagonal()
print(diagonal_elements)  # Output: [1 5 9]
```

19. transpose:
```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
transposed_arr = np.transpose(arr)
print(transposed_arr)  # Output: [[1 4]
                       #          [2 5]
                       #          [3 6]]
```

20. sum:
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
total = np.sum(arr)
print(total)  # Output: 15
```

21. var:
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
variance = np.var(arr)
print(variance)  # Output: 2.0
```

22. np.nditer():
```python
import numpy as np

arr = np.array([[1, 2], [3, 4]])
for x in np.nditer(arr):
    print(x, end=' ')
# Output: 1 2 3 4
```

23. np.matrix():
```python
import numpy as np

x = np.array([[1, 2], [3, 4]])
matrix = np.matrix(x)
print(matrix)
# Output:
# [[1 2]
#  [3 4]]
```

24. dot/matmul:
```python
import numpy as np

a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])
dot_product = np.dot(a, b)
print(dot_product)
# Output:
# [[19 22]
#  [43 50]]
```

25. pd.DataFrame():
```python
import pandas as pd

data = {'Name': ['John', 'Alice', 'Bob'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)
print(df)
# Output:
#    Name  Age
# 0  John   25
# 1  Alice  30
# 2  Bob    35
```

26. values:
```python
import pandas as pd

data = {'Name': ['John', 'Alice', 'Bob'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)
values = df.values
print(values)
# Output:
# [['John' 25]
#  ['Alice' 30]
#  ['Bob' 35]]
```

27. keys:
```python
import pandas as pd

data = {'Name': ['John', 'Alice', 'Bob'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)
keys = df.keys()
print(keys)
# Output: Index(['

Name', 'Age'], dtype='object')
```

28. items:
```python
import pandas as pd

data = {'Name': ['John', 'Alice', 'Bob'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)
items = df.items()
for key, value in items:
    print(key, value)
# Output:
# ('Name', 0    John
#           1    Alice
#           2    Bob
#           Name: Name, dtype: object)
# ('Age', 0    25
#          1    30
#          2    35
#          Name: Age, dtype: int64)
```

29. lambda:
```python
add_numbers = lambda x, y: x + y
result = add_numbers(5, 3)
print(result)  # Output: 8
```

30. enumerate():
```python
fruits = ['apple', 'banana', 'cherry']
for index, fruit in enumerate(fruits):
    print(index, fruit)
# Output:
# 0 apple
# 1 banana
# 2 cherry
```

31. while:
```python
counter = 1
while counter <= 5:
    print("Counter:", counter)
    counter += 1
# Output:
# Counter: 1
# Counter: 2
# Counter: 3
# Counter: 4
# Counter: 5
```

32. append():
```python
numbers = [1, 2, 3]
numbers.append(4)
print(numbers)  # Output: [1, 2, 3, 4]
```

33. clear():
```python
numbers = [1, 2, 3]
numbers.clear()
print(numbers)  # Output: []
```

34. pop():
```python
numbers = [1, 2, 3]
popped_number = numbers.pop()
print(popped_number)  # Output: 3
```

35. update():
```python
my_dict = {'name': 'John', 'age': 25}
my_dict.update({'age': 30, 'city': 'New York'})
print(my_dict)  # Output: {'name': 'John', 'age': 30, 'city': 'New York'}
```

36. def:
```python
def greet(name):
    print("Hello, " + name + "!")
    
greet("Alice")  # Output: Hello, Alice!
```

37. class:
```python
class Person:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        print("Hello, " + self.name + "!")
        
person = Person("John")
person.greet()  # Output: Hello, John!
```

38. __init__():
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def display_info(self):
        print("Name:", self.name)
        print("Age:", self.age)
        
person = Person("Alice", 30)
person.display_info()
# Output:
# Name: Alice
# Age: 30
```

39. self:
```python
class Circle:
    def __init__(self, radius):
        self.radius = radius
        
    def calculate_area(self):
        area = 3.14 * self.radius ** 2
        return area
    
circle = Circle(5)
area = circle.calculate_area()
print(area)  # Output: 78.5
```

40. `dict()`: Create an empty dictionary.
```python
my_dict = dict()
print(my_dict)  # Output: {}
```

41. `clear()`: Remove all key-value pairs from a dictionary.
```python
my_dict = {'name': 'John', 'age': 25}
my_dict.clear()
print(my_dict)  # Output: {}
```

42. `get()`: Retrieve the value associated with a specific key from a dictionary.
```python
my_dict = {'name': 'John', 'age': 25}
name = my_dict.get('name')
print(name)  # Output: John
```

43. `items()`: Return a list of key-value pairs in a dictionary.
```python
my_dict = {'name': 'John', 'age': 25}
items = my_dict.items()
print(items)  # Output: [('name', 'John'), ('age', 25)]
```

44. `keys()`: Return a list of keys in a dictionary.
```python
my_dict = {'name': 'John', 'age': 25}
keys = my_dict.keys()
print(keys)  # Output: ['name', 'age']
```

45. `values()`: Return a list of values in a dictionary.
```python
my_dict = {'name': 'John', 'age': 25}
values = my_dict.values()
print(values)  # Output: ['John', 25]
```

46. `pop()`: Remove a key-value pair from a dictionary and return its value.
```python
my_dict = {'name': 'John', 'age': 25}
age = my_dict.pop('age')
print(age)  # Output: 25
print(my_dict)  # Output: {'name': 'John'}
```

47. `update()`: Update a dictionary with the key-value pairs from another dictionary.
```python
my_dict = {'name': 'John'}
new_data = {'age': 25, 'city': 'New York'}
my_dict.update(new_data)
print(my_dict)  # Output: {'name': 'John', 'age': 25, 'city': 'New York'}
```
