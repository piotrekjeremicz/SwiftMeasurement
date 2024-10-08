# Compare Map algorithms

### Introduction
Swift provides three distinct mapping methods with similar functionalities. Each of the Higher Order Functions can be used for specific purposes, and some of them cover the functionality of others. However, are there notable performance differences between them?

## Measurement
**Measure the Higher Order Functions - Maps Comparison**\
_attempts: 10, repeats: 100 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | map        |  59.88 ms | +  0% | .......... |
| 2. | compactMap |  85.19 ms | + 42% | .............. |
| 3. | flatMap    | 125.00 ms | +109% | .................... |

## Conclusions
The measurements were taken for the same data set. Although the value results for each of the three measurements will be different, our objective is to determine the variation in performance for each of these functions.

The `map(_:)` function, the simplest implementation, occupies the first spot. The second, 40% slower, method is `compactMap(_:)`, where an additional step is taken to check if the supported variable doesn’t contain `nil`.

The `flatMap(_:)` function, which is known for its complexity, proved to be the slowest function in the test. It took twice as long to execute as the `map(_:)` function.

In conclusion, let’s select the mapping function that best suits your requirements.
