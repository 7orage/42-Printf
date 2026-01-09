[README.md](https://github.com/user-attachments/files/24477596/README.md)
# Printf
***
• _This project has been created as part of the 42 curriculum by <lheteau>. We are the 29th november 2025._

***
### Table of contents
***
1. _Description_
2. _Instructions_
3. _Resources_
4. _Data structure_

***
## **Description**
***
• Ft_printf is a function written to format and print data to the standard output (stdout). It reproduces the behavior of the standard C `printf` function without implementing the original buffer management, allowing formatted output of strings, integers, characters, hexadecimal numbers, and pointers.  

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

## **Data structure**
***
• The main function, ft_printf, reads the format string character by character. When a character is not %, it is printed directly. When % is found, the next character is treated as a conversion specifier.

The function ft_printf initializes the variable argument list, loops through the format string, and calls ft_find_conv to handle each conversion. It also keeps track of the total number of printed characters and returns this value at the end.

The function ft_find_conv selects the correct printing function depending on the specifier (c, s, d, u, x, p, etc.). Each type of data has its own function, which is responsible only for printing the value and returning how many characters were written.

Numbers are printed using recursive functions, which allows digits to be displayed in the correct order without using extra memory. Special cases such as NULL strings, pointers, and the %% format are handled to match the behavior of the original printf.
***
• The ```__attribute__((format(printf, 1, 2)))``` ensures compile-time checking of the format string and arguments, helping detect errors like the original printf.
