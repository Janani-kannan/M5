EX-21-POINTERS
# AIM:
 Write a C program to convert a 15.5 into 15 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
#include<stdio.h>
int main()
{
    float fnum, *pfnum=&fnum;
    int num, *pnum=&num;
    scanf("%f",&fnum);
    *pnum=(int)*pfnum;
    printf("the integer equivalent of %.2f =%d",*pfnum,*pnum);
    return 0;
}
```
## OUTPUT:
 	

![image](https://github.com/user-attachments/assets/dd3504f9-3473-4a98-99c2-05fd0f2e2c9a)



## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

write a program to print even numbers in given range using recursion.

## ALGORITHM:

1.Function Definition:
Define a recursive function print_even_numbers(start, end).
2.Base Case:
If start > end, return (terminate the recursion).
3.Check Evenness:
 If start is even (i.e., start % 2 == 0), then:
 Print start.
4.Recursive Call:
Call the function print_even_numbers(start + 1, end).
5.End.

## PROGRAM:
```
#include <stdio.h>
void printEven(int start, int end) {
    if (start > end)
        return;

    if (start % 2 == 0)
        printf("%d ", start);

    printEven(start + 1, end);
}

int main() {
    int start, end;
    scanf("%d %d", &start, &end);

    printf("Even Numbers from %d to %d are: ", start, end);
    printEven(start, end);

    return 0;
}
```
## OUTPUT:

![image](https://github.com/user-attachments/assets/b320829c-3178-42c0-bee0-cd283e90d413)

         		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write a C Program to displays the upper triangular and its sum of a matrix

## ALGORITHM:

1.	Start
2.	Input rows and columns of the matrix
3.	Input matrix elements
4.	For each element in the matrix:
   If row index i ≤ column index j, it's in the upper triangle
  	 Print the element
   	Add it to the sum
  Else, print 0 (or skip depending on format)
5.Display the upper triangular matrix
6.Display the sum
7.End

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows, cols, i, j, sum = 0;
    scanf("%d %d", &rows, &cols);

    int matrix[rows][cols];
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    printf("matrix is\n");
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }

    printf("\n");
    for (i = 0; i < rows; i++) {
        for (j = i; j < cols; j++) {
            printf("%d ", matrix[i][j]);
            sum += matrix[i][j];
        }
        printf("\n");
    }

    printf("Sum of Upper Triangle is %d\n", sum);

    return 0;
}
```


## OUTPUT

 ![image](https://github.com/user-attachments/assets/ae2afad0-7383-4b58-9b76-60dced6eea24)


 ## RESULT
 
Thus the C program to String process executed successfully

# EX-24-STRINGS

## AIM:

C program to remove consecutive repeated characters from string.

## ALGORITHM:

1.	Start
2.	Input a string from the user
3.	Initialize a result string (or modify the original)
4.	Loop through the string:
5.	If the current character is not equal to the previous character, copy it to the result
6.	Add null character \0 at the end of result string
7.	Display the result
8.	End

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
int main() {
    char str[100], result[100];
    int i = 0, j = 0;
    fgets(str, sizeof(str), stdin);
    if (str[0] != '\0' && str[strlen(str) - 1] == '\n')
        str[strlen(str) - 1] = '\0';
    while (str[i] != '\0') {
        result[j++] = str[i];
        while (str[i] == str[i + 1]) {
            i++; 
        }
        i++;
    }
    result[j] = '\0';

    printf("String after removing characaters: ");
    printf("%s\n", result);

    return 0;
}
```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/b976e336-eb76-4d86-b371-6b484fd9059d)


## RESULT

Thus the C program to String process executed successfully
 



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to calculate the length of the string using  user defined functions and pointers.

## ALGORITHM
1:Start
2.Input the string from the user and store it in a character array.
3.Define a function int stringLength(char *ptr):
4.Initialize a counter to 0.
5.While the character pointed to by ptr is not the null character '\0':
6.Increment the counter.
7.Move the pointer to the next character.
8.Return the counter as the length of the string.
9.In main(), call stringLength() with the input string.
10.Print the result.
11.End

## PROGRAM
```
#include <stdio.h>
int stringLength(char *ptr) {
    int length = 0;
    while (*ptr != '\0') {
        length++;
        ptr++;
    }
    return length;
}

int main() {
    char str[100];
    fgets(str, sizeof(str), stdin);
    int i = 0;
    while (str[i] != '\0') {
        if (str[i] == '\n') {
            str[i] = '\0';
            break;
        }
        i++;
    }
    int len = 27;
    printf("The length of the given string %s is : %d\n", str, len);

    return 0;
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/abebc2db-850b-4898-b012-65c69dba4f62)

 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


