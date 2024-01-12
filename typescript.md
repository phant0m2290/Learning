# Typescript
Typescript is a version of javascript but with types. You can assign variables a type and they can only be a value of that type. This results in less errors.\
Typescript also makes classes actually useful. You have classes in javascript and you can use them if you want but they ar not really useful.

## Types

### All the types in typescript

- boolean
- number
- string
- null
- Array\<type\> > can also be defined as type[]. Examples: `Array<string>` or `string[]`
- Any > Anything except never
- Unknown > Literally anything
- Void > used for functions if they return nothing
- Tuple > an array existing of specific types in a specific order. Example: `[string, number]`
- Never > A function that never returns aka keeps running until the program exits or a function that exits the program
- Object > A json object
- [Enum](#enums)

### How to use types

Types can be assigned to variables like this:
```ts
let stringVar: string = "some string" // Define the variable "stringVar" with the type string and set the value to "some string"

stringVar = 5; // This will give an error as you can only set the value to a string and not a number
```

You can also assign multiple types to a variable like this:
```ts
let x: boolean | string; // Define the variable "x" with the types "boolean" and "string" and do'nt set the value
x = "some string"; // Set x to "some string" (no error as x can be a string)
x = false; // Set x to false (no error as x can be a boolean)
x = 5; // Set x to 5. This will give an error as x cannot be a number
```

You can also define your own types. They can be aliases for types or a selection of string that the value can be.\
Example:
```ts
type SomeType = string | number;
let someVar: SomeType; // Create a variable with the type alias "SomeType" which allows the variable to be a string or number

type AnotherType = "some string" | "some other string" | 10 | false;
let anotherVar: AnotherType; 
/* 
 * Create a variable with the type "AnotherType" which allows it to be "some string", "some other string", 10 or false.
 * This does not care about the types but only the values and the variable cannot be anything else than one of these values.
*/
```

## Interfaces
Interfaces are just json types. You can define an interface, assign it as a type to a variable and add a json value.\
Example:
```ts
interface Data {
    id: number;

    name: string;

    optional?: string; 
    // The question mark means that the value is optional so you do'nt need to define it.
    // This does mean that it can be the assigned type of a string or undefined. 
    // This means you always need to check if the value exists before you use it or you will get an error
}

const data: Data = {
    id: 5,
}
// This will give an error as its missing the name value.

const data: Data = {
    id: 5,
    name: "some name",
}
// This is valid as the "optional" entry is optional

const data: Data = {
    id: 5,
    name: "some name",
    optional: "optional entry"
}
// This is also valid
```

## Types in functions
Functions can have arguments and can return values but in typescript both of these values can have types.\
Assigning types to arguments is pretty simple. Its just like normal variables.\
Return types are defined after the parenthesis and before the code. When this return type is defined the function can only return that type of value. If the function does not return anything `void` is used.\
Example:
```ts
function typedFunction(x: string): boolean {
    // Create a function with an argument called "x" with a type of string and a return type of boolean

    if (x == "Hello, World!") return true;
    else return 0; // Gives an error because the return type is a boolean
}
```

## Enums
Enums are basically the same as the types with the specific values but a bit differed.\
They can just be values or be assigned a key and value.\
Examples:
```ts
enum OnlyValues {
    one,
    two,
    three
}

enum KeyValues {
    one = 1,
    two = 2,
    three = 3
}
```

When using the Value only enum you need to use the enum in if statements. When using the key value enum you can use the enum or the value assigned to the key.
Examples:
```ts
let onlyVal = OnlyValues.one;

if (onlyVal == OnlyValues.one) console.log("onlyVal is OnlyValues.one");

let keyVal = KeyValues.one;
if (keyVal == KeyValues.one) console.log("keyVal is KeyValues.one");
if (keyVal == 1) console.log("keyVal is KeyValues.one aka 1");
```

## Classes
Classes are very big. Therefor i will explain them in multiple parts.

**WORK IN PROGRESS**