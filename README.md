EX-11-EMI-CALCULATOR
~~~
AIM
To write a program to prepare EMI calculator using function without return type and with arguments.

ALGORITHM
1.Start the program.
2.Read principal amount, rate of interest and months.
3.Pass these values as arguments to function.
4.Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.Display the result.
6.Stop the program.
~~~
PROGRAM
#include <stdio.h> #include <math.h>

// Function to calculate EMI void calculateEMI(float principal, float annualRate, int tenureMonths) { float monthlyRate = annualRate / (12 * 100); // Convert annual rate to monthly float emi;

emi = (principal * monthlyRate * pow(1 + monthlyRate, tenureMonths)) / 
      (pow(1 + monthlyRate, tenureMonths) - 1);

printf("Monthly EMI: ₹%.2f\n", emi);
}

int main() { float principal, rate; int tenure;

// Input
printf("Enter loan principal amount (₹): ");
scanf("%f", &principal);

printf("Enter annual interest rate (%%): ");
scanf("%f", &rate);

printf("Enter loan tenure in months: ");
scanf("%d", &tenure);

// Call EMI calculator
calculateEMI(principal, rate, tenure);

return 0;
}
~~~
OUTPUT
~~~
Enter loan principal amount (₹): 500000 Enter annual interest rate (%): 7.5 Enter loan tenure in months: 60 Monthly EMI: ₹10018.97
~~~
RESULT
~~~
Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
~~~
EX-12-FIBONACCI-SERIES
AIM
To write a C program to generate the Fibonacci series for the value 6.

ALGORITHM
1.Start the program.
2.Read number of terms to display.
3.Add the previous two terms and store it in new term.
4.Assign 2nd term to 1st term and 3rd term to 2nd term.
5.Repeat steps 3 and 4 n number of times.
6.Display the result.
7.Stop the program.
~~~
PROGRAM
#include <stdio.h>

int main() { int a = 0, b = 1, c, i, n = 6;

printf("Fibonacci Series up to %d terms:\n", n);
printf("%d %d ", a, b);

for (i = 3; i <= n; i++) {
    c = a + b;
    printf("%d ", c);
    a = b;
    b = c;
}

return 0;
}
~~~
OUTPUT
~~~
Fibonacci Series up to 6 terms: 0 1 1 2 3 5
~~~
RESULT
~~~
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
~~~
EX-13-ONE-DIMENSIONAL-ARRAY
AIM
To write a C program to read n elements as input and print the last element of the array.

ALGORITHM
1.Start the program.
2.Read a variable.
3.Read the array values n number of times.
4.Print the last element.
5.Stop the program.
~~~
PROGRAM
#include <stdio.h>

int main() { int n;

// Input number of elements
printf("Enter number of elements: ");
scanf("%d", &n);

int arr[n]; // Declare array of size n

// Input n elements into the array
printf("Enter %d elements:\n", n);
for (int i = 0; i < n; i++) {
    scanf("%d", &arr[i]);
}

// Print the last element
printf("Last element: %d\n", arr[n-1]);

return 0;
}
~~~
OUTPUT
~~~
Enter number of elements: 5 Enter 5 elements: 1 2 3 4 5 Last element: 5
~~~
RESULT
~~~
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
~~~
EX-14-POSITIVE-ARRAY-ELEMENTS
AIM
To write a C Program to count total number of positive elements in an array.

ALGORITHM
1.Start the program.
2.Read a variable.
3.Read the array values n number of times.
4.If the array value can be divided by 2 then increment count by 1.
5.Display result.
6.Stop the program.
~~~
PROGRAM
#include <stdio.h>

int main() { int n, positiveCount = 0;

// Input number of elements
printf("Enter number of elements: ");
scanf("%d", &n);

int arr[n]; // Declare array of size n

// Input n elements into the array
printf("Enter %d elements:\n", n);
for (int i = 0; i < n; i++) {
    scanf("%d", &arr[i]);
}

// Count positive elements
for (int i = 0; i < n; i++) {
    if (arr[i] > 0) {
        positiveCount++;
    }
}

// Output the result
printf("Total positive elements: %d\n", positiveCount);

return 0;
}
~~~
OUTPUT
~~~
Enter number of elements: 5 Enter 5 elements: 1 -2 3 4 -1 Total positive elements: 3
~~~
RESULT
~~~
Thus the program to count total number of positive elements in an array has been executed successfully.
~~~
EX -15 - Replace All Even Elements With 'E' In One Dimensional Array
Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

Algorithm:
1.Input the array: Read the size of the array. Input the elements of the array.
2.Iterate through the array: For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.Replace even elements with 'E': If an element is even, replace that element with the character 'E'.
4.Output the updated array: Print the updated array after replacements.
~~~
Program:
#include <stdio.h>

int main() { int n;

// Input number of elements
printf("Enter number of elements: ");
scanf("%d", &n);

int arr[n]; // Declare array of size n

// Input n elements into the array
printf("Enter %d elements:\n", n);
for (int i = 0; i < n; i++) {
    scanf("%d", &arr[i]);
}

// Replace even elements with 'E' (represented by -1 for this example)
for (int i = 0; i < n; i++) {
    if (arr[i] % 2 == 0) {
        arr[i] = -1;  // We use -1 as a placeholder for 'E'
    }
}

// Print the updated array
printf("Updated array:\n");
for (int i = 0; i < n; i++) {
    if (arr[i] == -1) {
        printf("E ");
    } else {
        printf("%d ", arr[i]);
    }
}

printf("\n");
return 0;
}
~~~
Output:
~~~
Enter number of elements: 6 Enter 6 elements: 1 2 3 4 5 6 Updated array: 1 E 3 E 5 E
~~~
Result:
~~~
Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.
~~~
