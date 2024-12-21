# Unexpected Empty Array Return in MATLAB Function

This repository demonstrates a common, yet subtle bug in MATLAB functions where an unexpected empty array `[]` is returned instead of a scalar value (e.g., 0 or NaN) under specific conditions. This can lead to errors or unexpected behavior later in your code.

The `bug.m` file contains the buggy function, while `bugSolution.m` provides a corrected version.

## Problem Description
The function `myFunction` should return a scalar value under all circumstances. However, when the condition `someCondition` is false, it returns an empty array `[]`. This unexpected empty array can cause problems when the function's output is used in further calculations or operations that require a numerical value.

## Solution
The solution is to explicitly handle the case where `someCondition` is false. Instead of returning an empty array, the function should return a scalar value (e.g., 0 or NaN) that indicates an appropriate default or invalid result. This ensures that subsequent operations are not affected by an unexpected empty array return.