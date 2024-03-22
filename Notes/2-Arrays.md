# Week2: Arrays
## Compiling
- the language c use the compiler `clang`
- in C, when you want to use compiler to compile code use `clang -o program_name program_script_name.c -lThird_party_library_name` <br>
`clang -o hello hello.c -lcs50`
- Then use `./program_name` to run

### Turning source code to machine code 
1. Preprocessing: At the top of the file, with `#` is the preprocess file, it preprocess to copy the functions will use below from other file to here. <br> E.g. `#include <stdio.h>`
2. Compiling: compile all the script you wrote to assembly language
3. Assembling: convert assembly code to 0 and 1's
4. linking: link your file to the files you use `hello.c``stdio.c``cs50.c` linked together

## Debugging
- step over: go to next line
- step into: inspect the inside of the line highlighted.

## AI
rubber duck debugging

## types
- bool: 1 byte
- int: 4 bytes
- long: 8 bytes
- float: 4 bytes
- double: 8 bytes
- char: 1 byte
- string: ? bytes

## Arrays
- `int scores[3];` give me array of size 3, tell the computer scores has 3 integers
- `scores[0] = 72;` assign first scores to 72
- Arrays only allowed one type of variables(int, str etc.)

## String 
- String is an array of characters
- At the end of the string use one more byte store all 0s to represents its ended.`\0` known as `NUL`
- String can also stored as arrays
- Count string length in C:
```C
int string_length(string s)
{
    int n = 0;
    while (s[n] != '\0')
    {
        n++;
    }
    return n;
}
```
A library called `<string.h>` has function called `strlen` can be used as well

- Uppercase the String : 32 is the gap between lowecase and uppercase in ASCII
```C
for (int i = 0, n = strlen(s); i < n; i++)
    {
        // If lowercase
        if (s[i] >= 'a' && s[i] <= 'z')
        {
            printf("%c", s[i] - 32);
        }
        else
        {
            printf("%c", s[i]);
        }
    }
```
A library called `<ctype.h>` has function called `toupper()` can be used as well.

## Command-line Arguments
```C
int main(int argc, string argv[])
{
    printf("hello, %s\n", argv[1]);
}
```

In command line just write `./greet Felix`