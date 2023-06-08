# p++

This language is designed to be a Java like language for RaspberryPi that compiles to c++. The goal is to make development of RaspberryPi languages much easier and entuative for anyone from beginners to experts.

(if it works lol)

.pip

# Contents

- [Syntax](#syntax)
  - [Comments](#comments)
  - [Types](#types)
    - [Primitive Types](#primitive-types)
    - [Compound Types](#compound-types)
      - [String](#string)
      - [Array](#array)
      - [Number](#number)
  - [Variables](#variables)
  - [Functions](#functions)
  - [Basic operations](#basic-operations)
  - [Classes](#classes)
  - [Loops](#loops)
  - [If & Else](#if--else)
- [Built in functions](#built-in-functions)
  - [Math](#math)
    - [Random](#random)
    - [Round](#round)
    - [Floor](#floor)
    - [Square](#square)
    - [Square Root](#square-root)
  - [Console](#console)
    - [Print](#print)
    - [Read](#read)
  - [RaspberryPi](#raspberrypi)
  - [Dev/Debugging](#devdebugging)
- [Code examples]
- [Compiler](#compiler)
- [To do list]

# Syntax

## Comments

First off lets start with comments so we can add helpful notes in later code snippets

### Inline:

```
// I am a comment
```

### Multiline:

```
/*
I am a comment
I am the second line!
*/
```

## Types

p++ has three primative data types.

### Primitive Types

```
int
decimal
char
bool
```

These types are combined to create more complex types such as:

### Compound Types

```
String
Array
Number
```

To fine one of these types use this syntax:

#### String

```
var exampleString:String = "Test"
```

A string is a group of characters.

#### Array

An array is a list of values. These values can be any data type.

```
var exampleArray:Array<String> = ["Test", "Test", "Test"];// This is an array of strings
```

#### Number

A number is a value that can be either an int or a decimal. It is mostly used in mathmatical operations where the type is not important.

```
var exampleNumber:Number = 15;
```

### Variables

```
// constants once defined can never be changed
const CONSTANT_VAR:String = "Test"

// Use the var keyword to define a normal variable
var name:String = "Test"

//simply update variables like this:
name = "Test 2"
CONST_VAR = "Test 2" // Throws error
```

## Functions

```
def functionName(param:TYPE):TYPE
^   ^             ^     ^     ^
1   2             3     4     5
```

1. Declare a function with the keyword "def"
2. Think of a name. Use camel case for these!
3. Write the name of your paramaters, add as many of these as you need
4. Add a colon followed by the param type.
5. Append another colon followed by a data type to set the return type. If this is not set the compiler will assume void.

### Example

```
def addNumbers(a:int, b:int):int {
    var sum:int = a + b;
    return sum;
}
```

This function takes two integer paramaters and returns the output of their sum.

## Basic Operations

All operations should work as expected. Bro if you dont know how pls go learn cause I don't wanna explain this...

## Loops

### For loop

```
for () {
    print();
}
```

### While loop

```
while (<condition>) {
    print();
}
```

## If & Else

```
if (<condition>) {
    print();
} else if (<condition>) {
    print();
} else {
    print();
}
```

## Classes

### class Definition

```
//Define class signiture:
class ClassName {
    // define class varaibles and stuff
    const CONSTANT_VAR:[TYPE] = [VALUE];

    /*
    This is the contructor and
    will be run once on class creation
    */
    init() {
        var name:String = "Kevin";
        var petsName:String;
        this.test = "String";
        this.id; // 15
    }
}
```

### How to use classes

```
class ClassName {
    const ID:int = 15;
    const NAME:String = "Kevin";
    var age:int = 0;

    init() {
        //contains a group of variables
        var petsName:String;
        this.test = "String";
        this.id; // 15
    }

    def age():void {
        this.age = this.age + 1;
    }
}

var testClass = new ClassName();
testClass.age();

```

# Built in functions

## Math

### Random

```
random(min, max)
```

Returns a random number between min and max

### Round

```
round(<number>)
```

Rounds a number to the nearest integer

### Floor

```
floor(<number>)
```

Rounds a number down to the nearest integer

### Square

```
sqr(<number>)
```

Returns the square of a number

### Square Root

```
sqrt(<number>)
```

Returns the square root of a number

### Trigonometry

```
sin(<number>)
cos(<number>)
tan(<number>)
```

Returns the sin, cos or tan of a number in radians

## Console

### Print

Calls the .toString() method if the data type is not primative.

```
print(/*Takes any data type*/)
```

### Read

```
read()
```

returns a string of the user input

## RaspberryPi

p++ will have directly integrated libraries with functions for gpio etc..

Both Pico And PI?? Different libriraries for each??

## Dev/Debugging

Execute c++ code directly. AVOID USE OF THIS.

```
exec("/*Valid c++ code*/")
```

## Other stuff

```js
let name = "Jeff";
console.log(`Hello my name is ${name}`);
```

```c++

int main() {
    char name[4] = "Jeff"
    printf("My name is %c", name)

    return 1;
}

```

# Compiler

## Usage

### Building

To build the file run the follwing command

```
builder build <file>
```

Running build without a file will build all files with the p++ file extension in the current directory.

```
builder build
```

### Running

To run the file run the follwing command. This will build and run the file.

```
builder run <file>
```
