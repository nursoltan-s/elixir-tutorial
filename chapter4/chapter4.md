## The match operator

We have used the = operator a couple times to assign variables in Elixir:

iex> 1 = x
1
iex> 2 = x
** (MatchError) no match of right hand side value: 1

## Pattern matching

The match operator is not only used to match against simple values, but it is also useful for destructuring more complex data types. For example, we can pattern match on tuples:

iex> {a, b, c} = {:hello, "world", 42}
{:hello, "world", 42}
iex> a
:hello
iex> b
"world"

## The pin operator

Use the pin operator ^ when you want to pattern match against an existing variable’s value rather than rebinding the variable:

ex> x = 1
1
iex> ^x = 2
** (MatchError) no match of right hand side value: 2
iex> {y, ^x} = {2, 1}
{2, 1}
iex> y
2
iex> {y, ^x} = {2, 2}
** (MatchError) no match of right hand side value: {2, 2}
