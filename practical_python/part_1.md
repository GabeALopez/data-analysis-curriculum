# All the Basics

Below are some topics that are practical when working with python and, by extension, data analysis:

- Lists
- Numpy Arrays
- Dictionaries
- If statements
- Opening and Closing Files
- Loops
- Functions
- Try Except
- Debuggers
- How to look things up

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

## Numpy Arrays

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

## Opening and Closing Files

## Loops

These are another general data structure that you can take with you with most programming languages. Loops are just as they sound. Things that loop! But it a little more complicated than just that. Loops are a data structure that loop anything within it's bounds. There a few types of loops: while, for, and do while. Python really only has while and for loops but do while can implemented just in not in the traditional sense. In the modern day we also have a fourth type of loop called a foreach loop, but this will be covered in a bit more detail later. But first let's look at simple python examples of each type of loop. 

**While Loop**

```python
"""
   Important to note that to signify things that go in a loop you must indent your 
   statements underneath the while loop as well as put a colon (:) next to the while 
   statement to indicate that something is supposed to underneath it.

   I say this vaguely on purpose as this applied to functions to, which will covered in 
   the function section.
"""
# Prints a simple count while increasing it
count = 0
while(count < 5):
   print(count)
   count += 1

```

So the while loop above just takes the count we declared above and prints it out. Once it prints out the count it increases the count. This will keep going until the condition is satisfied. If is is it will break out of the loop. Pretty nice.

**For Loop**

```python
# 6 is not inclusive here when using the range function
for count in range(1, 6):
   print(count)

```

This loop introduces an inbuilt function called the range function. A function will, again, be explained later but for now think of it as a container that has code in it that can be called up on multiple times to reuse said code. This range function serves to provide the loop the number of times it will iterate and print the count var. But you might be asking yourself why was "count" declared above the while loop but not really in the same way that "count" is in the for loop. The reason for this is that in the syntax of python and, by extension foreach loops, an almost temp variable is created for the instance that the loop is active. That being the case, the "count" variable (var for short) will only exist until the for loop ends. Now this is pretty handy when you start create more complicated pieces of code where you need just a var for the instance of the loop, which is not the same as in the while loop example.

It is important to note that the var in the for loop doesn't have to have the name "count" and can be named anything the user want really. Just make sure to be careful with naming the to be careful with naming the var. If you name a var the same as a previously made var or a special keyboard like "break" (Don't worry about what this keyword is just yet, for now just know it is a special keyword in python) it can cause problems in your code. Possibly even overwriting data in those previously made vars or keywords. There are some nuances in the naming scheme and with everything in life there are exceptions to the rules. But for a person starting out I would just avoid naming new vars with the same name as previously made ones or special keywords like the plague to avoid mistakes.

### Do While and Foreach Loops

Now I am going to take you out of python for a little bit and into the the world of c and c++. Don't worry this is not going to be complicated. Loop from these languages will be shown but you will be able to understand them. 

But without further let's introduce the two other loops I talked about. Let's start with do while loops. A do while is a loop that has a starting block of code that executes first before the main loop starts. The loop will continue to loop what is in the block of code until a condition is met.

Here is an example from c++:

```c++
#include <iostream>

int main() {

   int count = 1;

   do {
      //statement to print count to standard output
      std::cout << count << std::endl;
      //increase count by 1
      count++;
   } while (count <= 5);

   return 0;
}
```

The loop first executes everything in the do block and the count will be increased until the condition is met.

This is what this loop would look like in python:

```python
count = 0

while True:
   print(f"Count is {count}")
   count += 1
    
   if count >= 5:
      break

```

As you can see the loop has similar characteristics to the c++ code where something is executed first and then the condition is checked.

Now the other loop is the foreach loop. Now in python, it's for loop is technically a foreach statement and not a true for loop. 

A real for loop in c++ would look like this:

```c++
#include <iostream>

int main() {
   for (int count = 1; count <= 5; ++count) {
      std::cout << count << std::endl;
   }

   return 0;
}

```

Where as a c++ foreach loop would look like this:

```c++
#include <iostream>
#include <vector>

int main() {
   //Kinda like a list in python but is restricted to a data type
   //This is a generalization to help you to understand. It is not really what it is
   std::vector<int> numbers = {1, 2, 3, 4, 5};

   // Range-based for loop
   for (int number : numbers) {
      std::cout << number << std::endl;
   }

   return 0;
}

```

You can see the similarity to the python for loops with the foreach statement rather than the pure for loop. In the foreach loop it is read like this: foreach number in the vector of int numbers print out the number. This is similarly read in python.

