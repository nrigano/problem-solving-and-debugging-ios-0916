# Debugging Checklist
It's said that a programmer's job is 20% coding and 80% debugging. This is especially true as you start your journey into code. This cheetsheet should serve as a reference for mitigating against, identifying, and squashing bugs. Read through and follow these steps to avoid and solve problems in your code.

## Single Responsibility Principle (SRP)
One of the most important steps of debugging is to prevent bugs from being created in the first place. An important concept to which your code should adhere is the **Single Responsibility Principle**. 

Imagine you're writting a complex piece of code that will perform multiple distinct operations. Maybe you want to 

Each class and method should have a single responsibility, and should call on other classes or methods as necessary to achieve additional functionality. This also applies to smaller pieces of code. For instance, 

It's much easier to diagnose 

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