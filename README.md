# Node.js EADDRINUSE Error

This repository demonstrates a common Node.js error: `EADDRINUSE: address already in use :::8080`. This occurs when a server attempts to bind to a port that's already occupied by another process.

The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution for handling this error gracefully.

## How to Reproduce

1. Clone the repository.
2. Run `server.js`.
3. Attempt to run another instance of `server.js` (or any other application using port 8080).

You should encounter the `EADDRINUSE` error.

## Solution

The solution involves using the `server.on('error', ...)` event handler to check for the `EADDRINUSE` error and handle it appropriately (e.g., retrying after a delay or exiting gracefully). Refer to `serverSolution.js` for an example.