# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running request blocking the event loop.  The example shows a simple HTTP server that simulates a 5-second delay in processing a request. During this delay, the server becomes unresponsive to new connections.

## Problem

Node.js is single-threaded.  If a request takes too long to process, the entire server can be blocked, preventing it from handling other requests. This example highlights this issue.

## Solution

The solution involves using worker threads or asynchronous operations to handle long-running tasks without blocking the event loop. This allows the server to remain responsive to other requests during processing of long tasks.  This example is demonstrated using asynchronous operations.