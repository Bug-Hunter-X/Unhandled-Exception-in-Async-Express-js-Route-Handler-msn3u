# Unhandled Exception in Async Express.js Route Handler

This repository demonstrates a common error in Express.js applications: unhandled exceptions within asynchronous route handlers.  Improper error handling in such scenarios can lead to server crashes.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version with robust error handling.

## Problem

The issue lies in the asynchronous nature of the route handler.  An exception thrown inside the `setTimeout` callback isn't caught by the Express.js middleware, resulting in a server crash. 

## Solution

The solution involves using `try...catch` blocks to handle potential errors within the asynchronous operation.  This prevents unhandled exceptions from terminating the server and allows for graceful error handling, such as sending an appropriate error response to the client.