maxlt
=====

Usage
-----

    maxlt(x , table)

| Argument | Description      |
| -------: | :--------------- |
|        x | a numeric vector |
|    table | a numeric vector |

Value
-----

A numeric vector of length `length(x)`.
Each element of the return is the maximum value among those of
`table` which are less than the corresponding
element of `x`.
If there are no values in `table` which are less than
an element of `x`,
the corresponding elment of the return is `NA_real_`.
