# Firebase Realtime Database Transaction Bug
This repository demonstrates a common error when using Firebase Realtime Database transactions: handling null initial values. The `transaction` method requires a return value, even if the current value is null.  Failure to return a value will result in the transaction silently failing.

## Bug
The `bug.js` file shows an incorrect implementation where the function returns nothing when the current score is null. This leads to unpredictable behavior.

## Solution
The `bugSolution.js` file provides the correct implementation, showing how to handle the null case by providing a default value or null.