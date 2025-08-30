# Javascript cheatsheet

## Variables

Variables are used to store values and use them later on in the program.

There are two types of variables:
- `let` - create a variable which is mutable.
- `const` - create a variable which is not mutable

```js
let myVariable = 10;
myVariable = 15; // myVariable is not 15

const PI = 3.14;
PI = 5.21; // ERROR cannot reassign a value to const.
```

> [!note]
> When working with a const object the variable will point to a
> refernce of the object. Therefor you can't reassign to a new object
> BUT you can change the object values.

```js
const obj = {a:5};
obj = {b:2} // Won't work

const obj = {a:5};
obj.a = 7; // Will work.
```

## Data types

- `Number` - any number and floating point numbers.
- `String` - any text inside a double or single quotes.
- `Boolean` - true/false values.

## String literals

String literals give's the developer a better way to write strings
which might contain a variable.

String literals uses backticks ``` ` ```

```js
let var1 = 'Hello'
let var2 = 'World'

var1 + ', ' + var2 + '!'; // without string literals
`${var1}, ${var2}!` // with string literals
```

## Functions

A block of code which can be excuted ethier once or multiple times inside the program.

```js
function functionName(param1,param2,paramN){
    //the body of the function.
}
```

functions can also be used to return values.

```js
// The function will return a greeting message with the name provided.
function greetingMessage(name){
    return `Greeting, ${name}`
}
```

### Default values

You can set default values to parametrs for default behavior.

```js
function greetings(name,message = 'Greeting,') {
    console.log(`${message} ${name}`)
}
```

### Anonymous functions

If you know you will use the function only once you can create an anonymous function.

```js
setTimeout(function(){
    console.log('2 seconds passed')
}, 2000)
```

From ES6 we can use the fat arrow function

```js
setTimeout(() => {
    console.log('2 seconds passed')
}, 2000)
```

You can also immediatly call anonymous function:

```js
const hello = (name => {
    const message = `Greeting, ${name}`
    return message
})('John')

// hello = `Greeting, John`
```

> [!note]
> Nowadays you will mostly see fat arrows functions unless they are
> a part of an object.

## Conditions

Conditions are used to execute a part of a program only if something is true.

```js
let laptopAmount = 500;
let money = 800;

if (money >= laptopAmount){
    console.log('Getting a new computer')
} else {
    console.log('Not getting a new computer')
}
```

The condtion above will chec if there is enough money to buy a new computer
- if there is engough money buy a new one.
- otherwise don't buy a new one.

There are also switch statements which are used if there are multiple cases
```js
let a = 2;

switch(a) {
    case 1:
        a = 'one'
        break;
    case 2:
        a = 'two'
        break
    default:
        a = 'none'
        break
}
```

- It will check if a is equal to the case statment and execute accordingly.
- `default` case will execute if none of the above match.
- **Make sure to use `break` at the end of each case**
  - Unless you need multiple cases to execute the same code.

There are several logical operators:
| Operator | $ Description                                                             |
|----------|---------------------------------------------------------------------------|
| >        | Greater than                                                              |
| >=       | Greater than or equal                                                     |
| <        | Less than                                                                 |
| <=       | Less than or equal                                                        |
| ===      | strict equality checks if both types and values are match                 |
| !==      | strict inequality checks if both types are the same but value is not      |
| ==       | normal equality will convert both to one type and then check equality     |
| !=       | normal inequality will convert both to one type and then check inequality |

And there are 3 conditional operators:
| Operator | Description                                                                    |
|----------|--------------------------------------------------------------------------------|
| `&&`     | AND, will check if both the left and right side are true                       |
| `||`     | OR, will check if one side is true, will stop if the left side is already true |
| `!`      | NOT, negate the value - true becomes false and false becomes true              |

### Teranry operators

Teranry operators are used to for a short decision in which it will return the value at the end.

```js
condition ? return_if_true : return_if_false;
```

```js

let firstNumber = 10
let secondNumber = 20
let biggerNumber;

if (firstNumber > secondNumber){
    biggerNumber = firstNumber
} else {
    biggerNumber = secondNumber
}

// It can shrink to:

let biggerNumber = firstNumber > secondNumber ? firstNumber : secondNumber

```