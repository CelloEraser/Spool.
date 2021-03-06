In Spool there are no built in primitives you must declare your own types.
```
int x = 3;
```
This code does not compile.
However this code does.
```
type int = -8...7 {};
int x = 3;
```
Now a lot of things happened in line 5 which I will explain.

The "type" keyword is used for standalone types.

The "int" is the name of the declared type.

The "=" is the assignment of the type.

The "-8...7" is an example of the range operator "..." it specifies that int can only hold between -8 and 7 numbers.

The "{}" will be used later but can for now be empty.

The ";" is the line-ender in Spool you must end almost every statment with it.

The last example used the "..." operator for the range of int but you can manually declare the range.
```
type Day = ("Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday") {};
Day Wed = "Wednesday";
```
Now we get to the fun parts subtypes.

You can declare a subtype using the "sub" keyword inside he curly brackets of another type.

Subtypes must be with in the range of the type they are in, here is an example.
```
type Day = ("Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday") {
    sub WeekDay = Day[1...5]{};
};
```
In this example we used the "..." operator with in Day.

You see types also act as arrays of there range.

You can again declare ranges with in subtypes manually.
```
type Day = ("Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday") {
    sub WeekDay = ("Monday", "Tuesday", "Wednesday", "Thursday", "Friday"){};
};
```
To access a subtype you must first access the type then use the "extract" keyword take this example.
```
Day extract WeekDay tues = "Tuesday";
```
In this example tues is of type Day and of subtype WeekDay.

A type can have multiple subtypes and subtypes can have subtypes with in them as long as they are within range.
```
type Day = ("Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday") {
    sub WeekDay = ("Monday", "Tuesday", "Wednesday", "Thursday", "Friday"){
        sub WorstDay = ("Monday");
        sub BestWeekDay = ("Friday");
    };
    sub WeekEnds = ("Sunday", "Saturday"){};
};
```
