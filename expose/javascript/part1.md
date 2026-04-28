# Expose

## Part 1: A Quick Introduction...

### Var Declaration
1. Line 9 prints `values added:  20`
2. Line 13 prints `final result:  20`
3. The reason that var should not be used is because it has no block scoping allowing it to ignore code blocks. This might lead to naming conflicts and scoping issues since they can be accessed from anywhere within the function they are defined in (and the hoisting property can cause issues since you can use the var even if it was declared later).
4. Line 9 prints `values added:  20`
5. Line 13 returns an error: `ReferenceError: result is not defined.`
    This indicates that result is no longer defined (out of scope) and that is because `result` was defined using `let` within the if statement block making `result` only visible in that block.

### Const Declaration
6. Line 9 is unable to print anything due to an error occuring in line 7 (where execution stops): `TypeError: Assignment to constant variable.`
    This error occurs since line 7 is attempting to store the value of `num1 + num2` in `result` which was previous declared as a `const` in line 5. Constants cannot be reassigned, hence, the error.
7. Line 13 is also unable to print anything as a result of the same error described in **question 6** which stops the execution of the program