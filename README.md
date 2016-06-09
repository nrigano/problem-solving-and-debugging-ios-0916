# Problem Solving and Debugging Checklist
Coding is the process of identifying and solving problems. The intent of this document is to serve as a high-level reference for diving into a complex problem, as well as mitigating against, identifying, and squashing bugs. Read through and follow these steps to avoid and solve problems in your code.

## How to Solve Complex Problems
A complex problem is the combination of multiple simple problems. Therefore, **the most important step in solving a complex problem is to break it down into the smallest possible pieces.**

* Start with the inputs and outputs.
  * Determine what the expected result should look like and all the attributes you know the result should have.
	* Next, do the same for the all the ingredients that will be used to reach the desired output. If you don't know what the ingredients are, figure out what's available and determine what of that is relevant to the problem.
	* Write the inputs and outputs down, and as with your code, be clear and detailed. Oftentimes if the inputs and outputs of a problem are defined clearly enough, and with enough detail, the solution becomes clear.
* Describe the magic in the middle. Now that we know where our problem starts and ends, we can begin to describe the process by which our inputs turn into results.
  * Write down as many ideas as you can for potential paths which will take you from beginning to end. Don't rule anything out, no matter how absurd.


Pseudo code and comments



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
Add in breakpoints to

### Print Object
 When stopped at a breakpoint,

## Resources
### Google
### Stack Overflow
### RyPress
### NSHipster
