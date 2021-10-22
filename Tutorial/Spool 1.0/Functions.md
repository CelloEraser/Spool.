Functions are the main way of manipulating data within Spool.
The syntax for a function is quite similar to that of a variable.
Return Type Name(TypeofArgument NameofArgument) = {
    WhatevertheFunctionDoes;
}; 
All functions are pure in Spool, they all take in an input and return an output.
Here is an example of function uses.
```
type int = -32768...32767{};
int square(int x) = {
    return x*x;
};
int OperationMinusSeven(int x, int func operation) = {
    x |> operation() |>  - 7 |> return;
};
int number = OperationMinusSeven(4, square);
```