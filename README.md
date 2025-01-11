# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when using Express.js to parse JSON request bodies.  The problem arises when the request body is either empty or contains invalid JSON data.  The server fails to properly handle these cases, potentially leading to unexpected errors or behavior.

## Bug Description
The provided Express.js server uses `express.json()` middleware to parse incoming JSON requests. However, it does not gracefully handle situations where the request body is empty or contains malformed JSON.  This can result in the server throwing an error or failing silently, preventing proper processing of the request.

## Solution
The solution involves adding error handling to catch JSON parsing errors.  This allows the server to respond appropriately, even when the request body is invalid.  The solution also provides a more robust way to handle the missing body case. 