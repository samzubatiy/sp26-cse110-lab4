# Devtools part 2
1. What was the bug?
The bug is that the values pulled from the HTML input fields are automatically grabbed as strings, not numbers. When the calculateSum function tries to add them together ("2" + "3"), JavaScript performs string concatenation instead of mathematical addition, resulting in "23".

2. How would you fix it?
To fix it, I need to convert the string variables into numeric data types before adding them together. I can do this by wrapping num1 and num2 in the Number() function.