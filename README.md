# JavaScript 1

## Student Learning Objectives

<details>
<summary>JavaScript Basics</summary>
<ul>
<li>Students can recite and identify the primitive JavaScript datatypes.
<ul>
  <li>Number</li>
  <li>String</li>
  <li>Boolean</li>
  <li>Array</li>
  <li>Object</li>
  <li>Undefined</li>
  <li>Null</li>
</ul>
</li>
<li>Students can describe the difference between null and undefined</li>
<li>Students can describe the difference between weak (dynamic) and strong (static) typing.</li>
<li>Students can declare a variable</li>
<li>Students can assign a variable a value</li>
<li>Students can reassign variable values</li>
</ul>
</details>

<details>
<summary>Complex Datatypes</summary>
<ul>
<li>Arrays
<ul>
<li>Students can create an array literal</li>
<li>Students can hard code values into an array literal</li>
</ul>
</li>
<li>Objects
<ul>
<li>Students can create an object literal</li>
<li>Students can add multiple key/value pairs to an object</li>
</ul>
</li>
</ul>

</details>

<details>
<summary>If Statements and Functions</summary>
<ul>
<li>If... else
<ul>
<li>Students can declare if...else if... else blocks</li>
<li>Students can nest if statements</li>
<li>Students can use logical operators (&&, ||, ===)</li>
</ul>
<li>Functions
<ul>
<li>Students can create a function expression</li>
<li>Students can create a function declaration</li>
<li>Students can invoke a function</li>
<li>Students can return a value (String literal, array literal, object literal, function, variable, etc.) from a function</li>
<li>Students can describe the difference between parameters and arguments</li>
</ul>
</li>
</ul>

</details>

<details>
<summary>Scope, Let, and Const</summary>
  
* Scope
  * Students can access variables across scopes (local function scope to global scope)
* Let & Const
  * Students can declare let and const variables
  * Students can use let and const to create block-scoped local variables
</details>

---

## Javascript 1 lecture notes

### Introduction to JavaScript

---

In this lecture we introduce the basics of JavaScript, which, together with HTML and CSS make up the bulk of the internet. While HTML and CSS allow us to display information and style how it looks, JavaScript allows us to make things happen on our websites. Any interactivity or dynamic functionality of a website is usually created with JavaScript.

