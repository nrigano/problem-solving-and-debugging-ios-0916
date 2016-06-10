# Problem Solving and Debugging
Coding is the process of identifying and solving problems. The intent of this document is to serve as a high-level reference for diving into a complex problem, as well as mitigating against, identifying, and squashing bugs. Read through and follow these steps to avoid and solve problems in your code.

### Quick Hit List

* Clearly **define all your inputs and outputs**.
* **Break your complex problem into smaller problems**, then break those down even further until you see patterns and problems you recognize.
* Write code that conforms to the **Single Responsiblity Principle**. Every class, method, and function should have a single purpose.
* **Don't Repeat Yourself**. If you write or copy and paste the same code, stick it in a separate method and call the method when needed.
* **Check your variables**. Use logs, breakpoints, and your debugger to check the relevant data getting passed around and acted upon in your code. Make logs frequent and descriptive, with details on what's getting called, what's expected to happen, and what the contents of the data are.
* **Don't dwell on problems by yourself**. What might take hours of frustration and digging through code may be answered with a few minutes of searching online or by asking others for help.

## How to Solve Complex Problems
A complex problem is the combination of multiple simple problems. Therefore, **the most important step in solving a complex problem is to break it down into the smallest possible pieces.**

* Start with the inputs and outputs.
  * Determine what the expected result should look like and all the attributes you know the result should have.
  * Next, do the same for the all the ingredients that will be used to reach the desired output. If you don't know what the ingredients are, figure out what's available and determine what of that is relevant to the problem.
  * Write the inputs and outputs down, and as with your code, be clear and detailed. Oftentimes if the inputs and outputs of a problem are defined clearly enough, and with enough detail, the solution becomes clear.
  * Given the inputs you've listed, what is actually relevant? Think about how the inputs can be broken down into the simplest components which will be useful. For example, are you comparing an entire array to another entire array? Or is the goal actually to compare one string from an array to a string from the other array? Or even one character at a time from each string?
* Describe the magic in the middle. Now that we know where our problem starts and ends, we can begin to describe the process by which our inputs turn into results.
  * Write down as many ideas as you can for potential paths which will take you from beginning to end. Don't rule anything out, no matter how absurd. These can be just a few words, but it's always helpful to be detailed.
  * Starting with the simplest idea, go through each possible path and start to write pseudocode that describes roughly the steps you want to take. Laying out your ideas in plain language is useful as you can see more clearly the logic of your program as you go. If you write out your pseudocode as comments in your development environment, you'll later be able to add in actual code to match each line of pseudocode.
  * It always helps to draw out your ideas on paper.

## Single Responsibility Principle (SRP)
One of the most important steps of debugging is to prevent bugs from being created in the first place. An important concept to which your code should adhere is the **Single Responsibility Principle**.


Each class and method should have a single responsibility, and should call on other classes or methods as necessary to achieve additional functionality. This also applies to smaller pieces of code. For instance,

It's much easier to diagnose a problem when

## Don't Repeat Yourself (DRY)


## Check Variables
A good place to start debugging is to track the value of your variables.

### Logging
Use `NSLog` in Objective-C and `print()` in Swift to write out messages to the console in Xcode. It's good practice to insert logs as you write your code, long before any problem arises, so you can more easily visualize the flow of your program as it runs. An effective log should contain a brief description of where it is, what is going on, and what the contents are of relevant variables. Such a log message might look like this:

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
Add in breakpoints!

### Print Objects

## Resources
### Google
### Stack Overflow
### RyPress
### NSHipster
