# Task Management API

You are tasked with building a Task Management API using Laravel. The API will allow users to create, update, and delete tasks. Additionally, the API should include features related to task scheduling and processing using Laravel queues.

## Requirements

1. Set up a new Laravel project.
2. Create a RESTful API with the following endpoints:
   - `POST /api/tasks`: Create a new task.
   - `GET /api/tasks`: Get a list of all tasks.
   - `GET /api/tasks/{id}`: Get details of a specific task.
   - `PUT /api/tasks/{id}`: Update a task's details.
   - `DELETE /api/tasks/{id}`: Delete a task.
3. Task attributes: `title`, `description`, `due_date`, `status` (pending, completed), `priority` (low, medium, high).
4. Implement a queue job for sending task reminder emails to users a day before the task's due date.
5. Implement a scheduler that runs every hour to process the queue.
6. Write appropriate validation and error handling for the API endpoints.
7. Use Laravel's built-in Eloquent ORM for database interactions.
8. Use appropriate HTTP status codes and JSON responses for API interactions.

## Bonus (Optional)

- Implement user authentication and associate tasks with authenticated users.
- Add pagination to the list of tasks endpoint.
- Implement sorting and filtering options for the list of tasks.
- Write unit tests for your API endpoints and queue job.

## Submission

1. Create a public GitHub / BitBucket repository for your project.

2. Your repository must have a detailed README.md with instructions on how to set up & run your code locally. Include instructions for database setup, seeding, and running the application.

3. We would like you to present your work no later than 3 days from the day you receive your task.


This test aims to assess your ability to set up a Laravel project, design RESTful APIs, work with queues and schedulers, implement validation and error handling, and potentially tackle additional features. Feel free to adapt the task as needed and add more complexity based on your expertise level.
