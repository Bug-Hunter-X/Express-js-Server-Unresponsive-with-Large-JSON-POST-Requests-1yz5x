# Express.js Server Unresponsiveness with Large JSON POST Requests

This repository demonstrates a common issue in Express.js applications where the server becomes unresponsive when handling large JSON POST requests. The problem arises from synchronous request processing, causing the server to block and fail to respond to subsequent requests.

## Bug

The `bug.js` file contains an Express.js application that processes JSON POST requests.  A `setTimeout` function simulates an asynchronous operation, but the request handling itself is synchronous.  When a large JSON payload is sent, the server becomes unresponsive for the duration of the processing time, leading to a poor user experience and potential timeouts.

## Solution

The `bugSolution.js` file provides a solution using asynchronous request handling with promises or async/await to prevent blocking requests and improve server responsiveness. The use of async/await makes the code more readable.  This ensures the server remains responsive to other requests while handling large JSON payloads.