### Special Keywords for Loops

In loops there are two special keywords: break and continue with each having a role to play in running loops. The first keyword I am going to look at is "continue". "continue" is just as the sounds, it continues a loop. An example of using can be seen here where the previous for loop was written with a "continue" keyword:

```python
for count in range(1, 6):
   print(count)

   if count % 2 == 0:
      continue

```

In the for loop the code will continue anytime the value of count is divisible by 2. This being the case no odd numbers will print to the console. Pretty simple right?

Now the other keyword is "break". "Break" is a keyword that is might one would think, it breaks a loop. Here is another example rewriting the same code:

```python
for count in range(1, 6):
   print(count)

   if count % 2 == 0:
      break
```

Now this code will only print 2 and nothing else as the first number in count that is even is 2. Because of this the loop is broken is exits out.

Now this begs the question. Why would I want to use these keywords? What's the point? Well the importance of these keywords is that is make certain operations run just the little bit faster depending on what you are doing. Let's say for instance you need to loop through a gigantic log of user logon events and want to do a operation based on a list of users. How are you supposed to work on the specific user with that user's logs? It can be a little annoying as you don't want to loop through the entire log just to look for one user and you are using processing power just do that. Now that might sound confusion so let's illustrate this with sample data.

Here are my mock sign in logs for example:

```python
2024-07-09 08:15:34 - User: alice - Sign-in successful
2024-07-09 08:17:45 - User: bob - Sign-in successful
2024-07-09 08:18:56 - User: charlie - Sign-in failed (incorrect password)
2024-07-09 08:20:12 - User: charlie - Sign-in successful
2024-07-09 09:30:54 - User: alice - Sign-in failed (account locked)
2024-07-09 09:32:01 - User: alice - Sign-in successful
2024-07-09 09:45:21 - User: bob - Sign-in successful
2024-07-09 10:05:37 - User: charlie - Sign-in successful
2024-07-09 10:50:01 - User: alice - Sign-in successful
2024-07-09 11:00:27 - User: bob - Sign-in failed (incorrect password)
2024-07-09 11:10:19 - User: bob - Sign-in successful
2024-07-09 11:30:44 - User: charlie - Sign-in successful
2024-07-09 12:05:59 - User: alice - Sign-in failed (session timeout)
```

Now **foreach** user I want to know how many successes that user has had in this log. Now if I loop through the entire log just to find one user over and over again it will cost processing power and make the code slower as the code will have to check if a user is equal to the entry. That the being the case, we want to skip unnecessary events and thus continue will be helpful in a loop. On the other hand with break, if we were trying to look for critical event we don't need a loop through the entire log anymore. 

So let's demonstrate this with some code: 

```python
# Sample event log data
event_log = [
   "2024-07-09 08:15:34 - User: alice - Sign-in successful",
   "2024-07-09 08:17:45 - User: bob - Sign-in successful",
   "2024-07-09 08:18:56 - User: charlie - Sign-in failed (incorrect password)",
   "2024-07-09 08:20:12 - User: charlie - Sign-in successful",
   "2024-07-09 09:30:54 - User: alice - Sign-in failed (account locked)",
   "2024-07-09 09:32:01 - User: alice - Sign-in successful",
   "2024-07-09 09:45:21 - User: bob - Sign-in successful",
   "2024-07-09 10:05:37 - User: charlie - Sign-in successful",
   "2024-07-09 10:50:01 - User: alice - Sign-in successful",
   "2024-07-09 11:00:27 - User: bob - Sign-in failed (incorrect password)",
   "2024-07-09 11:10:19 - User: bob - Sign-in successful",
   "2024-07-09 11:30:44 - User: charlie - Sign-in successful",
   "2024-07-09 12:05:59 - User: alice - Sign-in failed (session timeout)"
]


#For loop using continue
count = 0
for event in event_log:
   event_parts = event.split(" - ")

   if 'alice' not in event_parts[1]:
      continue
   else:
      count += 1

print(f"Number of successes from user alice: {count}")


#For loop using break and continue keywords
for event in event_log:
   event_parts = event.split(" - ")

   if 'account locked' not in event_parts[1]:
      continue
   else:
      print(f"Timestamp of which an account lockout happened: {event_parts[0]})
      break

```

So the first loop in the code iterates through each event entry in the event logs, checks if alice is contained in the username part of the entry. If it is is not 'alice' it will continue to loop through the events otherwise keep a count of the number of sign ins. After the loop is done the script will printout the count of successes in the log

