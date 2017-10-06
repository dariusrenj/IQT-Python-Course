# Mapping Types

## Dictionary

Dictionaries **are mutable **objects and consist of key-value mappings. \(ex: {key: ‘value’, key: ‘value’}  \). They are initiialized using the curly-brackets {}. Dictionaries are not ordered and support all value types.

```py
>>> my_dict = {} # create empty dictionary​
>>> my_dict['one'] = 1 # add item to the dictionary​
>>> my_dict = {'one' : 1} #create a dictionary with an item​
>>> my_dict​
{'one': 1}​
​
>>> my_dict['two'] = 2 # add item to the dictionary​
>>> my_dict​
{'one': 1, 'two': 2}​
```

### Common Dict Operations

```py
>>> d[i] = y # value of I is replaced by y​
>>> d.clear() # removes all items​
>>> d.copy() # creates a shallow copy of dict_x​
>>> d.fromkeys(S[,v]) # new dict from key, values​
>>> d.get(k[,v]) # returns dict_x[k] or v​
>>> d.items() # list of (key,value) pairs​
>>> d.iteritems() # iterator over (key,value) items​
>>> d.iterkeys() # iterator over keys of d​
>>> d.itervalues() # iterator over values of d​
>>> d.pop(k[,v]) # remove/return specified (key,value)​
>>> d.popitem() # remove/return arbitrary (key,value)​
>>> d.update(E, **F) # update d with (key,values) from E​
​
```

# Set and Frozenset

A set is an unordered collection of unique elements. Sets **are muteable **but contain no hash value-- so they can't be used as dict keys or as an element of another set.

```py
>>> new_set = set() # create an empty set​
>>> new_set = {0, 1, 1, 1, 2, 3, 4} ​
>>> new_set​
{0, 1, 2, 3, 4}​

>>> new_set.add(5) # Add new key to set​
>>> new_set​
{0, 1, 2, 3, 4, 5}​

>>> x_set = set("This is a set")​
>>> x_set​
{'s', 't', 'e', 'h', 'I', ' ', 'T', 'a'}​

>>> another_set = set(['Ford', 'Chevy', 'Dodge', 105, 555])​
{'Chevy', 105, 155, 'Ford', 'Dodge'} # many ways to create set​
```



### Frozenset

Frozensets are identical to sets aside from the fact that they **are immutable**. Since frozensets are immutable, they are hashable as well. So they can be used as a dict key or element of another set.

```py
>>> new_set = frozenset([1,2,2,2,3,4])# create an frozenset​
>>> new_set​
frozenset({1, 2, 3, 4})​
>>> new_set.add(5)​
.......AttributeError: ‘frozenset’ object has no attribute ‘add’​
# Doesn't work since Frozenset is immutable

# Many… many ways to create frozenset as well. ​
​
```



### Common Set Operations

Some do not apply to Frozenset. 

```py
>>> s.issubset(t) # test if elements in s are in t​
>>> s.issuperset(t) # test if elements in t are in s​
>>> s.union(t) # new set with elements of t and s​
>>> s.intersection(t) # new set with common elements​
>>> s.difference(t) # new set with elements in s but not t​
>>> s.symmetric_difference # xor​
>>> s.copy() # new shallow copy of s​
>>> s.update(t) # return set s with elements from t​
>>> s.intersection_update(t)​
>>> s.difference_update(t)​
>>> s.symmetric_difference_update(t)​
>>> s.add(x) # add x to set s​
>>> s.remove(x) # remove x from set s​
>>> s.discard(x) # remove x from set s if present​
>>> s.pop() # remove arbitrary item​
>>> s.clear() #remove all elements from set a​
```


