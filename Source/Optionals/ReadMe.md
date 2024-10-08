# Unwrapping Optionals

### Introduction
Optionals are one of the most crucial type patterns in Swift. They enable us to determine whether a specific variable is assigned to a property or not. Swift has introduced several methods that facilitate unwrapping the value. However, the question arises: what is the most efficient way to determine if we will encounter `nil` or not?

## Measurement
**Measure the Unwrapping Optionals**\
_attempts: 100, repeats: 400 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Implicitly Unwrapped Optionals |  83.90 ms | +  0% | .......... |
| 2. | Nil-Coalescing Operator        |  84.41 ms | +  1% | .......... |
| 3. | Pattern Matching               |  84.56 ms | +  1% | .......... |
| 4. | Optional Binding - guard let   |  84.76 ms | +  1% | .......... |
| 5. | Optional Binding - if let      |  85.06 ms | +  1% | .......... |
| 6. | Forced Unwrapping              |  85.66 ms | +  2% | .......... |
| 7. | Optional Chaining              | 118.74 ms | + 42% | .............. |

## Conclusions
Unpacking optional values is a fundamental aspect of Swift, and it’s not surprising that many of its features are merely syntactic sugar. However, Optional Chaining set it apart from the rest. Why do we get this result?

To test Optional Chaining, we employed the code `let _ = some?.description`, which carries an extra step. By invoking the `description` variable, we trigger its access function, thereby incurring a slight increase in code execution time.
