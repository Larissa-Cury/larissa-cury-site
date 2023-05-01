---
title: "#8: Adding Timers"
weight: 3
subtitle: "#8: Notes on Adding Timers"
excerpt: "#8: Notes on Adding Timers"
date: 2023-04-30
draft: false
---

*Shall we start with notes on Adding Timers ?*

Ps: Notes based on Jonas Schmedtmann’s course on Udemy -- **No credits intended**

Ps2: Notes also based on [Mdn][1] -- **No credits intended**



## A) setTimeout()

1. **Aim:** Sets a timer which executes a function or specified piece of code once the timer expires.
2. **Mutates the array?** N/A
3. **Input:** N/A
4. **Returns:** Returns **timeoutID**, which is a positive integer value which identifies the timer created by the call to setTimeout(). This value can be passed to ```clearTimeout()``` to cancel the timeout.
5. **Does type coercion?** Yes! (cf. MDN post)

>
Note 1: Js works asynchronously, hence, because of this mechanism, code execution *DOENS'T* stop when we call ```setTimeOut()```  <br>
>



```js
//Parameters:

// 1) functionRef - A function to be executed after the timer expires.

// 2) code - An alternative syntax that allows you to include a string instead of a function, which is compiled and executed when the timer expires. This syntax is not recommended for the same reasons that make using eval() a security risk.

// 3) delay Optional - The time, in milliseconds that the timer should wait before the specified function or code is executed. If this parameter is omitted, a value of 0 is used, meaning execute "immediately", or more accurately, the next event cycle.

// param1, …, paramN Optional - Additional arguments which are passed through to the function specified by functionRef.

// In use:
// Set X miliseconds to print a string: 

// A) Prints after 3s

setTimeout(() => console.log('a string'), 3000); // Appears after 3s
console.log('Wait for it...') // Immediately

// B) Evaluate from a prompt:

const myQuestion = prompt('What are your fruits?');


 if (myQuestion === 'Oranges') {
console.log('Correct Answer ✅ '), 5000)
 } else {
   setTimeout(() => console.log('Wrong Answer, try again ❌'), 5000);
 }

// C) Passing arguments 

// All arguments that we passed after the delay will be arguments to the functions

const fruits = ['orange', 'apples'];

const fruitTimer = setTimeout(
  (f1, f2) => console.log(`Your order containing ${f1} and ${f2} will be delivered soon`),
  3000,
  ...fruits // put the elements comma separated
);

console.log('Waiting...'); // Immediatedly
```


<script type="text/javascript">
//Parameters:

// 1) functionRef - A function to be executed after the timer expires.

// 2) code - An alternative syntax that allows you to include a string instead of a function, which is compiled and executed when the timer expires. This syntax is not recommended for the same reasons that make using eval() a security risk.

// 3) delay Optional - The time, in milliseconds that the timer should wait before the specified function or code is executed. If this parameter is omitted, a value of 0 is used, meaning execute "immediately", or more accurately, the next event cycle.

// param1, …, paramN Optional - Additional arguments which are passed through to the function specified by functionRef.

// In use:
// Set X miliseconds to print a string: 

// A) Prints after 3s

setTimeout(() => console.log('a string'), 3000); // Appears after 3s
console.log('Wait for it...') // Immediately

// B) Evaluate from a prompt:

const myQuestion = prompt('What are your fruits?');


 if (myQuestion === 'Oranges') {
console.log('Correct Answer ✅ '), 5000)
 } else {
   setTimeout(() => console.log('Wrong Answer, try again ❌'), 5000);
 }

// C) Passing arguments 

// All arguments that we passed after the delay will be arguments to the functions

const fruits = ['orange', 'apples'];

const fruitTimer = setTimeout(
  (f1, f2) => console.log(`Your order containing ${f1} and ${f2} will be delivered soon`),
  3000,
  ...fruits // put the elements comma separated
);

console.log('Waiting...'); // Immediatedly
</script>

>
Aside note: In order to make it 'Wait' we should first print what we want and them remove the element. Js has a ```wait()``` function that *doesn't* do it for us. We have to print and remove after X ms.
>

## B) clearTimeout()

1. **Aim:** Cancels a timeout previously established by calling setTimeout().
2. **Mutates the array?** N/A
3. **Input:** timeoutID
4. **Returns:** Returns ****, which is a positive integer value which identifies the timer created by the call to setTimeout(). This value can be passed to ```clearTimeout()``` to cancel the timeout.
5. **Does type coercion?** N/A

>
We need the input to be an object from ```setTimeout()```
>


```js
//Parameters:

// 1) timeoutID - The identifier of the timeout you want to cancel. This ID was returned by the corresponding call to setTimeout().

// In use:
// Clear if contains 'apples'

// All arguments that we passed after the delay will be arguments to the functions

const fruits = ['orange', 'apples'];

const fruitTimer = setTimeout(
  (f1, f2) => console.log(`Your order containing ${f1} and ${f2} will be delivered soon`),
  3000,
  ...fruits // put the elements comma separated
);

console.log('Waiting...'); // Immediatedly

// clear: 

if (ingredients.includes('apples')) clearTimeout(fruitTimer); 

// fruitTimer WON'T be executed!
```


