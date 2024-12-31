# Node.js Server Unexpected Crash

This repository demonstrates a bug in a Node.js HTTP server where the server unexpectedly crashes after handling a certain number of requests. The crash occurs without any helpful error messages or logs.

## Bug Description

A simple Node.js HTTP server is created using the `http` module.  Under normal circumstances, this server should run indefinitely, handling incoming requests. However, after a number of requests, the server crashes without any apparent reason or error messages in the console.

## Bug Reproduction

1. Clone this repository.
2. Run `node server.js`.
3. Send multiple requests to the server (e.g., using `curl` or a browser). After a certain number of requests, the server will crash.

## Solution

The solution involves adding error handling to the server's `listen` method.  This prevents the server from crashing unexpectedly. A detailed solution is provided in `serverSolution.js`.