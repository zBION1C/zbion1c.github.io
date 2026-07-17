---
title: Types
---
# Objects
Objects are the most basic non-primitive type in javascript. An `object` refers to any javascript value with properties, which is almost all of them. To define an object we list its properties and their types:
```typescript
function printPoint(pt: {x: number, y: number}) {
  console.log("pt.x");
  console.log("pt.y");
}
printPoint({x: 3, y: 7});
```
Objects can have **optional** properties. To do this, add a `?` after the property name:
```typescript
function printName(obj: { first: string, last?: string}) {
  // Do something
}
// Both ok!
printName({first: "Bob"});
printName({first: "Alice", last: "Allison" });
```
One important thing you have to remember is that if you try to access a property that does not exist, you'll get the value `undefined`. For this reason, always check for undefined properties!

# Combining types
Typescript enables the definition of new types combining existing ones.

## Union type
A union type is a type formed from two or more other types, representing values that may be any one of those types. We refer to each of these types as the union’s members.
```typescript
function printId(id: number | string) {
  console.log("Your ID is: " + id);
}
```
Typescript will only allow an operation if it is valid for **every** member of the union.
The solution to this restriction is [[Narrowing|narrowing]] the union with code.
