# Function pointers in C

A function pointer is a type of pointer that points to the memory address of a function.

Example
<hr>

`fun.c`

```C

#include <stdio.h>

void fun(int a)
{
printf("The value of a is %d\n", a);
}

int main()
{
void (*ptr_fun)(int) = &fun;
/*
 * (*ptr_fun) is a pointer to a function that takes in one integer argument.
 * (*ptr_fun) is passed the memory address of func.
 */

/* The above line is equivalent of following two
       void (*fun_ptr)(int);
       fun_ptr = &fun; 
*/


 (*ptr_fun)(100);
return (0);
}

```

