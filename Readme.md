# API VERSIONING (Express Middleware)

Name: api-versioning
Version: 2.0.0
License: MIT

## Description

Express API Versioning is an Express.js middleware that dynamically loads
different API versions based on the version number specified in the request URL.
It helps maintain multiple API versions cleanly without breaking existing clients.

[Full Guide to Build an API Versioning & Deprecation Manager in NodeJs.](https://www.sevensquaretech.com/nodejs-api-versioning-deprecation-manager-with-github-code/)

## Features

- Supports URL-based API versioning (e.g., /v1/users, /v2/users)
- Seamless switching between API versions
- Works with Express 4.x
- Lightweight and easy to integrate

## Installation

Install using npm:

npm install api-versioning

Peer Dependency:

- express (4.x)

## Basic Usage

Example Express setup:

const express = require('express');
const versioning = require('api-versioning');

const app = express();

app.use(versioning({
apiPath: './api',
defaultVersion: 'v1'
}));

app.listen(3000, () => {
console.log('Server running on port 3000');
});

## Project Structure Example

api/
├── v1/
│ └── users.js
└── v2/
└── users.js

## Scripts

- npm test : Run test cases using Mocha
- npm run build : Build the project using Babel
- npm run coveralls : Generate coverage report

## Testing

Tests are written using Mocha, Chai, and Supertest.

Run tests:
npm test

## Development

This project uses Babel for transpiling modern JavaScript features.

Build Output:

- Source: src/
- Compiled: build/

## Keywords

express, api, versioning, express api versioning, expressjs
