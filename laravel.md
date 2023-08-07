# Laravel Multitenant with REST API Coding Test

## Problem

Create a Laravel application that serves as a multitenant REST API backend for a fictional e-commerce platform. Each tenant will have its own set of products and orders.

## Requirements

Implement a multitenant architecture where each tenant has its own isolated database and data. The tenants should be identified using subdomains, e.g., `tenant1.yourdomain.com`, `tenant2.yourdomain.com`, etc.

The application should have the following API endpoints:

- `/api/products`: Get a list of products for the authenticated tenant.
- `/api/products/{id}`: Get details of a specific product for the authenticated tenant.
- `/api/orders`: Get a list of orders for the authenticated tenant.
- `/api/orders/{id}`: Get details of a specific order for the authenticated tenant.
- `/api/tenants`: Get a list of all tenants (accessible only to a superadmin user).

Implement API authentication using Laravel Sanctum. Tenants and users should be authenticated via API tokens. There should be two types of users:

- Superadmin: Can access all tenant data and perform CRUD operations on tenants.
- Tenant User: Can access only their tenant's data (products and orders).

Create database migrations and seeders to populate sample data for multiple tenants, products, and orders.

Implement proper error handling for API requests, including authentication failures and resource not found.

Use Laravel best practices, including proper use of Eloquent models, relationships, and validation.

Add pagination to the API endpoints that return lists of resources.

Write unit tests to ensure the correctness of the API endpoints and the multitenant functionality.

Implement proper logging for API requests and errors.

The code should be well-organized, commented, and readable.

## Submission

1. Create a public GitHub / BitBucket repository for your project.

2. Your repository must have a detailed README.md with instructions on how to set up & run your code locally. Include instructions for database setup, seeding, and running the application.

3. We would like you to present your work no later than 5 days from the day you receive your task.

### The presentation would be done in these steps:

1. Run your code locally and demonstrate how to set up different tenants and users.

2. Show the API endpoints in action, including getting products and orders for a specific tenant.

3. Explain your code, including how you implemented the multitenant architecture, API authentication, and database migrations.

4. Run tests and explain how you ensured code quality and correctness.

Feel free to use any additional packages or libraries you find useful. Provide the source code of the Laravel application, along with any necessary instructions to run it.

Remember, you can modify or extend this challenge according to your specific requirements and the skills you want to evaluate.

Good luck with the coding test!
