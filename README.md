JavaScript Functions Guide
This guide explains the basics of JavaScript functions, including how to invoke and write them. Functions are blocks of code designed to perform specific tasks and can be reused by calling them.
Invoking Functions
Functions in JavaScript are recognizable by their parentheses (). You can call a function in the following ways:
// Function with no arguments
nameOfTheFunction();

// Function with multiple arguments
functionThatTakesInput("the input", 5, true);

Writing Functions
Functions are declared using the function keyword. Below is the basic syntax:
function nameOfTheFunction() {
    // Content of the function
}

You can call the function as shown:
nameOfTheFunction();

Example: Greeting Function
Below is an example of a function that prompts the user for their name and prints a greeting to the console:
function sayHello() {
    let you = prompt("What's your name? ");
    console.log("Hello", you + "!");
}

How to Use

Copy the code above into your JavaScript file.
Call the function by adding sayHello(); in your code.
When executed in a browser, it will prompt for a name and log a greeting to the console.

For more details on JavaScript functions, check out MDN Web Docs.
