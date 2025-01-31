# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input. The example shows a route that retrieves a user by ID.  If the ID is not a valid number, the application will crash.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides a corrected version with robust error handling.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Access the route with an invalid ID, e.g., `/users/abc`

## Solution

The solution involves using `isNaN` to check if the userId is a valid number before parsing and performing the lookup.
