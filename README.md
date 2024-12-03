# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the route `/users/:id` attempts to parse the `id` parameter as an integer without checking if it's a valid integer.  This can lead to unexpected errors if a non-integer ID is passed.

The `bug.js` file shows the flawed code. The `bugSolution.js` file provides the corrected code with improved error handling.

## How to Reproduce
1. Clone this repository.
2. Run `npm install express` to install the required package.
3. Run `node bug.js` and navigate to a route with an invalid user ID.  For example, `/users/abc`. You'll see an error because of the missing error handling.
4. Run `node bugSolution.js` to see the solution which includes improved error handling.