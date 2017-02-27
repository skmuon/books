#Functional Programming

Notes from _Why Functional Programming Matters_ by _John Hughes_

_The following are no so benefitial statements of FP_

In Functional Programming fundamental operation is the application of
functions to arguments. A main program is itself written as function that
receives the program's input as its argument and delivers the program's output
as its result.

Special characterstics and advantages of functional programs are as follows

1. FP contains no assignment statements, so variables once given a value never
   change
2. FP contains no side effects at all, a function call can have no other
   effect than its own computation

This eliminates major source of bugs and also removes dependency on order of
execution. Since no side effects can change expression's value, it can be
executed any time. One can freely replace values of variables with expression
and vice versa. This removes burden of prescribing a flow control. This
feature makes programs _**referentially transparent**_. This freedom helps
make functional programs more tractable mathematically than their conventional
counterparts.

In short FP contains _no side effects_, _no assignments_ and _no flow
control_.

Functional programmer are order of magnitude in  productivity than
conventional programmer, reason FP are oder of magnitude shorter.

## An analogy with structured programming

Virtues of SP (structured program) (Don't explain the +ves)

1. Contains no _goto_ statements
2. Blocks in SP do not have multiple entries or exits
3. SP are more tractable than unstructured counterparts

The most important difference between structured and unstructured programs are
that structured programs are designed in a modular way. Modular designs brings
great producticity improvements.

1. Small modules can be coded quickly and easily
2. General purpose modules can be reused leading to faster development
   subsequent programs
3. Modules of programs can be tested independently, helping to reduce the time
   in debugging

The absence of _goto_ and other virtues have very little to this increase in
productivity.

Modular design, break the bigger problem into smaller ones, the glue them
back. The way in which the original problem is broken down depends how it can
be glued back together. To increas modularity language should provide a new
kind of glue. Complicated scope rules and provisions for separate compilation
help only with clerical details. They can never make a great contribution to
modularization

## Gluing Functions Together

Recursion is the fundamental idea. Expalined in terms of list.

```

list of * :: Nil | Cons * (listof *)
```

Which means list of element * is either empty or * + list of *

```
	[]	means Nil
	[1]	means Cons 1 Nil
	[1,2,3] means Cons 1 (Cons 2 (Cons 3 Nil)

```
The elements of a list can be added by a recursive function _sum_. The
function _sum_ must be defined for two kinds of argument: an empty list (Nil)
and a Cons. Since the sum of no numbers is zero, definition is

```
sum Nil = 0
```

and since the sum of Cons can be calcualted by adding the first element of the
list to the sum of the others, we can define

```
sum (Cons n list) = num + sum list
```

Examining this definition, we see that only the boxed (not shown here, but
hightlighted in bold) are
specific to computing a sum.
```
sum Nil = 0
sum (Cons n list) = n + sum list
```

This means that the computation of a sum can be modularized by gluing together
a general recursive pattern and the boxed parts. This recursive pattern is
conventionally called _foldr_ and so _sum_ can be expressed as

```
sum = foldr (+) 0
```

The definition of _foldr_ can be derived just by parameterizing the definition
of sum, given

```
(foldr f x) Nil = x
(foldr f x)(Cons a l) = f a ((foldr f x)l)
```


# Gluing programs together
If _g_ and _f_ are functions then _(g.f)_  is a program that, when applied to
its input, computes

```
g(f input)
```

The program _f_ computes its output, which  is used as input to _g_. The two
programs are run together in strict synchronization. Program _f_ is only
started when _g_ needs input and stopped when _g_ is done.  (The function _f_
can run till infinity, but doesn't affect)

This allows termination conditions to be separated from loop bodies. A
powerful modularization. 

Since this method of evaluation runs _f_ as little as possible, this is called
__lazy evaluation__ .
