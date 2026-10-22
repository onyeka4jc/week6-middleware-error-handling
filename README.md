# Week 6: Middleware and Error Handling in Express



## Project Overview

This project builds on the Week 3 Todo API for the BeTechified Week 6 assignment. It demonstrates Express middleware, Joi validation, error handling, and API testing.



## Features

- Request logging middleware records request details and response status.

- Joi validates task creation and updates.

- Task names must contain at least three characters.

- Asynchronous route handlers use try/catch and forward errors.

- Centralized error-handling middleware returns appropriate status codes and JSON messages.

- MongoDB and Mongoose manage Todo records.



## Technologies

Node.js, Express.js, Joi, MongoDB Atlas, Mongoose, and dotenv.



## Installation

1. Install Node.js.

2. Clone this repository.

3. Install dependencies by running `npm install`.

4. Create a local `.env` file containing your MongoDB connection string:



`MONGODB_URI=your_mongodb_connection_string`



Replace the example value with your actual connection string. Never upload `.env` or publish database credentials.



## Running the Application

Development mode: `npm run dev`



Normal startup: `npm start`



## API Endpoints



| Method | Endpoint | Purpose |

|---|---|---|

| GET | `/todos` | Retrieve all Todo tasks |

| GET | `/todos/active` | Retrieve active tasks |

| GET | `/todos/completed` | Retrieve completed tasks |

| GET | `/todos/:id` | Retrieve one task |

| POST | `/todos` | Create a task |

| PUT | `/todos/:id` | Update a task |

| PATCH | `/todos/:id` | Partially update a task |

| DELETE | `/todos/:id` | Delete a task |



## Required Week 6 Tests



1. Successful `GET /todos` request â€” expected `200 OK`.

2. Successful `POST /todos` with `{"task":"Learn Express"}` â€” expected `201 Created`.

3. Invalid task: `POST /todos` with `{"task":"Hi"}` â€” expected `400 Bad Request`.

4. Missing task: `POST /todos` with `{}` â€” expected `400 Bad Request`.

5. Invalid update: `PATCH /todos/EXISTING_ID` with `{"task":"No"}` â€” expected `400 Bad Request`.



For Test 5, replace `EXISTING_ID` with an actual Todo ID. Send JSON bodies with the `Content-Type: application/json` header.



Capture screenshots of successful responses, validation failures, and terminal logs. Repeat the required failure tests against the deployed Render application and capture the results.



## Render Deployment



Build command: `npm install`



Start command: `npm start`



Configure `MONGODB_URI` in the Render service's environment settings. Ensure the deployed service can connect to MongoDB Atlas.



**Live Render URL:** https://week6-middleware-error-handling.onrender.com



## Assignment Objective

Demonstrate request logging, Joi validation, try/catch in asynchronous routes, centralized error handling, API testing, and deployment.
