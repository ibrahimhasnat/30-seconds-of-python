---
title: enumerate
tags: function, python
expertise: intermediate
firstSeen: 2022-09-14T06:34:17+00:00
---

`enumerate()` is built-in python function. It sets a counter to an iterable. We can treat it as a unique key for each element in the iterable.

It takes two parameters.

- The first one is any iterable object
- And the second one is starting value of the counter  __(default 0)__

But the second parameter is optional.


```python
lst = ['One', 'Two', 'Three']
print(enumerate(lst))

res = list(enumerate(lst)) # Converted from object to list

print(res) # [(0, 'One'), (1, 'Two'), (2, 'Three')]
```

Let's see an example by defining starting value of the counter. 

```python
lst = ['One', 'Two', 'Three', 'Four', 'Five']

print(list(enumerate(lst, start=5))) # [(6, 'One'), (7, 'Two'), (8, 'Three'), (9, 'Four'), (10, 'Five')]
```

If we don't define the starting value, we can use it as an __index-value__ pair. As we all know, the index starts from __0__.

```python
lst = ['One', 'Two', 'Three', 'Four', 'Five']

for i, val in enumerate(lst):
  print(f'The index of {val} is {i}')

# Output
# The index of One is 0
# The index of Two is 1
# The index of Three is 2
# The index of Four is 3
# The index of Five is 4
```

The way we fetched `i` and `val` from each iteration is called destructuring. __Ex:__ `i, val = (0, 'One')`.