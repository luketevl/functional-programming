# functional-programming
Learn about functional programming

# Material
- https://www.quora.com/What-is-a-side-effect-in-programming
- https://egghead.io/lessons/javascript-redux-pure-and-impure-functions
- https://wiki.haskell.org/Pointfree

## Pure Functions
- Have **inputs** and **outputs** well defined
```
function square(x){
  return x * x;
}
```
- _Don't have_ **side-effects**
- _Whenever_ your entry is 5 return will be _the same_.
```
func(3); // Result WHENEVER is 4
function func(x) {
  return x + 1;
}
```

## Hight Order Functions
- The functions that:
  - They operate on other functions
  - Received as a parameters
  - Return functions
  ```
  let calculate = function(fn, x, y){
    return fn(x, y);
  }
  ```
## Map
- The function **invoke** a callback and _return one new array with result_, apply item by item
```
const numbers = [1, 2, 3];
const square = x => x * x;
const squaredNumbers = numbers.map(square); // [1, 4, 9]
```

## Filter
- The function **invoke** a callback and _return one new array with result_, return the **filter** the elements in initial array with base in function calback.
```
const numbers = [1, 4, 7, 10];
const isBiggerThanFour = value => value > 4 ;
const numbersBiggerThanFour = numbers.filter(isBiggerThanFour); // [7, 10]
```

# Reduce
- The function received with parameters _callback_ functions and a _initial value_, transform the array in _unique value_
```
const numbers = [1, 2, 3];
const sum = (x, y) => x + y ;
const numbersSum = numbers.reduce(sum, 0); //6
```

# Currying
- _Transform_ the function with _multiples parameters_ in the _sequency_ the functions that have **one** _parameter_
```
const greeting = greet => name => `${greet} ${name}`;
const hello = greeting('Hello');

hello('World'); // Hello World
```

# Compose
- **Compose** small functions and create _complex_ functions, more reuse
```
const compose = (f, g) => x => f(g(x));

const toUpperCase = x => x.toUpperCase();
const exclaim = x => x + '!';

const angry = compose(toUpperCase, exclaim);

angry('ahhh'); // AHHH!
```
