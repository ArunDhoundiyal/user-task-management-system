### Here are the URLs for the CRUD operations based on your app's deployment at https://user-task-management-system.onrender.com. These URLs assume you are implementing the basic CRUD operations for user and task management:

### 1. User Operations
### User Registration (POST)

### URL: https://user-task-management-system.onrender.com/user_registration
Request Body:
json
Copy code
{
  "id": "150e8400-e29b-41d4-a716-446655440002",
  "userName": "Arun Dhoundiyal",
  "email": "arun@gmail.com",
  "password": "Arun@1234"
}
### User Login (POST)

### URL: https://user-task-management-system.onrender.com/user_login
Request Body:
json
Copy code
{
  "email": "arun@gmail.com",
  "password": "Arun@1234"
}
User Profile (GET)

### URL: https://user-task-management-system.onrender.com/user_profile
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
### 2. Task Operations
Create Task (POST)

### URL: https://user-task-management-system.onrender.com/create_task
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
Request Body:
json
Copy code
{
  "taskName": "Create Task Tracking Management System",
  "description": "I created a Task Tracking Management System as an assignment that I got from a company Robotspace",
  "dueDate": "2024-12-31",
  "status": "In Progress",
  "priority": "High"
}
Get Task (GET)

### URL: https://user-task-management-system.onrender.com/get_task/<task_id>
* Example: https://user-task-management-system.onrender.com/get_task/8
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
Delete Task (DELETE)

### URL: https://user-task-management-system.onrender.com/delete_task/<task_id>
* Example: https://user-task-management-system.onrender.com/delete_task/7
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
Delete All Tasks (DELETE)

### URL: https://user-task-management-system.onrender.com/delete_all_task
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
Edit Task (PUT)

### URL: https://user-task-management-system.onrender.com/edit_task/<task_id>
* Example: https://user-task-management-system.onrender.com/edit_task/8
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
Request Body:
json
Copy code
{
  "taskName": "Create Task Tracking Management System",
  "description": "I created a Task Tracking Management System as an assignment that I got from a company Robotspace",
  "dueDate": "2024-12-31",
  "status": "Completed",
  "priority": "Low"
}
Get Task List (GET)

### URL: https://user-task-management-system.onrender.com/task_list/?status=&search=
* Example: https://user-task-management-system.onrender.com/task_list/?status=In Progress&search=task
Headers:
makefile
Copy code
Authorization: Bearer <JWT_TOKEN>
General Notes
Replace <JWT_TOKEN> with the actual JWT token you get after successful user login.
The task_id in the URLs for getting, editing, and deleting tasks should be replaced with the actual task ID you want to manage.
