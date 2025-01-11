# Julia Function Bug: Unexpected Results with Negative Inputs

This repository demonstrates a subtle bug in a Julia function that arises from unexpected operator precedence. The function aims to square the input, returning a positive result regardless of the input's sign. However, due to how the negative case is handled, it produces unexpected results.

## Bug Description

The `myfunction` in `bug.jl` incorrectly handles negative inputs. The expression `-x^2` is evaluated as `-(x^2)`, resulting in the negative of the square, instead of the intended `(-x)^2` (square of the negative number).

## Solution

The corrected version in `bugSolution.jl` uses parentheses to ensure the correct order of operations for negative inputs.