## Description

This Repository has has all the code necessary for our (Alemseged Fekede and
Biniyam Wolde's) custom function called ``_printf()``.  It attempts to replicate
 the exact same process as the C function ``printf()``. This project is completed
 for the ALX software engineering program.

###functions used

* ``write``, ``malloc``, ``free``, ``va_start``, ``va_end``, ``va_copy``,
``va_arg``

## Brief Synopsis

``_printf()`` function takes 2 arguments: a character pointer to a string:
``format``, and a 'variable arguments list': ``arg_list``.  ``_printf()`` loops
through the format string searching for a conversion specifier, which is
indicated with the '%' symbol.  If found, the ``match_specifier()`` function
loops through an array of structs (contianing character and function pairs) to
find the specifier function that is matched with the given conversion specifier
from the format string, and then returns a pointer to that paired function.
``_printf()`` uses the pointer to that specifier function to call the specifier
function on the next queued argument from the ``arg_list``.  Each specifier
function writes a character one at a time as determined from the value in
``arg_list``. In the buffer branch and in the 'release: v0.1', our code writes
the characters from the format string and the associated specifiers to the
buffer, and in the 'no-buffer' branch, our code is instead written to standard
output one at a time.

## Usage

The directory contents should be compiled with the following command:

```
$ gcc -Wall -Werror -Wextra -pedantic *.c
```

`_printf()` function may be used, in any C language program.  This is the
prototype:

```
_printf(const char *[FORMAT], ...)
```

__FORMAT__ refers to a string with any number of specifiers followed by a '`%`'
symbol. i.e Alx software engineering cohort: %d Squad`.  __...__ refers to a
list of variadic (variable arguments in C Language), which can be any number of
variables of any type.  With the above example string, appropriate arguments
could be 7, 522  These examples together should be called
like so:

```
_printf("Alx software engineering cohort: %d Squad: %d",7, 522);
```

## Tests

To run tests, to check the overall functionality of the program, compile
with `main.c` as the main file:

```
$ cp test/main.c .
$ gcc *.c
```

## Authors
Alemseged Fekede github.com/ALemsegedF
Biniyam Wolde

## License

MIT Licence
