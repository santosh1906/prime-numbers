SanfoundryMenu


C Program to Find whether a Number is Prime or Not using Recursion
« PrevNext »
This is a C program to find whether a number is prime or not using recursion.

Problem Description
The following C program, using recursion, finds whether the entered number is a prime number or not.

Problem Solution
A prime number is an integer that has no integral factor but itself and 1.

advertisement

Program/Source Code
Here is the source code of the C program to find an element in a linked list. The C Program is successfully compiled and run on a Linux system. The program output is also shown below.

/*
 * C Program to find whether a Number is Prime or Not using Recursion
 */
#include <stdio.h>
 
int primeno(int, int);
 
int main()
{
    int num, check;
    printf("Enter a number: ");
    scanf("%d", &num);
    check = primeno(num, num / 2);
    if (check == 1)
    {
        printf("%d is a prime number\n", num);
    }
    else
    {
        printf("%d is not a prime number\n", num);
    }
    return 0;
}
 
int primeno(int num, int i)
{
    if (i == 1)
    {
        return 1;
    }
    else
    {
       if (num % i == 0)
       {
         return 0;
       }
       else
       {
         return primeno(num, i - 1);
       }       
    }
}
