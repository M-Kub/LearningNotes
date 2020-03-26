# Elixir Basics

Functions are the primary tool for building a program in functional languages like Elixir. They receive data, comlete operations and return values.


To reduce complexity, functions should have these properties:

- Immutable values.
- The result of the function, is affected only by functions arguments.
- The function doesn't generate effects beyond the value it returns.

Those functions are called pure functions.


## Example

```
add2 = fn (n) -> n + 2 end
add2.(2)
... => 4
```
---


