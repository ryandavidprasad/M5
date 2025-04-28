# EX-21 - Pointers  
## AIM:  
Write a C program to convert a 23.65 into 25 using pointer.

## PROGRAM:
```c
#include <stdio.h>
int main() {
    double num = 23.65;
    double *ptr = &num;
    *ptr = 25.0;
    printf("Updated value: %.2f\n", num);
    return 0;
}
```

## OUTPUT:
```
Updated value: 25.00
```

## RESULT:  
Thus the program to convert 23.65 into 25 using pointer has been executed successfully.

# EX-22 - Functions and Storage Class (Recursion)  
## AIM:  
Write a C program to calculate the Product of first 12 natural numbers using Recursion.

## PROGRAM:
```c
#include <stdio.h>

unsigned long long calculateProduct(int n) {
    if (n == 1)
        return 1;
    else
        return n * calculateProduct(n - 1);
}

int main() {
    int n = 12;
    unsigned long long product;
    product = calculateProduct(n);
    printf("Product of first 12 natural numbers: %llu\n", product);
    return 0;
}
```

## OUTPUT:
```
Product of first 12 natural numbers: 479001600
```

## RESULT:  
Thus the program to calculate the product of first 12 natural numbers using recursion has been executed successfully.


# EX-23 - Arrays and Its Operations  
## AIM:  
Write a C Program to find Sum of each row of a Matrix.

## PROGRAM:
```c
#include <stdio.h>

int main() {
    int rows, cols, i, j, sum;
    printf("Enter rows and columns of matrix: ");
    scanf("%d%d", &rows, &cols);

    int matrix[rows][cols];

    printf("Enter elements of matrix:\n");
    for(i = 0; i < rows; i++) {
        for(j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    for(i = 0; i < rows; i++) {
        sum = 0;
        for(j = 0; j < cols; j++) {
            sum += matrix[i][j];
        }
        printf("Sum of row %d = %d\n", i + 1, sum);
    }
    return 0;
}
```

## OUTPUT:
```
Enter rows and columns of matrix: 2 3
Enter elements of matrix:
1 2 3
4 5 6
Sum of row 1 = 6
Sum of row 2 = 15
```

## RESULT:  
Thus the program to find sum of each row of a matrix has been executed successfully.


# EX-24 - Strings (Pyramid Pattern)  
## AIM:  
Write a C program to print a pyramid string pattern.

## PROGRAM:
```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows, i, j, k;
    printf("Enter a string: ");
    scanf("%s", str);
    printf("Enter number of rows: ");
    scanf("%d", &rows);

    int len = strlen(str);

    for(i = 1; i <= rows; i++) {
        for(j = 1; j <= i; j++) {
            for(k = 0; k < len; k++) {
                printf("%c ", str[k]);
            }
        }
        printf("\n");
    }
    return 0;
}
```

## OUTPUT:
```
Enter a string: PROGRAM
Enter number of rows: 5
P R O G R A M 
P R O G R A M P R O G R A M 
P R O G R A M P R O G R A M P R O G R A M 
P R O G R A M P R O G R A M P R O G R A M P R O G R A M 
P R O G R A M P R O G R A M P R O G R A M P R O G R A M P R O G R A M 
```

## RESULT:  
Thus the C program to process string into a pyramid pattern has been executed successfully.


# EX-25 - Displaying Arrays Using Pointers  
## AIM:  
Write a C program to read and display an array of any 6 integer elements using pointer.

## PROGRAM:
```c
#include <stdio.h>

int main() {
    int arr[10], n, i;
    int *parr;

    parr = arr;

    printf("Enter number of elements (max 10): ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", (parr + i));
    }

    printf("Elements are:\n");
    for(i = 0; i < n; i++) {
        printf("%d ", *(parr + i));
    }
    printf("\n");

    return 0;
}
```

## OUTPUT:
```
Enter number of elements (max 10): 6
Enter 6 elements:
1 2 3 4 5 6
Elements are:
1 2 3 4 5 6
```

## RESULT:  
Thus the C program to read and display an array of any 6 integer elements using pointer has been executed successfully.
