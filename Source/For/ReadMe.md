# For Loop

### Introduction
Control Flow is a crucial aspect of any programming language. Swift offers a variety of loops and fundamental switches to manage code execution. However, `for` loop stands out as a truly unique construct, providing numerous alternative writing styles.

## Measurement
**Measure the Control Flow - For Loop**\
_attempts: 10, repeats: 100 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | for in by element |  90.22 ms | +  0% | .......... |
| 2. | forEach           |  94.69 ms | +  5% | .......... |
| 3. | for in by index   | 184.13 ms | +104% | .................... |

## Conclusions
An example of the current measurement is the same iteration on the same data sets. This time, the worst result can be the most basic loop based on index. However, it’s important to note that the code calling twice as slowly is not due to the implementation of the loop itself, but an additional step: accessing the element in the collection through the index.
