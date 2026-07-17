---
title: Basics
---
Typescript is simply a typed version of javascript. This note serve as a basic introduction to the esoteric typescript/javascript syntax and as a map to more complex concepts.

# Variable declaration
In javascript there are three different ways to declare a variable: `var`, `let` and `const`.

Variables declared with the **var** keyword can have global scope or [[Functions|function]] scope.
`var`-declared variables can be re-declared within the same scope.
```typescript
var x = 10; // Global scope

function f(): void {
  var y = 20; // Function scope
}
```
The `let` keyword is an improvement of `var`. It solves the problem of unwanted re-declaration present when using `var`. `let` is blocked scoped and cannot be **re-declared** in the same block.

```typescript
let x: number = 10;

if (times > 3) {
  let x: number = 60;
  console.log(x) // prints: 60
}

console.log(x) // prints: 10
```
The `const` keyword is used to declare constant variables, i.e. variables that cannot be re-assigned or re-declared. If an [[Types#Objects|objects]] is declared with `const` the whole variable cannot be re-assigned or re-declared, but its properties can be changed.
```typescript
const point = {
  x: 42,
  y: 69,
}

point.x = 13; // This can be done
```
