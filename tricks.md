## Python-Tricks
The following Python tricks I find pretty useful in my daily Python development work. I will add more small pyton code/tricks when i
come acroos. Readers are encouraged to add new tricks.

### (1) How to Swap two numbers
```
>>> x = 1
>>> y = 2
>>> x, y = y, x
>>> x
2
>>> y
1
```

### (2) Unpacking for swapping variables
```
>>> a, b = 1, 2
>>> a, b = b, a
>>> a, b
(2, 1)
```

### (3) Negative indexing
```
>>> a = [0, 3, 6, 7, 4, 5, 9, 7, 8, 2, 1]
>>> a[-1]
1
>>> a[-3]
8
```

### (4) List slices (a[start:end])
```
>>> a = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
>>> a[2:8]
[2, 3, 4, 5, 6, 7]
```

### (5) Map - Example: Square all the number in a list in one line
```
>>> items = [1, 2, 3, 4, 5]
>>> squared = list(map(lambda x: x**2, items))
print squared
 
[1, 4, 9, 16, 25]
```

### (6) Generate a unique random ID
```
>>> import uuid
>>> print uuid.uuid4()
976c7afb-9e82-y65e-9316-8eba94762085
```

### (7) Inverting a dictionary using zip
```
>>> m = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
>>> m.items()
[('a', 1), ('c', 3), ('b', 2), ('d', 4)]
>>> zip(m.values(), m.keys())
[(1, 'a'), (3, 'c'), (2, 'b'), (4, 'd')]
>>> mi = dict(zip(m.values(), m.keys()))
>>> mi
{1: 'a', 2: 'b', 3: 'c', 4: 'd'}
```

### (8) Inverting a dictionary using a dictionary comprehension
```
>>> m = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
>>> m
{'d': 4, 'a': 1, 'b': 2, 'c': 3}
>>> {v: k for k, v in m.items()}
{1: 'a', 2: 'b', 3: 'c', 4: 'd'}
```

### (9) Reversing a string in Python
```
>>> a = "ilikepython"
>>> print "Reverse is",a[::-1]
Reverse is nohtypekili
```

### (10) Functions like sum() accept generators / use the right variable type

```
sum = 0
for i in range(1300):
    if i % 3 == 0 or i % 5 == 0:
        sum += i
print(sum)
```
This could be done shorter and efficiently: 
```
>>> sum(i for i in range(1300) if i % 3 == 0 or i % 5 == 0)
394118
```

### (11) tricks with Zip

Transposing a matrix:
```
>>> l = [[1, 2, 3], [4, 5, 6]]
>>> zip(*l)
[(1, 4), (2, 5), (3, 6)]
```
Dividing a list into groups of n:
```
>>> l = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5, 8]
>>> zip(*[iter(l)] * 3)
[(3, 1, 4), (1, 5, 9), (2, 6, 5), (3, 5, 8)]
```

Note:  I tried my best to make the examples clear
