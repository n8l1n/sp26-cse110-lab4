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
    
    A. student.name

    B. student['Grad Year']

    C. student.greeting()

    D. student['Favorite Teacher'].name

    E. student.courseLoad[0]

## Basic Operators & Type Conversion
13. Arithmetic

    A. `"32"` - Since '3' is a string, 2 is coerced into '2' for string concatenation.

    B. `1` - The subtraction results in a numeric conversion where '3' becomes 3.

    C. `3` - null is coerced to 0 for the numeric addition

    D. `"3null"` - null turns into "null" and gets concatenated because '3' is a string.

    E. `4` - true becomes 1 in numeric coercion since 3 is a number

    F. `0` - both false and null are coerced numerically to 0

    G. `"3undefined"` - undefined is coerced into "undefined" and concatenated since '3' is a string.

    H. `NaN` - undefined is coerced to NaN and any arithmetic operation involving NaN results in NaN.

14. Comparison
    
    A. `true` - since different types are being compared, JavaScripts convert them to numbers

    B. `false` - since both values being compared are strings, we will compare the strings character by character (dictionary/lexicographical order) starting with '2' < '1' which is not true, resulting in false being returned. 

    C. `true` - different types are being compared in this problem, so they are converted to numbers since this is a regular equality operator.

    D. `false` - this time, a strict equality operator is being used, so the values will be compared without converting them. The number 2 is NOT equal to the string '2'.

    E. `false` - since these values are different types, and we are using the regular equality operator, they are converted to numbers. true becomes 1 which is NOT equal to 2.

    F. `true` - Boolean(2) computes to true since any non-zero number is true. This means that the expression essentially becomes true === true.

15. In javascript the `==` (regular equality operator) does not differentiate values by their types. If the operands being compared are different types, they are converted to numbers before being compared. The `===` (strict equality operator) checks the equality without converting the type. If the operands are different types, false is returned.

## Loops

16. **See part2-question16.js**

## Functions

17.  [ 2, 4, 6 ] will be returned after the function executes with the given parameters.  When the function is called, for each element in the array, the result of calling the callback function with that element is pushed into `newArr`. In this case, the callback function is `doSomething` which takes the argument, doubles it, and returned it. From here, it is pushed into `newArr`. Once this has been done for each element in `array`, `newArr` will contain all of  `array`'s elements but doubled by the callback. Then, `newArr` is returned.