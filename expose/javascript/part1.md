# Expose

## Part 1: A Quick Introduction...

1. Line 9 prints `values added:  20`
2. Line 13 prints `final result:  20`
3. The reason that var should not be used is because it has no block scope allowing it to ignore code blocks. This might lead to naming conflicts and scoping issues since they can be accessed from anywhere within the function they are defined in.
4. Line 9 prints `values added:  20`
5. Line 13 returns an error: `ReferenceError: result is not defined`
    This indicates that result is no longer defined and that is because `result` was defined using `let` within the if statement block making `result` only visible in that block.
6. 