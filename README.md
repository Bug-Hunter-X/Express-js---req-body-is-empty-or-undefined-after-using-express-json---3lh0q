# Express.js - Empty req.body Issue

This repository demonstrates a common issue in Express.js applications where the `req.body` is empty or undefined even after applying the `express.json()` middleware.  The problem often stems from incorrect middleware placement or configuration issues with body parsers.

## Bug Description

The provided `bug.js` file shows a simple Express.js application that attempts to parse a JSON request body. Despite using `express.json()`, the `req.body` remains empty when a POST request is sent.

## Solution

The `solution.js` file corrects this by ensuring that the `express.json()` middleware is placed before the route handler that expects a JSON body.  This ensures the body parser is invoked before the route handler processes the request.