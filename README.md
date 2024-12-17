# JavaScript Closure Issue in `setTimeout` Loop

This repository demonstrates a common JavaScript closure issue encountered when using `setTimeout` within a loop.  The problem arises because of how variables are captured within closures.  In the `bug.js` file, all `setTimeout` callbacks reference the *final* value of `i` (10), rather than the value of `i` at the time each callback is created.

The `bugSolution.js` file provides a solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, effectively capturing the correct value of `i`.  This is a common and effective way to avoid this type of closure problem in JavaScript.