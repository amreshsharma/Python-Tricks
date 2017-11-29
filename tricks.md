## Python-Tricks
The following Python tricks I find pretty useful in my daily Python development work. I will add more small pyton code/tricks when i
come acroos. Readers are encouraged to add new tricks.
###  I tried my best to make the examples clear

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