For the second second loop it will iterate through the log and checks if the event contains 'account locked'. If it does continue to the next event, if it doesn't then it will printout the timestamp of the event and then break out of the loop since we don't need to loop through the rest of the events.

Hopefully this helped to understand loops a bit more and how they compare with another language that is more strict in it's data types.

## Functions

## Try Except

## Debuggers: The Godsends of Coding

## Looking Things Up: The Real Challenge of Programming

Now I deliberately left out some other information throughout the this tutorial as I encourage you to be able to look up information on your own using google when it comes to adding together these differing concepts. Am I being lazy? Yes, I partly am but this is something that can only be done with practice. After all, no pain no gain. But I am not going to leave you out to dry. That being case, it begs the question of how you are supposed to look up some of these things. In the case of adding a list to a dictionary, I myself would go to google put in the search phrase "How to add list to dictionary" and start looking around on stackoverflow. Now since the future is now, we have AI chatbots to help us out on this one as well. Which are quite handy to figure out simple problems like finding out how to add a list to a dictionary. 

Now I am going to put a disclaimer about using chatbots like ChatGPT and Github copilot. They are not the end all be all for coding. Chatbots from my coding experience, all be it somewhat small, cannot help to build full on code bases for you and I encourage not to heavily rely on them. They are a tool not a programmer. The reason for this is these chatbots tends to make mistakes is that if you are unable to spot them then you are going to be left wondering why your code doesn't work despite replying constantly to the chatbot with being on the verge of bashing your computer with a brick. So when starting off I recommend to use these chatbot sparingly and when you get better and better at coding in python you can start to use it more as more of a reference rather than it telling you what/how to code.

Though please be also mindful what code you paste into ChatGPT. Especially if are working for an organization, as you shouldn't leak personal data of users when creating scripts and having ChatGPT analyze code. 

With that out of a way let's look at some examples of how I would look into things if I ran into issues.

### First Scenario: Even Simple Problems Can Take Forever

I am going to start off with a simple scenario here: I was trying to teach someone how to use python once and at the time it had been a little bit since I programmed it. I was trying to teach how to create a dictionary and loop through that dictionary for it's keys and values. But the issue was that I forgot how to do this.

So what was my thought process?:

I know the basic building blocks are that I need the for loop and dictionary. I know how to print items in a dictionary and I know that looping through a list just requires you to name on var in the foreach item in the list. So let's try do that with just as simple example separate from the main file. This way I can just focus on the problem rather than how it interacts with everything else in the main file:

```python

dict = {1:'test', 2:'test2', 3:'test2' }

for value in dict:
   print(value)
```

**Results:**

```
1
2
3
```

Well it is close but not what I am really looking for. I want to print out both the key and the value and not only that the var name "value" does not really match up to the data I am getting. It would be more appropriate to call this var "key" instead as it is getting just the keys.

This being the case, I took to the almighty google for help. I typed in the search "How to iterate through key and value in dictionary python". I got a few results on it. Now it is important when looking for information like this that you don't want to spend all day on one article. You probably want to spend like 15 seconds tops when looking for information as simple as this. Now for more complicated topics this will take longer of course. But you want to try to find an answer quickly so skim articles until you find something that is more familiar. I found an article on realpython.com, but I had to skim about less than quarter down until I got the header that explained the items method which was I was looking for. If you can't find anything in those 15 seconds then it is time to go to another article from those links on google. Remember, the name of the game is to be quick about it. You want to get on with your life. If the article doesn't get to the point, leave it. 

But looking through that header, I found their simple script that showed this:

```
>>> for key, value in likes.items():
...     print(key, "->", value)
...
color -> blue
fruit -> apple
pet -> dog
```

This looks what I am looking for. It, one, prints out not only the key but also the values and, two, it's simple. 

So let's try to apply this to our own script:

```python

dict = {1:'test', 2:'test2', 3:'test2' }

for key in dict.items():
   print(value)
```

**Results:**

```
(1, 'test')
(2, 'test2')
(3, 'test2')
```

Strange. Why doesn't it look like just straight values? Let me look at the example again:

```
>>> for key, value in likes.items():
...     print(key, "->", value)
...
color -> blue
fruit -> apple
pet -> dog
```

Oh, I see now. There are two vars in the for loop. Let's try something similar:

```python
dict = {1:'test', 2:'test2', 3:'test2' }

for key, value in dict.items():
   print(key, value)
```

**Results:**

```
1 test
2 test2
3 test2
```

