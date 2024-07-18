# Debuggers: The Godsends of Coding

Debuggers along with print statement can get you out of a jam a lot of time, especially when the code base you have is quite large. I am going to talk about the python debuggers. They are many debuggers for differing languages. From c to python you'll most likely see that that coding language has a debugger of some kind. But there is also the tried and true method of debugging but arguably the most annoying. Putting 'print' statements everywhere in the code! This I don't recommend unless you have to or want to get a better idea of what data in certain variables look like. But without further ado, what are debuggers? They are tools to follow the execution flow and look into what data is being saved/deleted in variables throughout your code. They are used to help you identify where issues may lie in your code's execution flow. Now this is a simplified explanation of it and thus if you are more interested in the nitty gritty details of how they work you can try to do some research on your own. But let's look into some simple code that is broken. 

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 2) 

# Test the function
number = 5
result = factorial(number)
print(f"The factorial of {number} is {result}")
```

Now this is code that is supposed to calculate the factorial of any number that we give to the variable 'number'. So in our case we are supplying the number 5 into the factorial function. The result we should expect is 120. So let's run it and see if we get that value. 

![alt text](https://github.com/GabeALopez/data-analysis-curriculum/blob/main/practical_python/Part_1/debugger_imgs/error.png)

Hmmm.... It looks we didn't get the result we were supposed to get. So let's add, what's called' a break point. Now a breakpoint tells the debugger where to stop the code so you can start tracing it. To add one in VS code you click on the left side of the line numbers. Let's add one on line 9 of the python code. When hovering your mouse over the left side of the line number 9 you will see a greyed out red dot. If you click it you will see a full red dot. To remove this breakpoint, you will click on the red dot once again. But for now let's keep the breakpoint. Once that is done, we are going to go to the top right where we see an arrow. There should be a drop down array next to it. Click on that and click 'Python Debugger: Debug Python File". This will run the script and stop it at the 9th line. Here is a graphic that shows everything that has been done so far: 

![alt text](https://github.com/GabeALopez/data-analysis-curriculum/blob/main/practical_python/Part_1/debugger_imgs/breakpoint.png)

What should appear is a big red box that is on the 9th line. This shows that the debugger has stopped on this line and is now awaiting you to issue commands. Now we are not going to use actual commands, but just use the VS code's GUI to do this. At the top of VS code you should see 5 arrows going in differing directions and a square. These are buttons where we are going to use to step through code. But let's go through what each button does. 

The first button on the far left is the continue button. This tells the debugger to continue running the code until it hits another breakpoint. 

**Side Note:** You can add more than just one breakpoint. You can put them on multiple different lines. So if you really wanted to you could add a breakpoint on every line. But that is really tedious so put your breakpoint at specific locations. But side note over!
**Sider Note:** You can hover over each button with your mouse and it will give you the name of the button as well as the shortcut for it. 

The second arrow is the step over button. This button will tell the debugger to step over a line of code. So for instance if you didn't want to brought into a function in your code execution, you can just jump right over it. 

The third arrow is the step into button, which you will be using most of the time. This button tells the debugger to step one by one line of code. 

The fourth arrow is the step out button. This tells the debugger to step out of a code block that it is. So for example, let's say you entered a function but you want to get out it since the problem in the code doesn't seem to be in that function. This is where the step out button comes in. We can get out of that function and onto the next after the function call with that button.

The fifth and final arrow will restart the program from the start. There isn't really much to explain about that. 

The last symbol, the square, will the stop the program and the debugger in it's entirety.

Here is a graphic that shows each one and their names with numbers:

![alt text](https://github.com/GabeALopez/data-analysis-curriculum/blob/main/practical_python/Part_1/debugger_imgs/buttons.png)

So let's now step through until we get to line 2. A nice thing I've written here about the debugger is that you can see the values of variables while the code is running. We can see this in this example by hovering over the variable 'n'. It will show five as that is the number we passed into the factorial function. Pretty cool!

Now lets step until we get to line 5 and then step again. Now look at the var 'n' it is three now. This is a little strange. If we follow this logic of subtracting 2 from 'n' we seem to be missing numbers to multiply as 5! = 1\*2\*3\*4\*5 but we are missing 4 in this equation. So maybe the problem is with line 5, where it should be decrementing by 1 not 2. So let's stop the debugger, change '2' to '1', and run it like normal: 

![alt text](https://github.com/GabeALopez/data-analysis-curriculum/blob/main/practical_python/Part_1/debugger_imgs/fix.png)

Viola! It calculates correctly now. If you have been following, congrats on your first debug. Out in the real world this is a way to find those bugs and being able to solve them. 

A bit of side tangent, but I wanted to put in my input on how I use the debugger in conjunction with print statements. A lot of time I end up using the debugger to solve very simple bugs or to figure out where the specific issue is located in the general scheme of the code. Now I have found that the debugger is not the end all be all, as in life, there are exceptions to the rules. I end up still using print statements to understand the data that that is being used/manipulated in very specific parts of code since the code sees the data differently than I do. A difference in perspective as it were. But using these in conjunction help me to get a better idea of the grander issue of things in my code. 