# MongoDB $inc Operator with String Value

This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations.  The `$inc` operator is designed to increment a numerical field by a specified value.  Attempting to increment a field with a string value will lead to unexpected results or errors.

## Bug
The provided `bug.js` file contains an example of this error.  The code attempts to increment the 'field' by the string value '1'. This will not result in the expected incrementation. Instead it will likely cause a failure or overwrite the field with the string value '1'. 

## Solution
The `bugSolution.js` file demonstrates the correct usage. The string value is parsed into a number before performing the update.