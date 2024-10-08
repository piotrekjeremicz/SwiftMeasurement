# Struct and Classes

### Introduction
It appears evident why we employ structures and classes. The former is ideal for representing values, while the latter is represented by a reference that can be shared across the code. However, what distinguishes them?

## Measurement
**Measure the Initialization**\
_attempts: 10, repeats: 100 000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Struct.init() | 268.06 ms | +  0% | .......... |
| 2. | Class.init()  | 278.26 ms | +  4% | .......... |

**Measure the Access**\
_attempts: 10, repeats: 100000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Struct.title |  20.76 ms | +  0% | .......... |
| 2. | Class.title  |  20.88 ms | +  1% | .......... |


**Measure the Copy**\
_attempts: 10, repeats: 100000_
|  | Name | Duration | Deviation | Scale |
| --- | --- | --- | --- | --- |
| 1. | Struct copy |  20.72 ms | +  0% | .......... |
| 2. | Class copy  |  28.13 ms | + 36% | ............. |

## Conclusions
Only the copying action provides the structure with a visible advantage. Time efficiency doesn’t favor any of the types here. However, it’s important to remember that a structure as a value type behaves differently from a class that’s a reference type. Even the memory they occupy can reveal other differences between these two language elements.
