# Map

### Introduction
Transforming data models is actually a key activity of any program. Swift provides us with Higher Order Functions that perform specific transformations on the collection.

The `map(_:)` function takes a closure defining an element’s transformation within a collection. Swift language offers flexibility in writing closures in full or shortened form. Additionally, KeyPath can be utilized to specify the relevant parameter. For comparison, we’ll also present a straightforward implementation using a `for` loop. 

## Measurement
**Measure the Higher Order Functions - Maps**\
_attempts: 10, repeats: 100 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Closure parameter   |  65.63 ms | +  0% | .......... |
| 2. | Shorthand argument  |  66.01 ms | +  1% | .......... |
| 3. | Key Path            |  83.09 ms | + 27% | ............ |
| 4. | Control Flow method |  94.46 ms | + 44% | .............. |

## Conclusions
Swift’s optimization is evident in the almost 50% worse result obtained by a simple implementation of the mapping function. Repeatedly calling the `append(_:)` method in `for` loop significantly slows down the code’s execution.

Surprisingly, there’s a notable difference in the performance of the `map(_:)` function when we point a parameter through KeyPath. It’s revealed that the additional access layer required during the path resolving adds almost 30% to the code execution time.

The advantage of using KeyPath is to enhance code readability. If you’re willing to accept a slight performance hit for elegant code, it’s worth it. However, if you’re working with large datasets, use closures instead.
