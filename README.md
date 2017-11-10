# Dan's Cheat Sheets!

## Functions Essentials

1. **Functions Essentials:**
    * [Simple No Args - 3 examples](#simple-no-args---3-examples)
    * [Single Argument - 5 examples](#single-argument---5-examples)
    * [Multiple Arguments - 3 examples](#multiple-arguments---3-examples)
    * [Destructuring](#destructuring)
1. **Object Expressions/Literals**
    * [Inline Methods/Functions - 4 methods](#inline-methodsfunctions---4-methods)
    * [Class Methods/Functions - 4 methods](#class-methodsfunctions---4-methods)
  
  
------------------

### Simple No Args - 3 examples

```js
function one() {
  return 1; 
}
// ES6 Fat Arrow Functions
const one = () => { return 1; }
const one = () => 1;
//                ^ Look ma! No `return` - simply by omitting curly braces
```

```js
// Example Output:
one() //=> 1
```

### Single Argument - 5 examples

```js
// 5 Identical ways to accept a *single* argument in your functions
function echo(val) {
  return val;
}
const echo = (val) => { return val; }
const echo = val   => { return val; }
const echo = (val) => val;
const echo = val   => val;
```

```js
// Example Output:
echo('hello') //=> 'hello'
```

### Multiple Arguments - 3 examples

```js
// 3 Identical ways to accept *multiple* arguments in your functions
function combine(a, b) {
  return a + b;
}
const combine = (a, b) => { return a + b; }
const combine = (a, b) => a + b;
```

```js
// Example Output:
combine('abc', '123') //=> 'abc123'
```


### Destructuring

```js
// Use Destructuring to 'unpack' value(s) from an object:
function greeting(user) {
  return 'Hello ' + user.name;
}
function greeting({name}) {
  return 'Hello ' + name;
}

// With Arrow function:
const greeting = ({name}) => { return 'Hello ' + name; }
// Getting Multiple arguments:
const greeting = ({firstName, lastName}) => { return 'Hello ' + firstName + ' ' + lastName; }
const greeting = ({firstName, lastName}) => 'Hello ' + firstName + ' ' + lastName
```


## Designing Objects (and related Class-ish things)


------------------

## Functions in Objects

### Inline Methods/Functions - 4 methods

```js
const numberMethods = {
// Pick one syntax/technique:
  one: function() { return 1; },
  one() { return 1; },
  one = () => { return 1; },
  one = () => 1,
}

numberMethods.one() //=> 1
```

### Class Methods/Functions - 4 methods

```js
class NumberMethods {
  constructor() {
    // often needed
  },
// **Pick one syntax/technique:**
  one: function() { return 1; },
  one() { return 1; },
  one = () => { return 1; },
  one = () => 1,
}

let nm = new NumberMethods()
nm.one() //=> 1
```







