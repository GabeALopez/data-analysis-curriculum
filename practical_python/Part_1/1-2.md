## Dictionaries

Dictionaries, what are they and what can they be used for? A dictionary is another type of data structure where it uses a key value pair structure. For example, every employee has an ID number associated with a name. The ID number is the key and the value is the employee name. So then why use dictionaries over a list for instance. Well more broadly speaking when programming you can put any data you want into a list or into a dictionary but sometimes the data you get makes more sense to be put into a key value pair system instead of a list.

So let's take the following two example data sets that are in csv format:

**Example 1:**
```csv
Product,Price
Apple,0.50
Banana,0.30
Orange,0.80
Mango,1.50
```

**Example 2:**
```csv
Item
Apples
Bananas
Oranges
Milk
Eggs
Bread
```

In example 1, there is a clear associated with the product and it's price. While with example 2 there is no clear association with an items as they are just **listed**. But as data gets more complicated the line between what should be put into a list and what shouldn't can get a bit blurry. So it's starts become up to the programmer to decide what is best based on the situation. But enough on that let's get into how to create a dictionary. In order to create an empty dictionary are you going to write the following code:

```python
my_dict = {}
```

This creates an empty dictionary. In order to create one with data you can write similar to the following: 

```python
my_dict = {1111: 'Joel', 2222: 'Andy', 3333: 'Karen'}
```

You might start to notice the syntax of the key value pairs. The general syntax is: key: value. This is format of which you user to add to the dictionary as well. So let's try to add another entry into this dictionary:

```python
my_dict = {1111: 'Joel', 2222: 'Andy', 3333: 'Karen'}
my_dict[4444] = 'Josh'
```

You will notice this is not like a list you use an append function to add an entry. What you do instead is use a new ID, or key, and put it brackets with the dictionary you want to add in front of the dictionary name. After that you make it equal to a value. If you ever look at data in a JSON format you will notice the similarity to python dictionaries they have.

### Side Tangent: Dictionaries and Maps

If you ever look into code like c or c++ you will notice that these two coding languages have something similar to python dictionaries. In c and c++ they are called maps and work very much the same way. They have a key which points to a value and may have heard the term "hashmaps" where map may be used in sorting. Of course these are not one to one as c and c++ are languages that work closely with the hardware of a system while python is like not in that it is a scripting language. I encourage you to look into the difference between and system language and a scripting language on your own time with google. It is a very interesting rabbit hole in of itself.