<script type="text/javascript">
//Parameters:

// 1) timeoutID - The identifier of the timeout you want to cancel. This ID was returned by the corresponding call to setTimeout().

// In use:
// Clear if contains 'apples'

// All arguments that we passed after the delay will be arguments to the functions

const fruits = ['orange', 'apples'];

const fruitTimer = setTimeout(
  (f1, f2) => console.log(`Your order containing ${f1} and ${f2} will be delivered soon`),
  3000,
  ...fruits // put the elements comma separated
);

console.log('Waiting...'); // Immediatedly

// clear: 

if (ingredients.includes('apples')) clearTimeout(fruitTimer); 

// fruitTimer WON'T be executed!
</script>


## C) setInterval()

1. **Aim:** Repeatedly calls a function or executes a code snippet, with a fixed time delay between each call.
2. **Mutates the array?** N/A
3. **Input:** N/A
4. **Returns:** Returns an **interval ID** (a numeric, non-zero value which identifies the timer) which uniquely identifies the interval, so you can remove it later by calling ```clearInterval()```
5. **Does type coercion?** N/A (I guess)


```js
//Parameters:

// 1) func - A function to be executed every delay milliseconds. The first execution happens after delay milliseconds.

// 2) code - An optional syntax allows you to include a string instead of a function, which is compiled and executed every delay milliseconds. This syntax is not recommended for the same reasons that make using eval() a security risk.

// 3) delay Optional - The time, in milliseconds (thousandths of a second), the timer should delay in between executions of the specified function or code. Defaults to 0 if not specified. See Delay restrictions below for details on the permitted range of delay values.

// 3) arg0, …, argN Optional - Additional arguments which are passed through to the function specified by func once the timer expires.

// In use:

// Note: there's a bug with this timer, but I cannot fix it right now -- I'll improve it afterwards :)

// A) Setting a countdown:

const myClock = function () {
  const fixBug = function () {
    // Ongoing message:

    const timeRunin = console.log(`Time is running!`);

    // Finish Countdown:

    if (time === 0) {
      clearInterval(timer);
      // Message: 
      console.log(`Time is Up!`);
    }

    // Remove one 1s every second

    time = time - 1; // time--;

    // console.log(time);
  };

  // Create time:
  let time = 60; // 1 min

  // Call the timer every second (1000 ms)
  fixBug();
  const timer = setInterval(fixBug, 1000);
};

myClock();

// Returns:

<!-- Time is running! script.js:1347 -->
<!-- Live reload enabled.  -->
<!-- (60) Time is running! script.js:1347 -->
<!-- Time is Up! script.js:1354 -->

// Prints Time is running 60 times and prints Time is Up! When time === 0

// B) Display the current time EVERY 1000 ms 

// setInterval(function () {
//   const now = new Date();
//   console.log(now);
// }, 1000);
```


<script type="text/javascript">
//Parameters:

// 1) func - A function to be executed every delay milliseconds. The first execution happens after delay milliseconds.

// 2) code - An optional syntax allows you to include a string instead of a function, which is compiled and executed every delay milliseconds. This syntax is not recommended for the same reasons that make using eval() a security risk.

// 3) delay Optional - The time, in milliseconds (thousandths of a second), the timer should delay in between executions of the specified function or code. Defaults to 0 if not specified. See Delay restrictions below for details on the permitted range of delay values.

// 3) arg0, …, argN Optional - Additional arguments which are passed through to the function specified by func once the timer expires.

// In use:

// Note: there's a bug with this timer, but I cannot fix it right now -- I'll improve it afterwards :)

// A) Setting a countdown:

const myClock = function () {
  const fixBug = function () {
    // Ongoing message:

    const timeRunin = console.log(`Time is running!`);

    // Finish Countdown:

    if (time === 0) {
      clearInterval(timer);
      // Message: 
      console.log(`Time is Up!`);
    }

    // Remove one 1s every second

    time = time - 1; // time--;

    // console.log(time);
  };

  // Create time:
  let time = 60; // 1 min

  // Call the timer every second (1000 ms)
  fixBug();
  const timer = setInterval(fixBug, 1000);
};

myClock();

// Returns:

<!-- Time is running! script.js:1347 -->
<!-- Live reload enabled.  -->
<!-- (60) Time is running! script.js:1347 -->
<!-- Time is Up! script.js:1354 -->

// Prints Time is running 60 times and prints Time is Up! When time === 0

// B) Display the current time EVERY 1000 ms 

// setInterval(function () {
//   const now = new Date();
//   console.log(now);
// }, 1000);
</script>

## D) clearIntervalout()

>
Works similiarly to ```clearTimeout()```
>
<br>


&#128021; Au-au! Timers are **REALLY** important for Psycholinguist's experiments! 

[1]:https://developer.mozilla.org/en-US/

