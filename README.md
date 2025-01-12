# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running operation in the request handler can make the server unresponsive. The example uses a simple `while` loop to simulate a time-consuming task, but this could be any CPU-bound operation.

## Bug

The `bug.js` file shows the problematic code.  The server becomes unresponsive when a request is made because the `while` loop blocks the event loop, preventing the server from processing any other requests.

## Solution

The `bugSolution.js` file demonstrates a solution using asynchronous operations. Instead of a blocking `while` loop, the solution uses `setTimeout` to simulate the long-running task asynchronously, allowing the event loop to continue processing other requests.

## How to Run

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js` to observe the unresponsive server.
4. Run `node bugSolution.js` to see the corrected version.