# Part 2
## Part 2. A Little More of a Challenge...
1. 3 (Loop terminates when i is no longer less than 3, leaving i with a value of 3. Var is function scoped)
2. 150 (discountedPrice was declared with var, it is function-scoped. 150 is the value from the last iteration of the loop (300 * 0.5))
3. 150 (finalPrice was declared with var at the top of the function, so it is accessible here and holds the value from the final loop iteration)
4. The function will return the array [50, 100, 150]. The code runs without errors and correctly pushes the discounted prices into the array (prices * 0.5).
5. This will cause a error. The variable i is declared with let, which means it is block-scoped. It only exists inside the for loop, so line 12 cannot see it.
6. This will cause a error. The variable discountedPrice is declared with let, which means it is block-scoped. It only exists inside the for loop, so line 13 cannot see it.
7. 150 (the variable finalPrice was declared with let at the very beginning of the function. Because it was declared in the main function block, it is accessible anywhere inside the function)
8. The function will return the array [50, 100, 150]. Assuming the error lines from the previous questions are commented out or ignored, the core logic works perfectly because the discounted array and finalPrice are in the proper scope.
9. his will cause a error. The variable i is declared with let, which means it is block-scoped. It only exists inside the for loop, so line 11 cannot see it.
10. 3 (the variable length was declared with const at the top of the function. Its block scope is the entire function, so it is accessible here and holds the length of the prices array)
11. The function will return the array [50, 100, 150]. Even though discounted is a const, JavaScript allows you to modify the contents of a const array using .push(). Also, declaring const discountedPrice inside the loop works because a brand new block scope is created for every single iteration of the loop.

## Data Types
12A. student.name
12B. student['Grad Year']
12C. student.greeting()
12D. student['Favorite Teacher'].name
12E. student.courseLoad[0]

## Basic Operators & Type Conversion
### Arithmetic
13A. '32', since one of the values is a string and the operator is a plus sign, JavaScript does string concatenation. The integer 2 is mapped to its string exact representation and attached to the end.
13B. 1, since the minus sign is only used for math, JavaScript converts the string '3' into a number and subtracts 2 from it.
13C. 3, the plus sign here does math because 3 is an integer. In numeric conversions, null becomes 0. So it does 3 + 0.
13D. '3null', since '3' is a string and we are using a plus sign, it does string concatenation. The null value is converted into the string 'null' and attached.
13E. 4, because 3 is an integer, it does math. In numeric conversions, true maps to 1. So it does 1 + 3.
13F. 0, this is a math operation. false maps to 0, and null also maps to 0. So it does 0 + 0.
13G. '3undefined', since '3' is a string and we use the plus sign, it does string concatenation. undefined becomes the string 'undefined' and is attached.
13H. NaN, since it is a minus sign, it tries to do math. '3' becomes the number 3, but undefined becomes NaN (Not a Number) when doing math. 3 minus NaN results in NaN.

### Comparison
14A. true, when comparing a string and a number, JavaScript converts the string '2' to the number 2. 2 is greater than 1.
14B. false, when comparing two strings, JavaScript compares them dictionary-style (character by character). The first character of '2' is greater than the first character of '12' (which is '1').
14C. true, the loose equality operator (==) automatically does type conversion. It turns the string '2' into the number 2, making them equal.
14D. false, the strict equality operator (===) checks both the value and the data type. Since one is a number and the other is a string, it immediately returns false without converting anything.
14E. false, with loose equality, the boolean true is converted to the number 1. 1 does not equal 2.
14F. true, the Boolean() function converts any non-zero number to true. So it is comparing true === true. Since both are the exact same value and the exact same data type (boolean), it returns true.

15. The == operator is the loose equality operator. It automatically converts the data types of the variables to match before it compares their values. The === operator is the strict equality operator. It checks both the value and the exact data type without doing any automatic conversions. If the data types are different, === will instantly return false.

### Functions
17. The result will be the array [2, 4, 6]. The modifyArray function loops through each element of the input array [1, 2, 3]. During each iteration, it takes the current element and passes it into the callback function, which in this case is the doSomething function. The doSomething function takes that number, multiplies it by 2, and returns the new value. That doubled number is then pushed into the newArr array. After the loop finishes doubling every item, the function returns the new array.

### setInterval(), setTimeout(), clearTimeout()
19.  1, 4, 3, 2 (vertically). First, it instantly prints 1. Then, it sees the timeout for 2 and pushes it to the background to wait 1 second. Next, it sees the timeout for 3 and pushes it to the background to wait 0 seconds. The main code then prints 4. Now that the main code is done, JavaScript sees the 0-second timeout is ready, and prints 3. Finally, the last timeout finishes and it prints 2.