> Note: JavaScript is regularly updated. The most significant update in recent years is known as ES6. Newly added features to ES6 can be found at [ECMAScript 6: New Features: Overview and Comparison](http://es6-features.org/#Constants)
> As you continue to study and learn more about JavaScript, it will be beneficial to know which features were added in ES6, and how they compare to previous versions. You will also want to continuously stay up-to-date with the most recently released features of JavaScript.

### Javascript Basics

#### Variables

---

Variables are the primary mechanism for storing data in JavaScript. Once a variable has been declared, it can be referenced later in the file.

Variables can be declared using the `var`, `let`, or `const` keywords in the following format:

```js
var num = 10
```

- In this example, if we reference `num` later in our file, we will actually be referencing the value, which is 10. You can assign any data type to a variable and variables can even be reassigned later in the file. For example:

```js
num = 15
```

- Notice that referencing `num` with the assignment operator `=` allows me to change its value. From here on, the value of num is 15. This can only be done with variables that have been previously declared

> NOTE: While it is possible to reassign a variable to a value of a different data type, it is generally not best practice to do so.

It is also possible to declare a variable without giving it a value. To do so, you simply declare the variable without providing a value, for example:

```js
var name
```

- This will initialize a variable for us but not provide it a value. If we attempt to reference it before providing a value, we will receive `undefined`.
- Variables in JavaScript are declared using camel case, meaning that the first word will be entirely lowercase, capitalizing the first letter of each subsequent word. To declare a variable using more than one word, you would format it like this:

```js
var numToKeepTrackOf = 20
```

#### Data Types

---

In JavaScript, data is represented using the following data types:

- **Number**
- **String**
  - Contained within single `''` or double `""` quotes, or backticks.
  - Usually used to hold words, sentances, or other predefined data.
- **Boolean**
  - `true` or `false`
- **Undefined**
  - Indicates that a variable has been initialized but has not yet been given a value.
- **Null**
  - Indicates that the value of the variable is `null`.
  - Note: This is different from undefined in that `null` is a value representing nothing, while undefined means there is no value provided.
- **Array**
  - Can be thought of as a list.
  - An array can contain any data type or even a mix of data types.
  - Contained witin brackets `[]` with each value separated by a comma.
  - Example:
  ```js
  var arrayOfNumbers = [1, 2, 3, 4, 5]
  var arrayOfStrings = ['brown', 'purple', 'green', 'yellow']
  ```
  - Values in an array are referenced using _bracket notation_.
    - This means, to access a specific value in an array, we provide the following: `Array[index]`
    - For example: to access the string `brown` in the array `arrayOfStrings` I would reference it as `arrayOfStrings[0]` because arrays are zero-indexed, meaning the first item in the array is located at index 0.
- **Object**
  - A collection of **key value pairs** with each key representing the name of a piece of data and the value being the value of that key.
  - Keys are also referred to as properties.
  - Contained within a set of curly brackets `{}`,
  - Keys are declared inside of an object by using a colon `:`.
  - Each key value pair is separated by a comma `,`.
  - Key value pairs can contain any data type.
  - Objects are used to represent collections of data that go together, for example:
    ```js
    var person = {
      name: 'Andrew',
      age: 27,
      married: true,
      friends: ['Jonathan', 'Josh', 'Spencer'],
    }
    ```
  - Values in objects are usually referenced using _dot notation_.
    _ For example: to access the `name` property on the object `person`, I would reference it as `person.name` which would give me the string `'Andrew'`
    _ New key value pairs can be added to an existing object using dot notation. For example, to add a `pets` property to our `person` object we can just say:
    `js person.hasPets = false`
    > Note: Numbers, Strings, Booleans, Undefined, and Null are referred to as primitive data types because they only contain one thing. Objects and Arrays are referred to as complex data types because they each contain many values.

### If statements and functions

##### If statement and functions allow us to execute code in sections referred to as code blocks. A code block is defined by the use of curly brackets `{}`

>

#### If Statements

---

If statements execute code based on if a certain condition is met. This is determined by the use of logical operators. The most common logical operators are:

- `>` and `>=` meaning greater than, and greater than or equal to. Usually used to compare two numbers
- `<` and `<=` meaning less than or less than, and less than or equal to. Usually used to compare numbers.
- `===` or the equality operator. Used to check exact equality of two values. Should only be used on primitive data types.
- `!==` or the inequality operator. Used to check for inequality of two values. Should only be used on primitive data types.
- `&&` or the and operator. Used to check if two separate conditions evaluate to true.
- `||` or the or operator. Used to check if either of two separate conditions evaluate to true.

The condition for an if statement is contained within parentheses `()` while the code to be executed is contained in curly brackets `{}`. An example of an if statement could be:

```js
if (2 === 2) {
  console.log('Math still works')
}
```

> As long as 2 is equal to 2, when we execute this file, the string `'Math still works'` will be printed to the console. However, if we write the following if statement:

```js
if (2 === 2 && 2 === 4) {
  console.log('Math is broken')
}
```

> Because, 2 will never be equal to both 2 and 4, we will never see this console log.

You can also provide `else` and `else if` statements to an if statement to handle exceptions. To build on our previous examples we could say:

```js
if (2 === 2 && 2 === 4) {
  console.log('Math is broken')
} else {
  console.log('Math still works')
}
```

> In this case we would see the second console log.

Else if statements are useful when comparing many conditions and are structured identially to regular if statements. For example:

```js
var num = 50

if (num >= 0 && num < 25) {
  console.log('Greater than zero, less than 25')
} else if (num >= 25 && num < 100) {
  console.log('Greater than 25, less than 100')
} else {
  console.log('Greater than 100')
}
```

> Depending on the value assigned to the `num` variable, we will see a different console log.

### Functions

---

Functions are reusable pieces of code that we can use to execute code blocks whenever they are invoked.

Functions can be written using either a function declaration or an expression.

A function declaration uses the following format:

```js
function nameOfFunction() {
  //Code to execute
}
```

A function expression uses this format:

```js
var nameOfFunction = function() {
  //Code to execute
}
```

> Note: You will learn some of the differences between function declarations and function expressions later in the course.

Functions are invoked by referencing the function name and pairing it with a pair of parentheses `()`. Think of these parentheses as the button you are pushing to invoke the function. For example, to invoke our above written function we simply type:

```js
nameOfFunction()
```

> Typing this invokes the function and executes any code written inside of it.

Functions can be set up to receive parameters, or values that will change depending on when the function is invoked. For example, here's a function that is set up to add two numbers together when invoked:

```js
function addTwo(num1, num2) {
  return num1 + num2
}
```

> The function takes in two numbers and returns their sum. `num1` and `num2` are "parameters", or placeholders, for whatever numbers end up being passed into the function. 
> This function could be invoked as follows:

```js
addTwo(2, 2) //Returns 4
addTwo(3, 3) //Returns 6
addTwo(5, 5) //Returns 10
```

> Functions are thus reusable. When functions are invoked, the values passed into it are called "arguments", they are what are actually used in the function in place of the parameters.

The `return` keyword is used to determine the value that is returned by the function. A function can return any data type, or even another function. When functions are invoked, they become equal to their `return` value, and can consequently be assigned to a variable. For example:

```js
var a = addTwo(2, 2) //Variable a is now assigned a value of 4
var b = addTwo(3, 3) //Variable b is now assigned a value of 6
```

> The `return` keyword prevents any code below it from executing. It effectively kicks us out of the function immediately when hit. Make sure your `return` statement is placed in a way that doesn't prevent intended behavior from happening.

> A final example:

```js
var name = 'Matt'
var name2 = 'Matias'

function sayHi(person) {
  return 'Hello, ' + person + '!'
  //We are joining multiple strings together into a larger string.
  //Joining strings together is called "concatenation"
}

//What would be the value of the following variable declarations?

var hiAndrew = sayHi(name)
var hiJonathan = sayHi(name2)
var hiBob = sayHi('Bob')
```

> Remember: Functions and if statements can also be nested inside of each other. The possibilities are infinite!

### Scope, Let, and Const

#### Scope

---

Scope is an incredibly important topic in Javascript because it determines what has access to the variables we delcare. The rule of thumb is that code blocks are able to look up in scope but not down. For example:

```js
var name = 'Andrew'

function sayHi(person) {
  var greeting = 'Hello, ' + person + '!'
  return greeting
}
```

> In this example, the function `sayHi` is able to use the variable `name` because it is part of the "global scope". Any variable that is declared in the global scope is available anywhere in our file.
>
> However, if we attempted to access our `greeting` variable outside of the function `sayHi`, we would be unable to do so because when we create a new code block, we create a new scope. We are able to "look out" into more general scopes, but not able to "look down" into more specific scopes.

#### Let and Const

---

With ES6, developers were given new ways to make variable declarations, the `let` and `const` keywords. Each have special properties. For the most part, `let` can be used just like `var`. `const` is unique in that it prevents the variable from being reassigned a value. `const` makes its value constant. Both `let` and `const` are block scoped, as opposed to `var` which is globally scoped. 

#### let

---

```js
let num = 10
```

> The main difference between `let` and `var` is that `var` is functionally scoped, and `let` is block scoped. For example:

```js
function doThing() {
  var a = 'Dog'
  console.log(a)
  //Prints 'Dog' to the console
  if (true) {
    var a = 'Cat'
    console.log(a)
    //Prints 'Cat' to the console
  }
  console.log(a)
  //Prints 'Cat' to the console
}

function doThing() {
  let a = 'Dog'
  console.log(a)
  //Prints 'Dog' to the console
  if (true) {
    let a = 'Cat'
    console.log(a)
    //Prints 'Cat' to the console
  }
  console.log(a)
  //Prints 'Dog' to the console
}
```

> Note: Keep in mind this is just an example. It is not a good idea to reuse variable names across various scopes, each unique variable should have an appropriate name. Good naming convention is one of the most important habits of a good developer.

#### const

---

`const` is a little different from `let` in that it cannot be reassigned after being declared. However, if an object or an array is assigned to a `const` variable, you can change their contents (properties on an object, indicies on an array). Let's see an example:

```js
const num = 10

num = 'ten'
//ERROR: Reassignment to constant variable.
//This will crash your code.

const person = {
  name: 'Andrew',
  age: 27,
  married: true,
}

person.name = 'Fred'
//This will work just fine
```

> It is generally speaking good practice to declare variables using `const`, using `let` only when needed, and avoiding `var` when possible. That said, there are valid use cases for each of `var`, `let`, and `const`, so there is no one size fits all approach to variable declaration. Ultimately, you will need to understand the differences between the three, and determine which fits best in a given scenario.  

### Additional Resources

---

#### General

---

- [JavaScript \| MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript) - General docs for JavaScript. MDN should be your first step when investigating any new JavaScript topic
- [JavaScript basics - Learn web development \| MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics) - The ultimate beginners guide to JavaScript, including instructions on connecting JavaScript and HTML.
- [Codewars](https://www.codewars.com/dashboard) - Great resource to practice problem solving and aquaint yourself with basic JavaScript concepts.
- [Repl.it](https://repl.it/~) - Code sandbox to practice JavaScript.

#### Videos

---

- [Traversy Media Javascript Intro](https://www.youtube.com/watch?v=hdI2bqOjy3c&list=PLillGF-RfqbbnEGy3ROiLWk7JMCuSyQtX&index=2&t=0s) - An introduction to many of the topics covered here.
  > Although this video is long, watching it will deepen your understanding of the discussed topics and prepare you for the more advanced topics we will be covering very soon.
