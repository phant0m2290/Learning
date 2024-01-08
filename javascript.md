# Learning javascript
## Index
- [Data Types](#data-types)
    - [Strings](#strings)
    - [Numbers](#numbers)
    - [Booleans](#booleans)
    - [JSON](#json-javascript-object-notation)
    - [Undefined and Null](#undefined-and-null)
- [Logging](#logging)
- [variables](#variables)
- [Basic math](#basic-math)


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
"SomeOther" += "String" // This will become "SomeOtherString"

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

4 == 4 // Checks if 4 equals to 4 by using == (Equals to). This will be true as 4 equals to 4

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

key = "otherValue" // From now on someJson.key is "otherValue". Any code before this still sees someJson.key as "value", everything after this will see it as "otherValue"
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

function exampleFunction() { return "someValue" }
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
Math is occurs also a thing. Its very easy
# **WIP**
