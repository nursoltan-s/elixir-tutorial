## Cond

case is useful when you need to match against different values. However, in many circumstances, we want to check different conditions and find the first one that does not evaluate to nil or false. In such cases, one may use cond:

iex> cond do
...>   2 + 2 == 5 ->
...>     "This will not be true"
...>   2 * 2 == 3 ->
...>     "Nor this"
...>   1 + 1 == 2 ->
...>     "But this will"
...> end
"But this will"

## if and unless

Besides case and cond, Elixir also provides the macros if/2 and unless/2 which are useful when you need to check for only one condition:

iex> if true do
...>   "This works!"
...> end
"This works!"
iex> unless true do
...>   "This will never be seen"
...> end
nil

## do/end blocks

At this point, we have learned four control structures: case, cond, if, and unless, and they were all wrapped in do/end blocks. It happens we could also write if as follows:

iex> if true, do: 1 + 2
3


