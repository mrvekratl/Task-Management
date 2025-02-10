# Task Management API

A scalable Task Management API built with ASP.NET Core, implementing SOLID principles, Entity Framework Core, and a layered architecture for efficient management of tasks, projects, users, and notifications.

## Project Structure

The solution is organized into the following projects:

- **TaskManagement.API**: Contains controllers and middleware for handling HTTP requests and responses.
- **TaskManagement.Application**: Defines interfaces for repositories and services, manages validation, configures Data Transfer Objects (DTOs), and sets up dependency injection.
- **TaskManagement.Common**: Contains DTOs for Notifications, Projects, Tasks, and Users, as well as enumerations used across the application.
- **TaskManagement.Domain**: Defines the core domain entities, including base entities and specific entities for Notifications, Projects, Tasks, and Users.
- **TaskManagement.Infrastructure**: Implements background services and other infrastructure-related functionalities.
- **TaskManagement.Persistence**: Contains the ApplicationDbContext utilizing Entity Framework Core and implements the generic repository pattern.

## API Endpoints

The API provides the following endpoints:

### Task Endpoints

- **POST** `/Task/Create`: Create a new task.
- **GET** `/Task/Get`: Retrieve a list of all tasks.
- **GET** `/Task/Get/{id}`: Retrieve a specific task by its ID.
- **GET** `/Task/DueDate`: Retrieve tasks sorted by their due dates.
- **PUT** `/Task/Update/{id}`: Update an existing task by its ID.
- **PUT** `/Task/Assignment`: Assign a task to a project.
- **PUT** `/Task/UnAssignment/{id}`: Unassign a task from a project.
- **DELETE** `/Task/Delete/{id}`: Delete a task by its ID.

### User Endpoints

- **POST** `/User/Create`: Create a new user.
- **GET** `/User/Get`: Retrieve a list of all users.
- **GET** `/User/Get/{id}`: Retrieve a specific user by their ID.
- **PUT** `/User/Update/{id}`: Update an existing user by their ID.
- **DELETE** `/User/Delete/{id}`: Delete a user by their ID.

### Project Endpoints

- **POST** `/Project/Create`: Create a new project.
- **GET** `/Project/Get`: Retrieve a list of all projects.
- **GET** `/Project/Get/{id}`: Retrieve a specific project by its ID.
- **PUT** `/Project/Update/{id}`: Update an existing project by its ID.
- **DELETE** `/Project/Delete/{id}`: Delete a project by its ID.

### Notification Endpoints

- **GET** `/Notification/Get`: Retrieve a list of all notifications.
- **GET** `/Notification/Get/{id}`: Retrieve a specific notification by its ID.
- **DELETE** `/Notification/Delete/{id}`: Delete a notification by its ID.

> **Note**: Notifications are automatically generated when a user is assigned to or unassigned from a task.

## API Documentation

For detailed API documentation and additional endpoints, access the Swagger UI by navigating to `/swagger` in your web browser after running the API.

---

This project demonstrates the implementation of a scalable and maintainable Task Management API using modern development practices. For more information and contributions, please visit the [repository](https://github.com/mrvekratl/Task-Management).



