## Revision of Basics

#### Just some known things,
A computer program is a sequence of instructions that tell the computer what to do. A _statement_ is a type of instruction that causes the program to perform some action.

There are many different kinds of statements in C++:

    Declaration statements
    Jump statements
    Expression statements
    Compound statements
    Selection statements (conditionals)
    Iteration statements (loops)
    Try blocks

A *function* is a collection of such statements that are executed sequentially for a specific task to perform within the program.

`#include<iostream>` is a special type of line called a preprocessor directive. This preprocessor directive indicates that we would like to use the contents of the iostream library, which is the part of the C++ standard library that allows us to read and write text from/to the console.
`int main()` is a special function that every C++ program must have and every execution starts from this function at first.
`{`
`std::cout << "fuck the world\n";` => `std::cout`(which stands for “character output”) and the << operator allow us to display information on the console
`}`

```
| n | Code                               |
| - + ---------------------------------- | 
| 1 | #include<iostream>                 |
| 2 |                                    |
| 3 | int main() {                       |
| 4 |  std::cout << "fuck the world\n";  |
| 5 | }                                  |
| - + ---------------------------------- | 
```
> [!CAUTION]  addtional information is to be added.

## Comments
The // symbol begins a C++ single-line comment, which tells the compiler to ignore everything from the // symbol to the end of the line. For example:
`// this is a hidden comment just like my thoughts which nobody cares about`

### Multi-line comments

The /* and */ pair of symbols denotes a C-style multi-line comment. Everything in between the symbols is ignored.
```
/* This is a multi-line comment.
   This line will be ignored.
   So will this one. */
```
Since everything between the symbols is ignored, you will sometimes see programmers “beautify” their multi-line comments:
```
/* This is a multi-line comment.
 * the matching asterisks to the left
 * can make this easier to read
 */
```
Multi-line style comments can not be nested. Consequently, the following will have unexpected results:
```
/* This is a multi-line /* comment */ this is not inside the comment */
// The above comment ends at the first */, not the second */
```
When the compiler tries to compile this, it will ignore everything from the first /* to the first */. Since this is not inside the comment */ is not considered part of the comment, the compiler will try to compile it. That will inevitably result in a compile error.

> [!WARNING]
> Don’t use multi-line comments inside other multi-line comments. Wrapping single-line comments inside a multi-line comment is okay.

### Objects and Variables
An object is used to store a value in memory. A variable is an object that has a name (identifier).
In general programming, the term object typically refers to an unnamed object in memory, a variable, or a function. In C++, the term object has a narrower definition that excludes functions.
