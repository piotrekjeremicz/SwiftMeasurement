# Compact Map

### Introduction
Transforming data models is actually a key activity of any program. Swift provides us with Higher Order Functions that perform specific transformations on the collection.

Compact map enables you to leverage the properties of optional types in Swift. By transforming collections based on this behavior, you can work with data that might or might not be assigned to a variable.

The `compactMap(_:)` function takes a closure defining an element’s transformation within a collection. Swift language offers flexibility in writing closures in full or shortened form. Additionally, KeyPath can be utilized to specify the relevant parameter. For comparison, we’ll also present a straightforward implementation using a `for` loop. 

## Measurement
**Measure the Higher Order Functions - Compact Maps**\
_attempts: 10, repeats: 100 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Control Flow method |  93.69 ms | +  0% | .......... |
| 2. | Closure parameter   | 103.58 ms | + 11% | ........... |
| 3. | Shorthand argument  | 103.62 ms | + 11% | ........... |
| 4. | Key Path            | 129.87 ms | + 39% | ............. |

## Conclusions
Control Flow implementation is the most efficient approach in our measurement. This means that closure support introduces an additional access layer that impacts performance. While it may not be a significant increase, it’s worth noting.

In this scenario, the approach employing KeyPath is burdened by a significant performance penalty of 40%. When compared with `map(_:)` and `flatMap(_:)`, KeyPath stands out as the method with the highest overhead. Therefore, in this particular case, it would always be prudent to evaluate whether we could eliminate the need to explicitly point out the property through the path by instead utilizing the closure.
