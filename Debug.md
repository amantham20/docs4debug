# How to Debug 101

## Debugging with Print Statements

We've all been there - trying to track down a bug in our code and resorting to adding print statements everywhere to see what's going on.

The simplicity of printing variable values or messages to check program flow makes print debugging an easy first step when issues arise. Just add a few print statements, run the code, and check the output to gain insight into what's happening under the hood. It doesn't require any fancy tools or setup.

However, print debugging has its downsides. It can clutter up the code with lots of print statements that you'll later have to clean up. And it doesn't work well for tracing deeper logical issues. Excessive printing can also slow down the program. After all the couse is about being computationaly efficient.

Here is a some of my code from Freshman year. 😳

![PrintDebug](images/PrintDebug.png)

## Debugging with a Debugger

While print statements have their place, to take your debugging skills to the next level, it's worth learning how to use a debugger built into your IDE. Debuggers allow you to pause execution, inspect variables, and step through your code line-by-line to understand what's happening.

Many IDEs like Visual Studio, and PyCharm have excellent debugging support. It's just a matter of learning the basics:

* Setting breakpoints to pause execution at certain lines
* Stepping over, into, or out of functions as you walk through code
* Viewing the call stack to understand the execution path
* Inspecting variables to check their values
* Watching expressions to track changes or issues

It may feel daunting at first if you've never used a debugger. But once you get the hang of it, you'll have way more visibility into your code and can zero in on problems much faster than with print statements alone. The investment of time pays off greatly in the long run.

So don't be afraid to graduate from print debugging and unlock the full potential of your IDE's debugger. Often one can combine it with judiciously placed prints and you'll have a killer debugging duo.

### working with break points

Breakpoints are one of the most useful features of debuggers in IDEs like VSCode and PyCharm. They allow you to pause execution at any line of code you specify to inspect the state of the program.

In VSCode, you can set a breakpoint by clicking on the editor margin to the left of the line number you want to break on. A red dot will appear indicating the breakpoint.

![BreakPoint](./VSCodeBreakPoint.png)

In PyCharm, click on the gutter to the left of the line number to set a breakpoint.

![BreakPoint](./PyCharmBreakPoint.png)

Breakpoints are enabled only during debug mode.

Here is an example of where a breakpoint has been hit during Debug for project 1.


The blue line highlights the current line of execution. 
<!-- show the pycharm image -->

In the lower right we can inspect the variables in the current scope at the breakpoint. [Color] Region

Key tips for inspecting variables:

* Check if a variable has the expected value at a given point.
* Inspect object properties to ensure they are set properly.
* Watch a variable to see when its value deviates from expectations.

### Hover Inspection
Both VSCode and PyCharm provide a handy hover inspection feature that lets you view variable values during debugging without explicitly expanding variables or setting watches.

Simply hover over any variable when paused on a breakpoint to see a popup with the current value.

### Navigating Debugged Code
Once execution is paused on a breakpoint, you have several options to step through code and analyze the flow:

<!-- Image for steps -->

* Resume - Resumes full execution until the next breakpoint. Useful to fast forward past uninteresting sections.
* Step Over - Steps to the next line, but does not enter any functions called on that line. Steps over code without digging into it.
* Step Into - Steps to the next line, entering any functions called on that line. Steps into code to deeply analyze it.
* Step Out - Runs the rest of the current function and stops at the line after the function call. Great for stepping out of code you don't need to debug.


<!-- Some tips for efficient debugging navigation:

* Step over setup code to get to the meat of the logic.
* Step into functions that contain bugs or complex code.
* Use step out to surface back out of details you've debugged. -->


### Leveraging the Stack Trace
Another useful debugging tool provided by IDEs' like VSCode and PyCharm is the stack trace. This gives you visibility into the sequence of function calls that led to the current execution point. Verry Very useful for functional programming and recursion.

<!-- ## [Recursion](#recursion). -->

When paused in the debugger, the stack trace shows the chain of functions calls in order from the top level caller down to the current line of execution. This helps reconstruct how the code reached its current state.


### 

























