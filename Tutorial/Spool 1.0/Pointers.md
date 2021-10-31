Pointers are well kind of messy.

You can declare a pointer using special types which are the names of the type preceded with an '&'.

Pointers contain the address of a value.

To get the address to a value you use '&'.
```
int x = 3;
&int ptrx = &x;
```
I actually lied about there being no variables in Spool, you can kind of make them but you have to use **pointer arithmetic**(Cue creepy bird sound, thunder and lightning).

Do you hear that, the souls of angry C/C++ programmers who had so much trouble with **pointer arithmetic**(Cue creepy bird sound, thunder and lightning) they became ghosts.

They now wander the mortal realm trying to stop people from sucumbing to their fate.

In all seriousness though pointer arithmetic is really useful.

Pointer arithmetic can be acheived using the + and - operators, moving the address up and down respectively.

For example here is an implementation to find a value around an address.
```
&int Implementation(int value, &int address) = {
    if(*address != value) { Implementation(value, address+1); } else { address } >|
};
```
You can also have addresses to functions.

These give you where the functions is stored in memory.
```
int square(int x) = {
    x*x >|;
};
&int asquare = &square();
int y = *(asquare + 5)(6);
```
This code gives the operation at the address of the square operation + 5 passing in 6.

The asterisk operator in this context turns an adress into its value.

Creating a pointer to a type or subtype with variables allows you to access those variables with the '->'.

If you would like the address of a variable in a type or subtype add an '&' to the front when accessing a value.

Be careful with pointers and only use them when you absolutely know what you are doing.
