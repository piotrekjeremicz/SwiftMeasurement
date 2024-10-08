# Flat Map

### Introduction
Transforming data models is actually a key activity of any program. Swift provides us with Higher Order Functions that perform specific transformations on the collection.

The `flatMap(_:)` function takes a closure defining an element’s transformation within a collection. Swift language offers flexibility in writing closures in full or shortened form. Additionally, KeyPath can be utilized to specify the relevant parameter. For comparison, we’ll also present a straightforward implementation using a `for` loop. 

## Measurement
**Measure the Higher Order Functions - Flat Map**\
_attempts: 10, repeats: 100 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Control Flow method | 160.23 ms | +  0% | .......... |
| 2. | Closure parameter   | 160.76 ms | +  0% | .......... |
| 3. | Shorthand argument  | 160.90 ms | +  0% | .......... |
| 4. | Key Path            | 181.61 ms | + 13% | ........... |

## Conclusions
Our base implementation of the flat mapping function using a for loop is the most efficient way to transform a set into another collection. Although the differences are minor, this implies that the `flatMap(_:)` function itself is more intricate.

Calling the algorithm with a path results in a 20% performance decrease compared to other methods. While this drop in performance may be negligible with a small dataset, it’s worth noting.
