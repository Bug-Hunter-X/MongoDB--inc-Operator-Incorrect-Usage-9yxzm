# MongoDB $inc Operator Bug
This repository demonstrates a common error when using the `$inc` operator in MongoDB. The `$inc` operator is used to increment a numerical field by a specified value. However, if a string is passed instead of a number, the operation fails, and the data may become corrupted.

## Bug
The `bug.js` file shows the incorrect usage of the `$inc` operator, where a string ('1') is passed instead of a number (1).  This leads to the update failing silently or producing unexpected results.

## Solution
The `bugSolution.js` file demonstrates the correct usage of the `$inc` operator, passing a numeric value to increment the field correctly.

## How to reproduce
1.  Clone this repository.
2.  Ensure a MongoDB instance is running.
3.  Run the `bug.js` script to see the error.  Then compare the results to running `bugSolution.js`.