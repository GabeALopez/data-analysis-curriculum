## Lists

Lists are a general destructure the hold some kind of data. This data can be ints, strings, float, etc. The nice attribute that lists have is that lists can many data differing data type in one list. In coding languages, like c and c++, an array can only hold one data type, but this is not the case for python. This is a blessing and a curse, as lists make it convenient for programers to add items to general data structure but it is a curse as in larger projects this feature can make your program inherently slow. The reasoning for this slowness is that the interpreter in python has to take time to discern which data type is which in the list. As in C and c++ the data type is already determined thus no time is needed to discern the data type.

Here are some simple examples of using lists in python:

Example with a simple for loop. Loops will be covered later but know that each item in the list is being printed out to the console:

```python
my_list = ['Hello', 'World', 2024]

for item in my_list:
   print(item)
```

Instantiates, adds a value, and then prints the full list:

```python
my_list = ['Hello', 'World', 2024]

my_list.append('My Value')

print(my_list)
```

Creates two lists and adds the second list to the first one:

```python
my_list = ['Hello', 'World', 2024]
my_new_list = [2024, 'World', 'Hello']

my_list.extend(my_new_list)
```

Lists are a nice way to hold general data but they do not give the functionally that can happen with arrays. In the next section, we are going to talk about numpy arrays. Numpy arrays help to try to provide this type of functionally. Although not 100% an array, however they are closest one have arrays in python.