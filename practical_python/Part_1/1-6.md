## Functions

Functions are like reusable blocks of code and most programming languages have them. So when would you want to reuse a block of a code? You would want reuse blocks of code procedures that seem to be repeatable in in some way. So let's say you create code to square of a value, but the thing is you don't want to code that again for a different value. This is where functions come in.

We can declare a simple function like so to square a number:

```python
def square(x):
   return x*x
```

Let's break this function down a little bit. In order to create a function we have to name it something and in this case we aptly named it "square". The var in the parenthesizes is called a parameter where a general variable is going to be specifically in the function. When we use it in code, or call it, we are going to put into the parenthesizes is a variable, or passing in a variable. The operations will be then done inside function where whatever number is passed into the function will be squared and given, or returned, back is our squared function.

We can call the square function like so:

```python
def square(x):
   return x*x

#This is where the square function is called and placed into the var squared_num
squared_num = square(5)

print(squared_num)
```

For these functions you can have as many parameters as you want to be passed into these functions and have them do whatever you really want them to do. The sky is really the limit.

Interestingly enough, you can also call functions within functions. This gets into the idea of recursion where you can break down a problem by calling functions within functions. An example of this are calculating factorials. So let's say you wanted to calculate 5!, it would take a bit of time to do in loop, but it is easier to create using recursion. Now I am not saying that you should always use recursion for everything. Unfortunately recursion is known to slow down your code as it keeps having to call function after function. 

But let's look at the factorial recursion: 

```python
def factorial(n):
   if n == 0:
      return 1
   else:
      return n * factorial(n - 1)

```

You can see in the factorial function, we are actually calling the function over and over. And once we get to a point where I we can't calculate anymore we come back and multiply every number we have collected throughout each iteration. Pretty neat!