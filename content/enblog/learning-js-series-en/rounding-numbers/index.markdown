---
title: "#6: Rounding numbers"
weight: 3
subtitle: "#6: Notes on Rounding numbers"
excerpt: "#6: Notes on Rounding numbers"
date: 2023-04-30
draft: false
---

*Shall we start with notes on Rounding numbers?*

Ps: Notes based on Jonas Schmedtmann’s course on Udemy -- **No credits intended**



## Rouding Integers

## #1. Math.trunc()

1. **Aim:** Remove any decimals after the integral part of the number
2. **Mutates the array?** N/A
3. **Input:** a number
4. **Returns:** Returns the integral part of the a numeric expression, x, removing any fractional digits. If x is already an integer, the result is x.
5. **Does type coercion?** Yes!


```js
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1. x — A numeric expression.

// In practice:

console.log(Math.trunc(countriesSUM)); // returns 708

// Other examples:

console.log(Math.trunc(20.89)); // returns 20
console.log(Math.trunc(20.39)); // returns 20
```


<script type="text/javascript">
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1. x — A numeric expression.

// In practice:

console.log(Math.trunc(countriesSUM)); // returns 708

// Other examples:

console.log(Math.trunc(20.89)); // returns 20
console.log(Math.trunc(20.39)); // returns 20
</script>

## #2. Math.round()

1. **Aim:** Rounds to the next integer
2. **Mutates the array?** N/A
3. **Input:** a number
4. **Returns:** Returns a supplied numeric expression rounded to the nearest integer.
5. **Does type coercion?** Yes!



```js
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1. x — The value to be rounded to the nearest integer.

// In practice:

console.log(Math.round(countriesSUM)); // returns 708

// Other examples:


console.log(Math.round(countriesSUM)); // returns 708


console.log(Math.round(20.89)); // returns 21
console.log(Math.round(20.39)); // returns 20
console.log(Math.round('20.39')); // returns 20
```


<script type="text/javascript">
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1. x — The value to be rounded to the nearest integer.

// In practice:

console.log(Math.round(countriesSUM)); // returns 708

// Other examples:


console.log(Math.round(countriesSUM)); // returns 708


console.log(Math.round(20.89)); // returns 21
console.log(Math.round(20.39)); // returns 20
console.log(Math.round('20.39')); // returns 20
</script>

## #3. Math.ceil()

1. **Aim:** To round *up* a number
2. **Mutates the array?** N/A
3. **Input:** a number
4. **Returns:** Returns the smallest integer greater than or equal to its numeric argument.
5. **Does type coercion?** Yes!



```js
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1.@param x — A numeric expression.

// In practice:

console.log(Math.ceil(countriesSUM)); // returns 709

// Other examples:

console.log(Math.ceil(20.89)); // returns 21
console.log(Math.ceil(20.39)); // returns 21
console.log(Math.ceil('20.39')); // returns 21
```


<script type="text/javascript">
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1.@param x — A numeric expression.

// In practice:

console.log(Math.ceil(countriesSUM)); // returns 709

// Other examples:

console.log(Math.ceil(20.89)); // returns 21
console.log(Math.ceil(20.39)); // returns 21
console.log(Math.ceil('20.39')); // returns 21
</script>

## #4. Math.floor()

1. **Aim:** To round *down* a number
2. **Mutates the array?** N/A
3. **Input:** a number
4. **Returns:** Returns the greatest integer less than or equal to its numeric argument.
5. **Does type coercion?** Yes!



```js
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1.@param x — A numeric expression.

// In practice:

console.log(Math.floor(countriesSUM)); // returns 708

// Other examples:

console.log(Math.floor(20.89)); // returns 20
console.log(Math.floor(20.39)); // returns 20
console.log(Math.floor('20.39')); // returns 20
```


<script type="text/javascript">
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1.@param x — A numeric expression.

// In practice:

console.log(Math.floor(countriesSUM)); // returns 708

// Other examples:

console.log(Math.floor(20.89)); // returns 20
console.log(Math.floor(20.39)); // returns 20
console.log(Math.floor('20.39')); // returns 20
</script>

## #5. Math.floor()

1. **Aim:** To round *down* a number
2. **Mutates the array?** N/A
3. **Input:** a number
4. **Returns:** Returns the greatest integer less than or equal to its numeric argument.
5. **Does type coercion?** Yes!



```js
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1.@param x — A numeric expression.

// In practice:

console.log(Math.floor(countriesSUM)); // returns 708

// Other examples:

console.log(Math.floor(20.89)); // returns 20
console.log(Math.floor(20.39)); // returns 20
console.log(Math.floor('20.39')); // returns 20
```


<script type="text/javascript">
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1.@param x — A numeric expression.

// In practice:

console.log(Math.floor(countriesSUM)); // returns 708

// Other examples:

console.log(Math.floor(20.89)); // returns 20
console.log(Math.floor(20.39)); // returns 20
console.log(Math.floor('20.39')); // returns 20
</script>

> Note: Math.trunc() x Math.floor() <br>
1. They are equal when dealing with *POSITIVE* numbers. However, they aren't equal when dealing with *NEGATIVE* numbers <br>
2. With negative numbers, rounding works the other way around <br>
3. So, the tip is to use ```Math.floor()``` instead of ```Math.trunc()```


```js
console.log(Math.trunc(-50.2)) // - 50
console.log(Math.floor(-50.2)) // - 51 
```


<script type="text/javascript">
console.log(Math.trunc(-50.2)) // - 50
console.log(Math.floor(-50.2)) // - 51 
</script>

## Rouding floating point numbers (aka, decimals)

## #6. .toFixed()

1. **Aim:** To round the decimals 
2. **Mutates the array?** N/A
3. **Input:** a number
4. **Returns:** Returns a *string* representing a number in fixed-point notation.
5. **Does type coercion?** No!



```js
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1. fractionDigits — Number of digits after the decimal point. Must be in the range 0 - 20, inclusive.


// In practice:

console.log(countriesSUM.toFixed()); // 708
console.log(countriesSUM.toFixed(1)); // 708.5
console.log(countriesSUM.toFixed(2)); // 708.50
console.log(countriesSUM.toFixed(3)); // 708.497
console.log((-25.3684555585).toFixed(3)); // -25.368


// To return a number:

console.log(+countriesSUM.toFixed()); // 708
console.log(+countriesSUM.toFixed(1)); // 708.5
console.log(+countriesSUM.toFixed(2)); // 708.50
console.log(+(-25.3684555585).toFixed(3)); // -25.368
```


<script type="text/javascript">
// Countries' data:

const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81];

const countriesSUM = countriesPOP.reduce(
  (acc, country, i, arr) => acc + country,
  0
);

console.log(countriesSUM); // 708.4970000000001

// Parameters:

// 1. fractionDigits — Number of digits after the decimal point. Must be in the range 0 - 20, inclusive.


// In practice:

console.log(countriesSUM.toFixed()); // 708
console.log(countriesSUM.toFixed(1)); // 708.5
console.log(countriesSUM.toFixed(2)); // 708.50
console.log(countriesSUM.toFixed(3)); // 708.497
console.log((-25.3684555585).toFixed(3)); // -25.368


// To return a number:

console.log(+countriesSUM.toFixed()); // 708
console.log(+countriesSUM.toFixed(1)); // 708.5
console.log(+countriesSUM.toFixed(2)); // 708.50
console.log(+(-25.3684555585).toFixed(3)); // -25.368
</script>

&#128021; Au-au! This section will be written soon! 


