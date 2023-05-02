# JavaScript Basics in Express

This repository contains a series of controller functions I wrote using Express to create API endpoints for an application. It uses functions from my JavaScript Basics code, which are called when each controller function runs.

The starter files and end-to-end tests were cloned from: https://github.com/CommandShiftHQ/javascript-basics-express

## Getting started

### Clone this repository

- Create a fork of this repo.
- Clone your copy of the repo using the command: `git clone git@github.com:_your-github-username_/javascript-basics-express`

### Install the project dependencies

Use the command `npm install` to download the project's dependencies.

## Run the test code

Use the command `npm test` to run the Jest end-to-end tests.

To run the tests for each group of controller functions, use the commands:

- `npm test -- strings`
- `npm test -- numbers`
- `npm test -- booleans`
- `npm test -- arrays`

## Check the routes with Postman

- Use the command `npm start` to start your server
- Open Postman and enter http://localhost:3000
- Add the path specified in the controller function e.g. `/numbers/multiply`
- Check each controller function to see whether you need to make a GET request or POST request
- For GET requests, you can add your own parameters to the route. Parameters are indicated by a colon e.g. `/numbers/subtract/:b/from/:a`.
- For POST requests, you will need to add information to the request body. Select `Body` and `raw`, then select `JSON` from the dropdown. Check the corresponding end-to-end test to see what data is needed. It should be written in JSON format e.g
  {"value": true}
