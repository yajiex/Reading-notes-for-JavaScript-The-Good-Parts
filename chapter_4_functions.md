# Chapter 4: Functions
* Every function object is created with a `prototype` property. Its value is an object with a `constructor` property whose value is the function.
* A function always returns a value. If the return value is not specified, then `undefined` is returned.
* If the function was invoked with the `new` prefix and the return value is not an object, then `this` (the new object) is returned instead.
* Some languages offer the tail recursion optimization. This means that if a function returns the result of invoking itself recursively, then the invocation is replaced with a loop, which can significantly speed things up. Unfortunately, JavaScript does not currently provide tail recursion optimization. Functions that recurse very deeply can fail by exhausting the return stack:

