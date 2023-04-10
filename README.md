# Dynamic-Memory-c

Dynamic Memory Allocation can be defined as a procedure in which the size of a data structure (like Array) is changed during the runtime.

malloc() method 

• The "malloc" or "memory allocation" method in C is used to dynamically allocate a single large block of memory with the specified size.
- It returns a pointer of type void which can be cast into a pointer of any form.
• It doesn't Initialize memory at execution time so that it has initialized each block with the default garbage value initially.

Syntax:

           ptr = (cast-type*) malloc (byte-size)
For Example:

           ptr = (int*) malloc(100 * sizeof(int))
Since the size of int is 4 bytes, this statement will allocate 400 bytes of memory. And, the pointer ptr holds the address of the first byte in the allocated memory.


calloc() function 

• The calloc() function allocates multiple block of requested memory.
It initially initialize all bytes to zero.
It returns NULL if memory is not sufficient.

The syntax of calloc() function is given below:

          ptr=(cast-type*)calloc(number, byte-size)  
          
For Example:

           ptr = (float*) calloc(25, sizeof (float));
This statement allocates contiguous space in memory for 25 elements each with the size of the float.       


realloc() function 

If memory is not sufficient for malloc() or calloc(), you can reallocate the memory by realloc() function. In short, it changes the memory size.

syntax of realloc() function.

          ptr=realloc(ptr, new-size)  
          
          
free() function in C
The memory occupied by malloc() or calloc() functions must be released by calling free() function. Otherwise, it will consume memory until program exit.

Let's see the syntax of free() function.

     free(ptr)  