Look at that, it prints out the straight values now. Mission success! And it only took a minute! Now for those who are doing this for the first time it might take more like 15 minutes. This is a skill you train overtime and you will get better as you keep doing this over and over. It is important to recognize how to break down a problem. If you can break down a problem into smaller parts and then work your way up you can find solutions to many bigger issues.

### Second Scenario: When to Use a Chatbot

I know I put the disclaimer to minimize using a chatbot, but with everything life there are exceptions to the rules. I suggest to use chatbots when you can't figure out just where the code is going wrong. Hopefully you would use a debugger to find this out but sometimes it is quicker to check it with a chatbot. Furthermore, you would want to use a chatbot to quickly just understand what a piece of code is doing as well. For example, take the following function:

```python
def rearrange_chunks(chunks, key):
   key_hash = hashlib.sha256(key.encode()).digest()
   key_index = int.from_bytes(key_hash, byteorder='big')

   # Seed the random number generator with the hash of the key
   rng = np.random.default_rng(key_index)  # Save the random value

   # Generate a random permutation of indices
   permuted_indices = rng.permutation(len(chunks))
   # Take the reverse of the array starting from the end backwards

   # Rearrange chunks based on the permuted indices
   rearranged_chunks = [None] * len(chunks)
   for i, index in enumerate(permuted_indices):
      chunk = apply_distortion(chunks[index])
      rearranged_chunks[i] = chunk
   return rearranged_chunks
```
This function was in a project I was in that encrypted an image. A friend made this but I didn't really understand what it was doing specifically at the time. I was lazy and didn't want to read the code for 15 minutes so I pasted it into chatGPT to get it break it down for me quickly. After it had spat out it answer, I was able to quickly understand what it was doing. So what took me 15 minutes to understand the code it took just a minute. But please understand that in this scenario I am using ChatGPT as a tool and a supplement to my coding not as something that codes the entire codebase for me.

This really concludes the tutorial part of this document. Now the next thing to do is try put everything into practice. The next section uses weather data that you can mess around with. Follow the parts, and you will essentially know how to program in python. Anything you don't know, you will pick up as you research for a solution to your smaller problems. Remember to take larger problems and break them down into something that is manageable. After that, work your way up with bigger and bigger problems.

Good Luck on the exercise!

## Exercise: Analyzing Weather Data

In this exercise, you will analyze weather data for a week. The data includes daily temperatures and humidity levels. You will perform various tasks such as reading data from a file, calculating average values, finding maximum and minimum values, and handling potential errors using try-except blocks.

### Part 1: Prepare the Data

1. **Create a Text File**:
   - Name the file `weather_data.csv`.
   - Add the following content to the file:

     ```
     Day, Temperature, Humidity
     Monday,25,60
     Tuesday,30,65
     Wednesday,28,62
     Thursday,26,61
     Friday,27,63
     Saturday,29,64
     Sunday,24,59
     ```

### Part 2: Read the Data from the File

2. **Open and Read the File**:
   - Write a function to read the data from the file.
   - Store the data in a list of dictionaries.
   - Each dictionary should have keys: `day`, `temperature`, and `humidity`.
   - Use try-except blocks to handle potential file-related errors.

### Part 3: Calculate Average Temperature and Humidity

3. **Average Calculation**:
   - Write a function to calculate the average temperature.
   - Write another function to calculate the average humidity.
   - Use numpy arrays to facilitate these calculations.

### Part 4: Find Maximum and Minimum Values

4. **Maximum and Minimum Calculation**:
   - Write a function to find the day with the maximum temperature and its value.
   - Write a function to find the day with the minimum temperature and its value.
   - Write functions to find the days with the maximum and minimum humidity and their values.

### Part 5: Handle Errors Gracefully

5. **Error Handling**:
   - Modify the function that reads the weather data to handle errors such as missing or malformed data lines.
   - Use try-except blocks to catch and report these errors without stopping the execution of the program.

### Summary

- **Lists**: Use to store the weather data.
- **Dictionaries**: Each entry in the list should be a dictionary representing a day's data.
- **Numpy Arrays**: Use to calculate the average values.
- **Try-Except Blocks**: Use to handle file not found and data parsing errors.
- **Functions**: Encapsulate logic for reading data, calculating averages, and finding min/max values.
- **File Operations**: Open and read from the weather data file.
- **Loops**: Iterate over file lines and data entries.

### Additional Tips

- Make sure to import necessary modules like `numpy`.
- Test your functions individually to ensure they work correctly.
- Print intermediate results to verify your calculations step by step.
- Handle edge cases, such as empty files or files with incorrect data formats.
