# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, causing the server to become unresponsive. The solution showcases how to use asynchronous operations or worker threads to prevent this issue. 

## Bug

The `server.js` file contains a Node.js HTTP server with a request handler that performs a 5-second long synchronous operation.  This blocks the event loop, and the server will not be able to respond to further requests until the long operation completes.

## Solution

The `serverSolution.js` file demonstrates how to resolve this by refactoring the code to use asynchronous operations and prevent blocking the event loop.