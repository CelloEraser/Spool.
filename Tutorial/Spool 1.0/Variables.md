Now that you know how to make types it is time for variables.

Variables don't really exist in Spool, but it is the best name for what they are.

Every variable in Spool is immutable, it cannot change.
```
int x = 3;
x = 5;
```
This code will not work no matter what.

You might think that this is boring since they can't change.

They are still useful however.

Inside of types and subtypes you can declare variables using the syntax (Type) (Name).

For subtypes they must either have the same variables or a subset of variables.

Types and subtypes can exist without ranges but they must have variables inside of them.

When declaring a type or subtype with variables the syntax looks like this.
```
Type Name = Value { Name = Value; };
```
You can access the variable inside a variable using the "." operator.

If the type of a variable is a subtype you only have access to variables in that subtype.
