# Unexpected NaN comparison in JavaScript

This repository demonstrates a common, yet easily overlooked, issue in JavaScript related to comparing NaN (Not a Number) values.

## The Problem

In JavaScript, `NaN` (Not a Number) is a special value that represents the result of an invalid numerical operation.  The peculiar behavior of `NaN` is that it is *not equal* to itself, regardless of whether you use loose (`==`) or strict (`===`) equality comparison.

The provided `bug.js` file showcases this unexpected behavior.  The function `foo` attempts to compare two values, including `NaN`, for equality, but yields incorrect results.

## The Solution

The recommended solution is to use the `Number.isNaN()` method to reliably check if a value is `NaN`.  This method accurately identifies `NaN` without exhibiting the inconsistent behavior of equality operators.  The `bugSolution.js` file provides an improved version of the function, leveraging `Number.isNaN()` for correct comparisons.

## How to run the code

1. Clone this repository.
2. Navigate to the repository's directory using your terminal.
3. Run the JavaScript files using Node.js (or your preferred JavaScript runtime):
   ```bash
   node bug.js
   node bugSolution.js
   ```