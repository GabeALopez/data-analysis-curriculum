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

