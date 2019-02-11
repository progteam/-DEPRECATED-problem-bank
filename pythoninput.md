Two main methods for taking in input with Python 3:
- [input](https://github.com/progteam/problem-bank/blob/master/pythoninput.md#input)
- [sys.stdin](https://github.com/progteam/problem-bank/blob/master/pythoninput.md#sysstdin)
***

```python
## input()
```

Returns line read from input after being converted to a string

Optionally can be provided an argument that is printed to standard ouput

``` python
>>> a = input("Enter a number\n")
Enter a number
5
>>> print(a)
'5'
```

If input is desired in some type other than string, you can convert it like so:

```python
a = int(input())
b = float(input())
```

[input() Documentation](https://docs.python.org/3/library/functions.html#input)

In some cases it may be useful to separate the line of input based on a delimiter 
such as ' ' or ','

In Python we can do that with:

```python
split()
```

Returns a list of words in the strings, separated by the provided delimter. If argument is left blank then
separates on spaces.

```python
>>> groceries = "apples, bananas, milk, eggs"
>>> grocery_list = groceries.split(',')
>>> print(grocery_list)
['apples', 'bananas', 'milk', 'eggs']
```

[split() Documentation](https://docs.python.org/3/library/stdtypes.html#str.split)

***
# sys.stdin
```python
from sys import stdin
```
Can be used to iterate over lines of input, such as test cases for Kattis problems

However, trailing newlines are not stripped with this method, unlike input(). 

```python
for line in stdin:
    print(line)
```

[sys Documentation](https://docs.python.org/3/library/sys.html)
