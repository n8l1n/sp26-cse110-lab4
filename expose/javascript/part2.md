# Part 2: A little More of a Challenge...

1. Line 12 prints the value stored in `i` which is `3`. We pass a list of prices containing 3 values, so in the for loop, we loop from i = 0 to i = 2 which is less than three. Then i is incremented to 3 which is not < prices.length resulting in the end of the loop..
2. Line 13 prints 150. For each interation, we take the i'th value of the prices and apply the discount, but we overwrite the value previously stored in `discountedPrice`. Since `discountedPrice` is declared as a `var`, it can be accessed from outside the if statement and anywhere in the function and the final operation performed and stored in `discountedPrice` is 300 * (1 - 0.5) since 300 is the last value stored in `prices`.
3. Line 14 also prints 150. During each iteration, the value stored in `finalPrice` is overwritten with the rounded value from discount price and once again, the last value written into `finalPrice` before it is outputted is 150.
4. This function returns `discounted` which stores [ 50, 100, 150 ] because for each iteration, we push the calculated `finalPrice` into the `discounted` list.
5. In line 12, an error occurs: `ReferenceError: i is not defined`. This is because `i` is declared with `let` inside of the for loop code block (more specifically, the parameters of the for loop), which means that `i` is only visible inside of that block (block-local/block-scoped variable). On line 12, `i` is being referenced outside of the block which no longer sees `i` (it is no longer in scope).
6. On line 13, an error occurs: `ReferenceError: discountedPrice is not defined`. This is because discountedPrice is declared inside of the for loop. Variables declared using `let` are block-local which means that they are only visible within the block they are declared in `{...}`.
7. Line 14 will print 150. The variable `finalPrice` is declared within the function, but outside of any loops or if statements which means that it can be used anywhere within the function. When the program is run, it will enter the for loop where for each iteration, finalPrice is updated to store the price at index `i` of `prices` after the discount has been applied. The last operation written into `finalPrice` is the rounded value of `prices[2]` after the discount has been applied, which is 150.
8. This function will return [ 50, 100, 150 ]. For each iteration of the for loop, `finalPrice` is pushed into the `discounted` list. This means that each price in `discounted` will store the value of each entry in `prices` after the discount has been applied.
9. Line 11 will result in an error: `ReferenceError: i is not defined`. Once again, this is because `i` is declared with `let` inside of the for loop expressions which means it is block-scoped to the for loop. In line 11, `i` is out of scope.
10. Line 12 will print 3 since it stores the length of `prices`. Prices is passed storing 3 elements so when the program is run and that length is assigned to the `const length` variable.
11. This function will return [ 50, 100, 150 ]. For each iteration of the for loop, the `discountedPrice` is calculated then pushed into `discounted`. Although `discounted` is declared as a `const`, the contents can be modified as long as the variable itself is not reassigned.

## Data Types

12. Notations:
    A.
    B.
    C.
    D.
    E.