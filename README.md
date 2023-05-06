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

- Use the command `npm start` to start your server.
- Open Postman and enter http://localhost:3000.
- Add the path specified in the controller function e.g. `/numbers/multiply`.
- Check each controller function to see whether you need to make a GET request or POST request.
- For GET requests, you can add your own parameters to the route. Parameters are indicated by a colon e.g. `/numbers/subtract/:b/from/:a`.
- For POST requests, you will need to add information to the request body. Select `Body` and `raw`, then select `JSON` from the dropdown. Check the corresponding end-to-end test to see what data is needed. It should be written in JSON format e.g
  {"value": true}.

### Strings

| Route                              | HTTP Verb | Description                                                           |
| ---------------------------------- | --------- | --------------------------------------------------------------------- |
| `/strings/hello/:string`           | GET       | Returns `Hello ${string}`                                             |
| `/strings/upper/:string`           | GET       | Returns the string in all uppercase                                   |
| `/strings/lower/:string`           | GET       | Returns the string in all lowercase                                   |
| `strings/first-characters/:string` | GET       | Returns a given number of characters from the beginning of the string |

### Numbers

| Route                          | HTTP Verb | Description                                            |
| ------------------------------ | --------- | ------------------------------------------------------ |
| `/numbers/add/:a/and/:b`       | GET       | Adds two numbers                                       |
| `/numbers/subtract/:b/from/:a` | GET       | Subtracts one number from another number               |
| `/numbers/multiply`            | POST      | Multiplies two numbers                                 |
| `/numbers/divide`              | POST      | Divides one number by another                          |
| `/numbers/remainder`           | POST      | Gives the remainder of dividiing one number by another |

### Booleans

| Route                                 | HTTP Verb | Description                                                                          |
| ------------------------------------- | --------- | ------------------------------------------------------------------------------------ |
| `/booleans/negate`                    | POST      | Returns true when passed false and false when passed true                            |
| `/booleans/truthiness`                | POST      | Returns false for falsy values and true for truthy values                            |
| `/booleans/is-odd/:a`                 | GET       | Returns true when passed an odd number and false when passed an even number          |
| `/booleans/:string/starts-with/:char` | GET       | Returns true when the string starts with a given character and false when it doesn't |

### Arrays

| Route                             | HTTP Verb | Description                                                  |
| --------------------------------- | --------- | ------------------------------------------------------------ |
| `/arrays/element-at-index/:index` | POST      | Returns the element at the given index                       |
| `/arrays/to-string`               | POST      | Returns the array as a string                                |
| `/arrays/append`                  | POST      | Returns the array with a given value appended                |
| `/arrays/starts-with-vowel`       | POST      | Returns a filtered array of elements that start with a vowel |
| `/arrays/remove-element`          | POST      | Returns an array with the element at the given index removed |
