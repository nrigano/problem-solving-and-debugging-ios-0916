# Problem Solving and Debugging
Coding is the process of identifying and solving problems. The intent of this document is to serve as a high-level reference for diving into a complex problem, as well as mitigating against, identifying, and squashing bugs. Read through and follow these steps to avoid and solve problems in your code.

## Quick Hit List

* Clearly **define all your inputs and outputs**.
* **Break your complex problem into smaller problems**, then break those down even further until you see patterns and problems you recognize.
* Write code that conforms to the **Single Responsiblity Principle**. Every class, method, and function should have a single purpose.
* **Don't Repeat Yourself**. If you write or copy and paste the same code, stick it in a separate method and call the method when needed.
* **Read all warning and error messages**. These messages are presented for your benefit, and will either illuminate an unapparent bug or provide a point from which to start the debugging process.
* **Check your variables**. Use logs, breakpoints, and your debugger to check the relevant data getting passed around and acted upon in your code. Make logs frequent and descriptive, with details on what's getting called, what's expected to happen, and what the contents of the data are.
* **Don't dwell on problems by yourself**. What might take hours of frustration and digging through code may be answered with a few minutes of searching online or by asking others for help.

## How to Solve Complex Problems
A complex problem is the combination of multiple simple problems. Therefore, **the most important step in solving a complex problem is to break it down into the smallest possible pieces.**

* Start with the inputs and outputs.
  * Determine what the expected result should look like and all the attributes you know the result should have.
  * Next, do the same for the all the ingredients that will be used to reach the desired output. If you don't know what the ingredients are, figure out what's available and determine what of that is relevant to the problem.
  * Write the inputs and outputs down, and as with your code, be clear and detailed. Oftentimes if the inputs and outputs of a problem are defined clearly enough, and with enough detail, the solution becomes clear.
  * Given the inputs you've listed, what is actually relevant? Think about how the inputs can be broken down into the simplest components which will be useful. For example, are you comparing an entire array to another entire array? Or is the goal actually to compare one string from an array to a string from the other array? Or even one character at a time from each string?
* Describe the magic in the middle. Now that you know where our problem starts and ends, describe the process by which the inputs turn into results.
  * Write down as many ideas as you can for potential paths which will take you from beginning to end. Don't rule anything out, no matter how absurd. These can be just a few words, but it's always helpful to be detailed.
  * Starting with the simplest idea, go through each possible path and start to write pseudocode that describes roughly the steps you want to take. Lay out your ideas in plain language to see more clearly the logic of your program as you go. If you write out your pseudocode as comments in your development environment, you'll later be able to add in actual code to match each line of pseudocode.
  * Diagram the flow of data in your program and the actions which take place. Draw out steps in as much detail if you can. If you can draw it, you can code it.

## Single Responsibility Principle (SRP)
One of the most important steps of debugging is to prevent bugs from being created in the first place. An important concept to which your code should adhere is the Single Responsibility Principle.

Each class and method should have a single responsibility, and should call on other classes or methods as necessary to achieve additional functionality. Try to apply this priciple at each scope of your code.

## Don't Repeat Yourself (DRY)
If you find yourself writing the same code multiple times, put it in a separate method and call that when necessary. This creates fewer potential points of failure and will make refactoring easier, if necessary.

## Error/Warning Messages
Error messages and warnings are provided for your benefit. If you get an error or warning message, take a moment to read through it. Many simple, but unapparent, problems will be made clear, and you will now have a point from which to start your search for a solution to more complex problems.

## Check Variables
A good place to start debugging is to track the value of your variables. You may find that variables don't hold the values you expect, or don't hold any value at all. There are several ways to examine the values your variables hold.

### Logging
It's good practice to insert logs as you write your code, long before any problem arises, so you can more easily visualize the flow of your program as it runs. An effective log should contain a brief description of where it is, what is going on, and what the contents are of relevant variables. Such a log message might look like this:

```
addNewCustomerToDeliLine method in AppDelegate just called with customer dictionary:
{
	"name" = "Kanye West",
	"food" = "ham on ham with ham",
	"side" = "more ham",
	"drink" = "green tea"
}
```

Descriptive logs make it easier to identify variables that contain unexpected values and diagnose methods that aren't functioning as intended. Add as many logs as you like, as they are free to use and provide a means to search through the flow of data within your program while and after it runs.

### Breakpoints
Add in breakpoints to watch as variables in your code are declared, instantiated, assigned values, or altered. Breakpoints allow you to see line-by-line what your program is doing, and work well when used in conjunction with logs to pinpoint appropriate locations for their use.

## Resources
There are many resources you can and should use to help solve problems and debug your code. Every major problem you come across can be broken down into smaller problems, and almost every one of those smaller problems has been experienced and solved by someone else.

### Documentation
Official documentation is an often-overlooked resource for problem solving, and should be the starting point for much of your debugging. Use documentation to understand the capabilities, properties, and characteristics of the elements of your code. If you're not sure what something can do, or how to interact with or implement a piece of code, dig into the documentation.

### Google
This should always be your first stop after the documentation. Simply searching for an error code or a clear description of the problem you face will bring you multiple potential solutions. If relevant results don't show up, increase the specificity of your search terms. Conversely, you can abstract your search to more generally describe the problem at hand.

### Other People
Don't spend more than an hour trying to solve a problem on your own. After you've exhausted online resources, talk to your neighbors. See if anyone around you has experienced and solved the problem you face, and **ask not what the solution is, but how you can solve the problem on your own**. If your neighbors also wind up stumped, and a thorough search on the internet turns up nothing, it's time to ask an instructor.

<p class='util--hide'>View <a href='https://learn.co/lessons/problem-solving-and-debugging'>Problem Solving And Debugging</a> on Learn.co and start learning to code for free.</p>
