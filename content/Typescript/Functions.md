---
title: Functions
---

# Functions basics
Functions are defined like this in typescript:
```typescript
function greet(name: string): void {
  console.log("Hello" + name.toUpperCase() + "!!");
}
```
In typescript functions are first-class citizens, in the sense that they are considered **values** like any other value.
