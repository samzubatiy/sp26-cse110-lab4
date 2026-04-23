# Part 1
1. 20 (nothing special happening here)
2. 20 (var is funciton scoped)
3. You shouldn't use var because it does not have block scope. This means variables can leak out of loops or if statements, causing bugs and naming conflicts that are hard to fix.
4. 20 (just like the first q)
5. Returns an error. It returns a error because let is block-scoped. This means the result variable only exists inside the if block, so line 13 cannot see it.
6. Returns an error. It returns a error because variables declared with const cannot be reassigned. Since result was initialized to 0, trying to change it to 20 crashes the code before it even gets to line 9.
7. Returns an error. The program already crashed at line 7. But even if it didn't, const is block-scoped just like let, so line 13 wouldn't be able to see the result variable outside of the if block anyway.