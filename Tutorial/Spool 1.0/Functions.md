Functions are the main way of manipulating data within Spool.
The syntax for a function is quite similar to that of a variable.
```
Return Type Name(TypeofArgument NameofArgument) = {
    WhatevertheFunctionDoes;
};
```
All functions are pure in Spool, they all take in an input and return an output.
Here is an example of function uses.
```
type int = -32768...32767{};
int square(int x) = {
    x*x >|;
};
int OperationMinusSeven(int x, int func operation) = {
    x |> operation() |>  - 7 >|;
};
int number = OperationMinusSeven(4, square);
```
The first function square introduces us to the >| operator this tells us to return whatever is on the other side.
What is on the other side is in this case is the square of x.
After that we see the "func" keyword.
The func keyword is how we pass in functions to other functions.
Inside the body of the function we see |> or pipe operator.
The pipe operator takes whatever is on the left and passes it to the right, so to read this expression we break it up.
x is passed right to the function operation,
then the value of that is passed to - 7,
which is then returned using the >| operator.
In total operation(x) - 7, just like the function's name.
