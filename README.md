# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int M, N;

    // Input values
    printf("Enter the starting number (M): ");
    scanf("%d", &M);

    printf("Enter the ending number (N): ");
    scanf("%d", &N);

    printf("Even numbers from %d to %d are:\n", M, N);

    // Ensure starting from an even number
    if (M % 2 != 0)
        M++;  // If M is odd, move to next even number

    // Loop through and print even numbers
    for (int i = M; i <= N; i += 2) {
        printf("%d ", i);
    }

    printf("\n");
    return 0;
}

```
## OUTPUT:


![alt text](c1.png)







## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter number of rows: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {      // outer loop → number of rows
        for (int j = 1; j <= i; j++) {  // inner loop → print '*' in each row
            printf("* ");
        }
        printf("\n");  // move to next line
    }

    return 0;
}

```
## OUTPUT:

![alt text](c2.png)



## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
```
#include <stdio.h>

// Function declarations
void add(int a, int b);
void subtract(int a, int b);

int main() {
    int num1, num2;

    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    // Function calls
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}

// Function definitions

// Performs addition (with argument, no return)
void add(int a, int b) {
    int sum = a + b;
    printf("Sum = %d\n", sum);
}


// Performs subtraction (with argument, no return)
void subtract(int a, int b) {
    int diff = a - b;
    printf("Difference = %d\n", diff);
}

```


## OUTPUT:


![alt text](c3.png)



## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int num, digit, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    // Use a for loop to extract digits and find sum of odd ones
    for (; num > 0; num = num / 10) {
        digit = num % 10;          // extract last digit
        if (digit % 2 != 0) {      // check if odd
            sum += digit;
        }
    }

    printf("Sum of odd digits = %d\n", sum);

    return 0;
}

```


## OUTPUT:

![alt text](c4.png)


## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
```
#include <stdio.h>

// Function declaration
int factorial(int n);

int main() {
    int num, result;

    printf("Enter a number: ");
    scanf("%d", &num);

    if (num < 0)
        printf("Factorial is not defined for negative numbers.\n");
    else {
        result = factorial(num);  // Function call
        printf("Factorial of %d = %d\n", num, result);
    }

    return 0;
}

// Function definition
int factorial(int n) {
    int fact = 1;

    for (int i = 1; i <= n; i++) {
        fact = fact * i;
    }

    return fact;   // return the result to main()
}
```


## OUTPUT:
![alt text](c5.png)

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
