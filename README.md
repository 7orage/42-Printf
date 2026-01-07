[README.md](https://github.com/user-attachments/files/24477596/README.md)
# Printf
***
• _This project has been created as part of the 42 curriculum by lheteau. We are the 29th november 2025._

***
### Table of contents
***
1. _Description_
2. _Instructions_
3. _Resources_

***
## **Description**
***
• printf is a function written to format and print data to the standard output (stdout). It reproduces the behavior of the standard C `printf` function, allowing formatted output of strings, integers, characters, hexadecimal numbers, and pointers.  

The function supports the following format specifiers:  
- `%c` for characters  
- `%s` for strings  
- `%p` for pointers  
- `%d` / `%i` for signed integers  
- `%u` for unsigned integers  
- `%x` / `%X` for hexadecimal numbers  
- `%%` for the '%' character
***
• The goal of this project is to understand variadic functions (`...`), format parsing, and low-level output using the `write` system call, as well as to manage memory and handle edge cases correctly.  

## **Instructions**
***
• A Makefile is provided for easy compilation. Simply run: ```make``` .
***
• To use ft_printf in your own project, include the header: ```"libftprintf.h"``` .
***
• Example main :
```
#include "libftprintf.h"

int main(void)
{
    int n = 42;
    char c = 'A';
    char *str = "Hello, 42!";
    void *ptr = &n;

    ft_printf("Char: %c\n", c);
    ft_printf("String: %s\n", str);
    ft_printf("Pointer: %p\n", ptr);
    ft_printf("Integer: %d\n", n);
    ft_printf("Unsigned: %u\n", 3000);
    ft_printf("Hex lowercase: %x\n", 255);
    ft_printf("Hex uppercase: %X\n", 255);
	ft_printf("Simple %%: \n");


    return 0;
}
```

## **Ressources**
***
• I used several articles and online resources to support my coding journey. Notably, the video “1#  c - Variadic functions” by the youTuber codivily was very helpful. I also consulted the websites unstop.com and koor.com, which provided explanations about the formats specifiers and the usage of variadic functions in C.
***
• Artificial Intelligence tools were helpful in the writing and structuring of this README.

