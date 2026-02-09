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
System Architecture
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

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```
🧩 Entities & Attributes
1️⃣ TEAM Table

Represents a group or team of users.

Attribute	Type	Description
team_id	INT (PK)	Unique identifier for the team
name	VARCHAR	Team name
created_at	DATETIME	Team creation timestamp

📌 Purpose:
Organizes users into teams (useful for small teams or organizations).

2️⃣ USERS Table

Stores user account information.

Attribute	Type	Description
user_id	INT (PK)	Unique user ID
name	VARCHAR	User’s name
email	VARCHAR	User email
password	STRING	Encrypted password
team_id	INT (FK)	References TEAM

📌 Purpose:
Each user belongs to one team, but a team can have many users.

3️⃣ TASKS Table

Stores task details created by users.

Attribute	Type	Description
task_id	INT (PK)	Unique task ID
description	TEXT	Task description
status	ENUM	Completed / Pending
due_date	DATE	Task deadline
created_at	DATETIME	Task creation time
user_id	INT (FK)	Assigned user
category_id	INT (FK)	Task category

📌 Purpose:
Tracks all tasks, their status, deadlines, and ownership.

4️⃣ CATEGORIES Table

Defines task categories.

Attribute	Type	Description
category_id	INT (PK)	Category ID
name	VARCHAR	Category name

📌 Purpose:
Helps group tasks (e.g., Work, Personal, Urgent).

🔗 Relationships Explained
🔹 TEAM → USERS

One-to-Many (1:M)

One team can have many users

Each user belongs to exactly one team

📌 Implemented using:

USERS.team_id → TEAM.team_id

🔹 USERS → TASKS

One-to-Many (1:M)

One user can create multiple tasks

Each task is assigned to one user

📌 Implemented using:

TASKS.user_id → USERS.user_id

🔹 CATEGORIES → TASKS

One-to-Many (1:M)

One category can have many tasks

Each task belongs to one category



🔄MAPPING

@OneToMany → Team → Users

@ManyToOne → User → Team

@OneToMany → User → Tasks

@ManyToOne → Task → User

@ManyToOne → Task → Category







