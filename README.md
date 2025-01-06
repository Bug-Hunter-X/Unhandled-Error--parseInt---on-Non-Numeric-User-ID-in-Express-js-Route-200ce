# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  the lack of error handling when dealing with user input.  Specifically, the code attempts to parse a user ID from the route parameters as an integer but does not handle cases where the ID is not a valid number. This can lead to unexpected crashes or incorrect behavior.

## Bug Description

The `bug.js` file contains an Express.js route handler that fetches a user based on their ID.  The code uses `parseInt()` to convert the ID from a string to an integer. However, it lacks error handling if the ID is not a valid integer. This can cause a runtime error if a non-numeric ID is provided.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler. It includes comprehensive error handling to address the issue. The solution checks if the parsed ID is a number before using it to search for a user. If the ID is invalid, an appropriate error response is sent.

## How to Run

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install Express.js.
4. Run `node bug.js` to see the buggy version.
5. Run `node bugSolution.js` to see the corrected version.