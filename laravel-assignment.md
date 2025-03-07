# PHP Machine Test - Laravel

## Objective
Develop a small Laravel-based API for a "Task Management System" where users can create tasks, assign them, and mark them as completed. This test will evaluate your ability to work with Laravel’s core concepts, including queues, jobs, service containers, dependency injection, scheduling, middleware, and authentication using Sanctum.

---

## Requirements
1. **Use Laravel 11+** with PHP 8.3+
2. **Use Laravel Sanctum** for authentication
3. **Implement a Queue & Job** to send task assignment notifications
4. **Use a Custom Middleware** to log request execution time
5. **Implement Dependency Injection** for a Task Service
6. **Schedule a Command** to automatically mark overdue tasks as "expired"
7. **Use MySQL** as the database

---

## Task Details

### 1. User Authentication (Laravel Sanctum)
- Implement **user registration** and **login APIs** using Laravel Sanctum.
- Only authenticated users should be able to create and assign tasks.

### 2. Task Management API
#### Endpoints
1. `POST /api/tasks` - Create a new task (Authenticated)
2. `PUT /api/tasks/{id}/assign` - Assign a task to a user
3. `PUT /api/tasks/{id}/complete` - Mark a task as completed
4. `GET /api/tasks` - List all tasks with filters (status, assigned user, etc.)

#### Task Fields
- `id`
- `title` (string, required)
- `description` (text, nullable)
- `assigned_to` (foreign key to users table, nullable)
- `status` (enum: `pending`, `completed`, `expired`, default: `pending`)
- `due_date` (datetime, nullable)
- `created_at`, `updated_at`

### 3. Queues & Jobs (Notification System)
- When a task is assigned to a user, a **Job** should be dispatched to send an email notification to the assigned user.
- Use Laravel’s **queue system** (Database queue driver) to handle this asynchronously.

### 4. Custom Middleware (Log Execution Time)
- Create middleware that **logs request execution time** in `storage/logs/laravel.log`.
- Apply this middleware to all API routes.

### 5. Service Container & Dependency Injection
- Create a **TaskService** to handle business logic (e.g., creating, assigning, completing tasks).
- Inject **TaskService** into the TaskController instead of calling models directly.

### 6. Scheduler (Expire Overdue Tasks)
- Create a Laravel **Command** that:
  - Runs every hour.
  - Checks for tasks with a past `due_date` that are still `pending`.
  - Marks them as `expired`.
- Register the command in the Laravel **scheduler**.

---

## Bonus (Optional)
1. Use **Event-Listener** to log when a task is completed.
2. Implement **API Resource Transformations** for the Task model.

---

## Submission Instructions
1. Upload your project to **GitHub/GitLab** (Make it public).
2. Share the repository link.
3. Provide a **README.md** with setup instructions.

---

### Evaluation Criteria
✅ Code Quality & Best Practices  
✅ Proper Use of Laravel Concepts  
✅ Working APIs with Authentication  
✅ Handling Async Jobs & Scheduling  
✅ Middleware and Dependency Injection
