Resources
Read or watch:

0x08. Recursion, introduction
What on Earth is Recursion?
C - Recursion
C Programming Tutorial 85, Recursion pt.1
C Programming Tutorial 86, Recursion pt.2
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General
What is recursion
How to implement recursion
In what situations you should implement recursion
In what situations you shouldn’t implement recursion
Copyright - Plagiarism
You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
You are not allowed to publish any content of this project.
Any form of plagiarism is strictly forbidden and will result in removal from the program.
Requirements
General
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
You are allowed to use _putchar
You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
Don’t forget to push your header file
You are not allowed to use any kind of loops
You are not allowed to use static variables

Question #0
What does this code print?

void print(int nb)
{
    if (nb < 0) 
    {
        return;
    }
    printf("%d", nb);
    nb --;
    print(nb);
}

int main(void)
{
    print(4);
    return (0);
}

4321


1234


01234


43210

Question #1
What does this code print?

void print(int nb)
{
    printf("%d", nb);
    -- nb;
    if (nb > 0) 
    {
        print(nb);
    }
}

int main(void)
{
    print(4);
    return (0);
}

3210


321


4321


43210

Question #2
What does this code print?

int print(int nb)
{
    if (nb < 0) 
    {
        return (0);
    }
    printf("%d", nb + print(nb - 1));
    nb --;
    return (nb);
}

int main(void)
{
    print(4);
    return (0);
}

64200


01234568


00246

Question #3
What does this code print?

void print(int nb)
{
    printf("%d", nb);
    nb --;
    if (nb > 0) 
    {
        print(nb);
    }
}

int main(void)
{
    print(2);
    return (0);
}

210


21


012


12

Question #4
What does this code print?

void print(int nb)
{
    printf("%d", nb);
    nb ++;
    if (nb < 10) 
    {
        print(nb);
    }
}

int main(void)
{
    print(4);
    return (0);
}

456789


345678910


987654


109876543

Tasks
0. She locked away a secret, deep inside herself, something she once knew to be true... but chose to forget
mandatory
Write a function that prints a string, followed by a new line.

Prototype: void _puts_recursion(char *s);
FYI: The standard library provides a similar function: puts. Run man puts to learn more.

julien@ubuntu:~/0x08. Recursion$ cat 0-main.c
#include "main.h"

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    _puts_recursion("Puts with recursion");
    return (0);
}
julien@ubuntu:~/0x08. Recursion$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 _putchar.c 0-main.c 0-puts_recursion.c -o 0-puts_recursion
julien@ubuntu:~/0x08. Recursion$ ./0-puts_recursion 
Puts with recursion
julien@ubuntu:~/0x08. Recursion$ 

1. Why is it so important to dream? Because, in my dreams we are together
mandatory
Write a function that prints a string in reverse.

Prototype: void _print_rev_recursion(char *s);


2. Dreams feel real while we're in them. It's only when we wake up that we realize something was actually strange
mandatory
Write a function that returns the length of a string.

Prototype: int _strlen_recursion(char *s);
FYI: The standard library provides a similar function: strlen. Run man strlen to learn more.

3. You mustn't be afraid to dream a little bigger, darling
mandatory
Write a function that returns the factorial of a given number.

Prototype: int factorial(int n);
If n is lower than 0, the function should return -1 to indicate an error
Factorial of 0 is 1

4. Once an idea has taken hold of the brain it's almost impossible to eradicate
mandatory
Write a function that returns the value of x raised to the power of y.

Prototype: int _pow_recursion(int x, int y);
If y is lower than 0, the function should return -1
FYI: The standard library provides a different function: pow. Run man pow to learn more.


5. Your subconscious is looking for the dreamer
mandatory
Write a function that returns the natural square root of a number.

Prototype: int _sqrt_recursion(int n);
If n does not have a natural square root, the function should return -1
FYI: The standard library provides a different function: sqrt. Run man sqrt to learn more.

6. Inception. Is it possible?
mandatory
Write a function that returns 1 if the input integer is a prime number, otherwise return 0.

Prototype: int is_prime_number(int n);



