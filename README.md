✅ Task Management Application

A lightweight Task Management Application designed to help users organize, track, and manage daily tasks efficiently. The application allows creating, updating, deleting, and filtering tasks based on completion status and due dates.


📌 Project Description

The Task Management Application is a productivity tool that helps individuals or small teams manage their tasks effectively.
The Angular frontend offers a clean and intuitive UI, while the Spring Boot backend exposes RESTful APIs for task operations.
The system supports containerized deployment using Docker and is cloud-ready with Azure Container Instances.

🎯 Key Objectives

Improve task organization and productivity

Provide clear visibility of pending and completed tasks

Enable scalable and cloud-ready deployment

⚙️ Core Functionalities

Create new tasks

Edit existing tasks

Delete tasks

Mark tasks as Completed / Pending

Filter tasks by status

Sort tasks by due date

🛠️ Technology Stack
Layer	Technology
Frontend	Angular
Backend	Spring Boot, Spring Data JPA
Database	H2 / PostgreSQL
DevOps	Docker, Azure Container Instances
🧱 System Architecture
Angular UI → Spring Boot REST API → Database

🗄️ Database Design

Task Table

Field	Type
id	Long
title	String
description	String
completed	Boolean
due_date	Date
🔌 REST API Endpoints
Method	Endpoint	Description
GET	/api/tasks	Get all tasks
POST	/api/tasks	Create new task
PUT	/api/tasks/{id}	Update task
DELETE	/api/tasks/{id}	Delete task
PATCH	/api/tasks/{id}/status	Update task status
🐳 Docker Setup

Run the complete application using:

docker-compose up --build

☁️ Azure Deployment

Docker images pushed to Azure Container Registry

Deployed using Azure Container Instances

# TaskManagerFrontend

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 21.1.2.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Vitest](https://vitest.dev/) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.

