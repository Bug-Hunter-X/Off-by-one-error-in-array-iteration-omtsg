# Off-by-one Error in Java Array Iteration

This repository demonstrates a common off-by-one error in Java when iterating over an array. The error occurs when the loop condition allows the index to go beyond the valid bounds of the array, resulting in an `ArrayIndexOutOfBoundsException`.

The `Bug.java` file contains the buggy code, while `BugSolution.java` provides the corrected version.

## Bug
The bug lies in the `for` loop's condition `i <= arr.length`.  Array indices are zero-based, so the valid indices for an array of length `n` are 0 to `n-1`.  The incorrect condition attempts to access `arr[arr.length]`, which is out of bounds.

## Solution
The solution changes the loop condition to `i < arr.length`, ensuring that the loop terminates before attempting to access an invalid index.