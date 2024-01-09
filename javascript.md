# Learning javascript
## Index
- [Learning javascript](#learning-javascript)
  - [Index](#index)
  - [Data Types](#data-types)
    - [Strings](#strings)
    - [Numbers](#numbers)
    - [Booleans](#booleans)
    - [JSON (JavaScript Object Notation)](#json-javascript-object-notation)
    - [Undefined and Null](#undefined-and-null)
  - [Logging](#logging)
  - [Variables](#variables)
  - [Basic math](#basic-math)
  - [Functions](#functions)
    - [Normal functions](#normal-functions)
    - [Anonymous functions](#anonymous-functions)
  - [If statements](#if-statements)


## Data Types
Javascript has a lot of different types of data. You have strings which is just text, You have numbers, Booleans which is either `true` or `false`, and json (JavaScript Object Notation).\

### Strings
Strings are defined by using double quotation marks.\
Example:
```js
"This is a string"
```
\
You can add 2 string together by using a plus sign.\
Example:
```js
"Some" + "String" // This will become "SomeString"
```
\
You can also add things to a string by using `+=`. `+=` basically means you add something to the value and then set the value to the new value.\
Example:
```js
"Some other" += "string" // This will become "Some otherstring"

"abcdef" += "g" // This will become "abcdefg"
```
this might look the same as just adding 2 strings together but if you have a [variable](#variables) with a string value and you add that string to another string the variable will not change. This adds the string to the variable.

### Numbers
Numbers are pretty self explanatory. Their just numbers.\
There are however a few things that are important to know.\

- `NaN` NaN literally means `Not a Number`

- `Infinity` Infinity is exactly what it says

### Booleans
Booleans are either `true` or `false`. They are mainly used for things that can be on/of or true/false.\
They are mainly used for statements.\
Examples:
```js
11 > 10 // Checks if 11 is greater than 10 using > (Greater than symbol). This will be true as 11 is bigger than 10

9 >= 10 // Checks if 9 is equals or greater than 10 using >= (Greater than or equals to symbol). This will be false as 9 is not 10 nor greater than 10

11 <= 11 // Checks if 11 is equals or lower than 11 using <= (Less or equals to symbol). This will be true as 11 equals to 11

4 < 2 // Checks if 4 is lower than 2 using < (Less than symbol). This will be false as 4 is greater than 2tInfinity

4 == 4 // Checks if 4 has the same value as 4 by using == (Equal to). This will be true as 4 has the same value as 4

4 === "4" // Checks if 4 has the same value and type as "4" by using === (Equal value and type). This will be false as 4 has the same value as "4" but not the same type as one is a number and the other a string

4 != 4 // Checks if 4 is not 4 by using != (Not equals to). This will be false as 4 equals to 4
```
You can also invert a boolean by using an exclamation mark.\
Example:
```js
true // This just equals true

!false // This also equals false as its inverted by the exclamation mark

!!false // This is false as its inverted and then inverted again
```

### JSON (JavaScript Object Notation)

json is an easy way to store data using key value pairs. So every entry has a name (the key) and a value.\
json looks like this:
```json
{
    "key": "value",
    "secondKey": 123,
    "someBoolean": false,
    "MoreJSON": {
        "key": "value"
    }
}
```
As you can see json has keys and values and the values can be any type, strings, numbers, booleans, or more json.\
\
You can use json like this:\
(In this example [variables](#variables) and [logging](#logging) are used. Please refer to [variables](#variables) and [logging](#logging) for an explanation)
```js
const someJson = {
    key: "value" // In javascript the key does not need to be a string, in .json files the keys do need to be a string. .json files also cannot have comments like this
}

console.log(someJson) // This will log the json object as a whole i.e. {key: "value"}

console.log(someJson.key) // This will only log the specified value i.e. "value"
```
\
You can also modify json.\
Example:\
(In this example [variables](#variables) are used. Please refer to [variables](#variables) for an explanation)
```js
const someJson = {
    key: "value"
}

key = "other value" // From now on someJson.key is "other value". Any code before this still sees someJson.key as "value", everything after this will see it as "other value"
```

### Undefined and Null
- `Undefined` Undefined means that the value is not defined.
- `Null` Null means that the value is assigned a Null value which basically means that there is no value but it is defined.

## Logging
Logging is very important. Its used for debugging or just for getting information.\
You can log everything, strings, numbers, booleans, json, even functions (although without executing them it will just show up as something like this `[Function (exampleFunction)]`).\
To log something to the console you can use the `console.log` function.\
Example:
```js
console.log(10); // Logs 10 to the terminal

console.log("Hello, World!"); // Logs Hello, World! to the console

console.log(true); // Logs true to the console

function exampleFunction() { return "some value" }
console.log(exampleFunction); // As explained above this will log [Function (exampleFunction)]
console.log(exampleFunction()); // Here you actually execute the function and this logs someValue as the function returns the string "someValue"
```

## Variables
You can declare variables using the `let` keyword followed by the name of the variable followed by an equals sign and then the initial value of the variable.\
Example:
```js
let x = 10;
```
In this example i declare a variable named `x` and set it to `10`.

When using the `let` keyword to declare a variable you can always assign a different value to it just by entering the name of the variable followed by an equals sign followed by the new value.\
Example:
```js
let x = 10; // Declare x and assign it a value of 10

x = 5; // Change the value to 5
```

You can also declare variables without assigning it a value. You can always assign a value to it later.\
Example:
```js
let x; // Declare x but don't assign it a value

x = 5; // Set x to 5
```

You can declare constants using the `const` keyword. Constants need to be assigned a value when you declare it and the value cannot be changed.\
Example:
```js
const x = 10;
```

So the next example would give an error as you cannot resign a constant variable.
```js
const x = 10;

x = 5; // Error
```

## Basic math
Math is of course also a thing. Its very easy.\
You have the basics like addition, subtracting, multiplication, dividing and modulus:
```js
1 + 1 // Addition

1 - 1 // Subtraction

1 * 1 // Multiplication

1 / 1 // Dividing

1 % 1 // Modulus
```
\
And then of course you have brackets:
```js
(1 + 1) * 5 // Without brackets this would be 6. With them it is 10
```
If you know a little math you should know why this is but this is because the [order of operations](https://en.wikipedia.org/wiki/Order_of_operations).

## Functions
There are two types of functions

### Normal functions
Normal functions are declared like this:
```js
function exampleFunction() {

}
```
and they can be executed like this:
```js
exampleFunction()
```
\
But usually functions don't just execute code. You can also put arguments in them and they can also return values.\
Example:
```js
function funcWithArgs(argument) { // In this case i put a name in the brackets and that will be available as a variable inside the function
    console.log(argument); // Log the argument value
}

funcWithArgs("some string"); // Execute the function with the argument "someString". In this case it will log the argument so that would be "someString"

function funcWithMoreArgs(argument1, argument2) { // Function with 2 arguments
    console.log(argument1, argument2); // Log both arguments value
}

funcWithMoreArgs("first string", "second string"); // Execute the function with the arguments "first string" and "second string"
```
\
And then they can also return values.\
Example:
```js
function funcThatReturns() {
    return "some value" // return "some value"
}

console.log(funcThatReturns()); // Logs "some value"
const x = funcThatReturns(); // Create a constant variable with the value that the function returns so in this case "someValue"
```

### Anonymous functions
Anonymous functions are just like normal functions but their defined differently.\
Example:
```js
const anonFunction = () => {

}
```
So a variable is created and then you set the variable to the function.\
you start with the brackets where you can put your arguments in, then an arrow `=>` to define the code that runs when the function is executed and then the curly brackets where you put the code in

## If statements
If statements can be used to check if a value is true.\
They start with `if` and can have multiple `else if` statements and optionaly at the end an `else` statement.\
If statements are like functions without the arguments and return value.\

There are also some logical operators:\
- `==` Equals value > This will check if the value is the same as another value but does not check if its the same type. Example: `1 == 1` will return true `1 == "1"` will also return true
- `===` Equals value and type > This will check if the value is the same as another value and if the type is the same. Example: `1 == 1` will return true but `1 == "1"` will return false
- `||` OR > Check if at least one of the values is true. Example: `1 == 5 || 10 < 11` In this case the whole thing will be true as one of the statements is true. 1 is not 5 and therefor `false` but 10 is less than 11 and therefor `true` and since we use the or operator if either is `true` the whole thing is `true` so this would be true
- `&&` AND > Check if all values are true. Example: `1 == 5 || 10 < 11` This will return `false` as one statement is `true` and one is `false`. 1 is not 5 and therefor `false` but 10 is less than 11 and therefor `true` and since we use the and operator if either is `false` the whole thing is `false`

Example:
```js
const x = 5;

if (x > 4) {
    console.log("x is higher than 4");
} else {
    console.log("x is or is less than 4");
}

if (x == 4) {
    console.log("x is 4");
} else if (x < 4) {
    console.log("x is less than 4");
} else if (x > 5) {
    console.log("x is greater than 5");
} else {
    console.log("x is 5 as its not 4, greater than 5 and less than 4");
}
```
