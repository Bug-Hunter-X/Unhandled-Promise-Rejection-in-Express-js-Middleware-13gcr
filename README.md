# Unhandled Promise Rejection in Express.js Middleware

This example demonstrates a common error in Node.js Express.js applications: insufficient error handling within asynchronous middleware.  When an asynchronous operation (like a database query) fails, the error might not be properly handled, leading to a silent failure or an incomplete response to the client.

## Bug Description
The provided `bug.js` code features an Express.js route handler that performs an asynchronous operation.  If this operation throws an error, the error is logged to the console, but the Express response is not handled, resulting in the client not receiving a proper error message.

## Solution
The `bugSolution.js` code shows how to correctly handle errors within asynchronous middleware.  It uses a `try...catch` block to capture any errors and send an appropriate error response to the client.