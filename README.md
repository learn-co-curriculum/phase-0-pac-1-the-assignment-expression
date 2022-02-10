# The Assignment Expression

## Learning Goals

- Define the _Assignment Expression_
- Define Mutability / Immutability
- Learn what the Return Value of an _Assignment Expression_ is

## Introduction

So you've seen the first of our **essential three expressions**, the _constant
expression_, which gives JavaScript some constant facts about the world: `2` is
`2`, `3` is `3`, etc...

It's really useful to associate an _expression's evaluated result_ with a
'name'. We call those names that we associate with the _expression's_ result,
_variable names_ or, commonly, just _variables_. The process of bonding an
expression to a variable is called _assigning a variable_. Programmers also say
that "the variable name 'points to' the expression that was assigned to it."

A helpful metaphor here is that it's like adding a new entry to a dictionary:
`aFunNumber`'s definition is `3 * (10 - 4)` or `myBirthYear`'s is `1989`. Or you
can think about a variable name as a label you put on a box. Using this
metaphor, the box labeled `aFunNumber` contains the value `3 * (10 - 4)`, and
the box labeled `myBirthYear` contains the value `1989`.

We create the association between a variable name and a value by using the
second of our **essential three expressions**: the _assignment expression_.

## Define the _Assignment Expression_

In JavaScript, the assignment expression is like so:

![Assignment Expression Graphic](https://curriculum-content.s3.amazonaws.com/phase-0/the-assignment-expression/assigning-a-variable.jpg)

Here are some examples:

```js
aFunNumber = 3 * (10 - 4);
myBirthYear = 1989;
```

Variable names are most often descriptions of what their assigned expressions
_mean_. In JavaScript, when a variable name is made of multiple words, every
word after the first is capitalized. This is referred to as _camelCase_ and
although it isn't strictly required, it is a common convention in JavaScript.

> **Note**: In JavaScript, it's _optional_ to include a semi-colon at the end of
> each line. You may encounter JavaScript expressions written both ways.

While you _can include_ numbers and some symbols in variable names, let's keep
things simple for the moment and just use camelCased letters.

Consider the following expression:

```js
maximumSpeed;
```

Run this alone in a REPL, and we get an error:

```text
ReferenceError: maximumSpeed is not defined
```

Here, JavaScript, by default, doesn't know anything about `maximumSpeed`.

When we define a variable using the "assignment expression" we add something new
to JavaScript.

```js
maximumSpeed = 9000
```

Let's try this out in the REPL:

<iframe height="400px" width="100%" src="https://replit.com/@lizbur10/Sandbox?lite=1&outputonly=1" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

Notice that by using the assignment expression, `maximumSpeed = 9000`, our code
evaluates to `9000` when run. Once `maximumSpeed` is defined, JavaScript will
know what it is. Now try putting just `maximumSpeed` in and hitting enter and
you'll see that JavaScript remembered its value! (We'll look at this more
closely in the next lesson.)

> **_SUPER-IMPORTANT_**: In the assignment expression `=` means "assignment". It
> does not mean "what's on the left of the `=` is equal to what's on the right."
> In math courses, we use `=` to say that the expressions on either side of the
> `=` are the same. JavaScript uses `==` and `===` for that purpose. It's very
> common — and very confusing — for beginners to have bugs where they confuse
> `=` for `==` or `===`.

## Define Mutability / Immutability

A variable is said to be "mutable." That means the value that the name "points
to" can be changed during the running of the program. Being able to change the
value a variable points to is very important. For example, if we need to do
something 10 times, we need a variable to keep track of how many times the thing
happens. That variable will need to change: its value will need to increase by 1
each time. Here's _mutability_ in action:

Many years ago my height in centimeters was 50cm; go ahead and add the following
line into the REPL's console:

```js
heightInCentimeters = 50;
```

<iframe height="400px" width="100%" src="https://replit.com/@lizbur10/Sandbox?lite=1&outputonly=1" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

But today my height is 180cm. Let's now put the following code into the console:

```js
heightInCentimeters = 180;
```

Now that we have assigned `heightInCentimeters` to two different values, what do
you think the console will return if we just type `heightInCentimeters` and hit
enter? Let's try it out!

If you guessed we would see a return value of `180`, you were right! The last
value assigned to the variable is what is saved.

Sometimes, we might want to make a variable's value permanent. We might want to
say "hey, this value should not change." We want to say that the value is
_immutable_, the opposite of _mutable_. We do this by writing a **constant**
(not the same as the constant expression we discussed previously). We'll go into
more detail on constants in the next part of this course.

## Return Value of an _Assignment Expression_

The return value of an _assignment expression_ is the evaluated result of the
expression to the right of the `=`.

```js
recurringExpressionValue = 3 * (10 - 4);
// => 18
```

Pay attention here: the return value of the assignment expression **_IS NOT THE
SAME THING_** as getting the value out of the variable name. We'll learn to get
the value "back out of a variable" in the next lesson. What JavaScript is saying
is that the assignment expression's return value is the value of the expression
to the right of the `=`.

> **Note**: The line underneath `recurringExpressionValue` indicates what this
> expression evaluates to; in this case, it's the number `18`. Any line that
> starts with `//` in JavaScript is a "comment": it's code that is ignored by
> the JavaScript engine, but can be used to indicate something to other
> developers looking at your code.

## Conclusion

Think about a baby who has never spoken before. Before it stands a parent saying
their name over and over (...and over) again.

![Learning to talk 1](https://curriculum-content.s3.amazonaws.com/phase-0/the-assignment-expression/Image_55_Mama-Baby_1.png)

They wave towards their bodies and say their names again and again. What the
parent is trying to do is teach the baby to assign their face to the variable
name "Mama" or "Dada." But to the baby, this means nothing.

While neither the baby or the (average) adult is aware of it, they're trying to
teach the baby the second of the _three essential expressions_: the assignment
expression. Then, one magical day, it clicks for the baby. It performs an
assignment in its precious little head:

![Learning to talk 2](https://curriculum-content.s3.amazonaws.com/phase-0/the-assignment-expression/Image_55_Mama-Baby_2.png)

Unfortunately, Mom is still sad; she doesn't have any _proof_ that the
assignment was successful. For that to work, the baby will need to prove that it
can "look up" the variable assignment of who "ma-ma" points to. The baby will
need to learn the last of our _essential expressions_: the variable lookup
expression!
