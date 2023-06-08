
# p++
This language is designed to be a Java like language for RaspberryPi that compiles to c++. The goal is to make development of RaspberryPi languages much easier and entuative for anyone from beginners to experts.

(if it works lol)

# Contents
 - [Syntax](#syntax)
    - [Comments](#comments)
    - [Types](#types)
    - [Functions](#functions)
    - [Basic operations](#basic-operations)
    - [Classes](#classes)
 - [Built in functions](#built-in-functions)
 - [Code examples]
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
```
These types are combined to create more complex types such as:
### Compound Types
```
Array
String
```
To fine one of these types use this syntax:
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
## RaspberryPi

## Dev/Debugging
Execute c++ code directly. AVOID USE OF THIS.
```
exec("/*Valid c++ code*/")
```

Calls the .toString() method if the data type is not primative.
```
print(/*Takes any data type*/)
```



l
l

l

l

l
```js
let name = "Jeff"
console.log(`Hello my name is ${name}`)
```

```c++

int main() {
    char name[4] = "Jeff"
    printf("My name is %c", name)

    return 1;
}

```