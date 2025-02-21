This repository demonstrates a common JavaScript closure issue encountered when using `setTimeout` within a loop. The issue arises because the `setTimeout` callback function does not capture the value of `i` at the time it's created, but rather captures a reference to the variable `i`.  Therefore, by the time the `setTimeout` callbacks finally execute, the loop has already completed, and `i` will hold its final value (10). The solution demonstrates how to use an immediately invoked function expression (IIFE) to correctly capture the value of `i` for each iteration of the loop.