rangeNeat
=========

_Create one interval that contains another._

Usage
-----

    rangeNeat(x, minsNeat, widthsNeat)
    
|   Argument | Description      |
| ---------: | :--------------- |
|          x | a numeric vector |
|   minsNeat | a numeric vector |
| widthsNeat | a numeric vector |

Value
-----

Returns a numeric vector of length two representing an interval.
The minimum of the return, _MIN_, will be the greatest element of `minsNeat` that is less than or equal to the minimum of `x`.
The maximum of the return, _MAX_, will be the least value that is greater than or equal to the maximum of `x`,
given that _MAX_ - _MIN_ is one of `widthsNeat`.

Details
-------

The original intent is to compute ranges for graphs so that
the plot positions fall within the plot area and
the plot area is sized and positioned aesthetically (i.e.,
according to some notion of an aesthetic minimum for the plot area and
an aesthetic plot width or height).

Warnings
--------

Expect strange results if `min(x) < min(minsNeat)` or `diff(range(widthsNeat)) < diff(range(x))`.

Examples
--------

    rangeNeat(c(-pi, pi), -10:0 , 1:20)
    # [1] -4  4
