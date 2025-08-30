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

[!NOTE]
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

