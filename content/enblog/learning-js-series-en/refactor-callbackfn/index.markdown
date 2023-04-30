---
title: "#2: Refactoring a callback function"
weight: 3
subtitle: "#2: Notes on Refactoring a callback function"
excerpt: "#2: Notes on Refactoring a callback function"
date: 2023-04-30
draft: false
---

*Shall we start with notes on Refactoring a callback function ?* <br>

**Aim:** Rewrite the same *callbackfn* separately and pass it as an argument to others callback functions  

Ps: Notes based on Jonas Schmedtmann’s course on Udemy -- **No credits intended**




## #1: .filter(), .some() and .every()


```js
// Create arrays: 

const countriesSpelled = ['B','r','a','z','i','l']
const countries = ['Brazil', 'Denmark', 'USA', 'Italy', 'Colombia', 'Argentina']
const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81] // in milions of people

// Create a function to return only populations above 200 milion:

const isBiggerThan200 = pop => pop > 200;

// In Use:

// Filter:
console.log(countriesPOP.filter(isBiggerThan200)); // [214.3, 331.9]
// Some:
console.log(countriesPOP.some(isBiggerThan200)); // T
// Every:
console.log(countriesPOP.every(isBiggerThan200)); // F
```


<script type="text/javascript">
// Create arrays: 

const countriesSpelled = ['B','r','a','z','i','l']
const countries = ['Brazil', 'Denmark', 'USA', 'Italy', 'Colombia', 'Argentina']
const countriesPOP = [214.3, 5.857, 331.9, 59.11, 51.52, 45.81] // in milions of people

// Create a function to return only populations above 200 milion:

const isBiggerThan200 = pop => pop > 200;

// In Use:

// Filter:
console.log(countriesPOP.filter(isBiggerThan200)); // [214.3, 331.9]
// Some:
console.log(countriesPOP.some(isBiggerThan200)); // T
// Every:
console.log(countriesPOP.every(isBiggerThan200)); // F
</script>


&#128021; Au-au! This is a good way to stick to DYI! 

