# Node.js Server Hang: Missing res.end()

This repository demonstrates a common error in Node.js HTTP servers: forgetting to call `res.end()` to properly close the response.  This can lead to the server becoming unresponsive.

## The Bug
The `bug.js` file contains a simple HTTP server that omits the crucial `res.end()` call. This causes the server to hang and fail to respond correctly to subsequent requests.

## The Solution
The `bugSolution.js` file provides the corrected code with the added `res.end()` call. This ensures that the response is properly closed and the server functions as expected.  This demonstrates the correct way to handle HTTP responses in Node.js.

## How to Reproduce
1. Clone this repository.
2. Run `node bug.js`.
3. Try making requests to the server; note the lack of response.
4. Run `node bugSolution.js`.  The server will now respond correctly.