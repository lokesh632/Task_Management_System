# Task-Management-System

The Task Management System using PHP and MySQL can help a particular company manage its project task progress. The system has three system users: the Admin, Project Manager, and the Regular Employee.
Admin users can only create the Task Management System users. The admin user or the Project Managers will create a new project first and some essential details and references of the users. When creating a project, the admin or project managers must list all the employees to handle the project’s tasks. After completing the project, the regular employees are limited only to adding their work progress for the project they are assigned. They are also allowed to edit the data of the progress that they only submitted. Then, as the employees regularly update the system about their progress, the project managers will read or scan their activities. The project manager can check or decide if a particular task is done and need to update the system’s task status. For the system’s printable report, only the admin users and project managers have access to this function or feature of the system. The Admin user is those users who have access to all of the data stored in the system’s database, especially on creating and managing system users. The Project Managers are those users that contain the project details and progress under her/his management. The Regular Employees will submit their work productivity in each task of the project.

# Features
 - Login Page
 - Home Page
 - Project (CRUD Features)
 - Task List Page
 - Progress Form
 - Report Generation
 - User (CRUD Features)
 - Project Status
 - and Many More...


# Technologies Used
  - PHP
  - MySQL
  - HTML
  - CSS
  - JavaScript
  - Bootstrap
  - JQuery
  - Ajax

# API Endpoints

  - User Endpoints:

  - Task Endpoints:

  - Search and Filter Endpoints:

# Admin & Usage Examples

  - Admin Endpoints:

    - Register a new user:
      - Request: POST /api/users
        ```html
        http://localhost/task_management_system/index.php?page=user_list
        ```
      - Body:
        ```json
        {
            "name":"Administrator",
            "role":"admin",
            "username":"admin@admin.com",
            "password":"admin123"
        }
        ```
        <img src="Project_Screenshots/Admin_detail.JPG"/>

  - Admin Endpoints:

    - Register a new user:
      - Request: POST /api/users
        ```html
        http://localhost/task_management_system/index.php?page=user_list
        ```
      - Body:
        ```json
        {
            "name":"Lokesh",
            "role":"project manager",
            "username":"lokesh@gmail.com",
            "password":"1234"
        }
        ```


        <img src="Project_Screenshots/User_detail.JPG"/>
        
        
    -  Log in to a admin account:
      

        - Request: POST /api/users/login
          ```html
          http://localhost/task_management_system/login.php
          ```
        - Body:
          ```json
          {
              "username":"admin@admin.com",
              "password":"admin123"
          }
          ```

          <img src="Project_Screenshots/Admin_loginpage.JPG"/>
          
  
  - Task Endpoints:

    - Create a new task:
        - Request: POST /api/tasks/{token}
          ```html
          http://localhost/task_management_system/index.php?page=task_list
          ```
        - Body:
          ```json
          {
              "title":"title",
              "description":"description",
              "dueDate":"2023-09-22",
              "completed":"false"
          }
          ```

          <img src="Project_Screenshots/task_list.JPG"/>
          
    - Add a new project:
        - Request: PUT /api/tasks/{token}
          ```html
          http://localhost/task_management_system/index.php?page=new_project
          ```
        - Body:
          ```json
          {
              "title":"title",
              "description":"description",
              "dueDate":"2023-09-25",
          }
          ```

          <img src="Project_Screenshots/Add_project.JPG"/>

          
    - Assign a task to another user:
        - Request: PUT /api/tasks/{token}/{taskId}/{userId}
          ```html
          http://localhost/task_management_system/index.php?page=view_project&id=9
          ```

          <img src="Project_Screenshots/Project_view.JPG"/>

          
    - Mark a task as complete:
        - Request: PUT /api/tasks/complete/{token}/{taskId}
          ```html
          http://localhost/task_management_system/
          ```

          <img src="Project_Screenshots/Admin_Dashboard.JPG"/>

          
    - Admin detail:

      - Admin access:
      Body:
          ```json
          {
              "username":"admin@admin.com",
              "password":"admin123"
          }
          ```
          <img src="Project_Screenshots/Admin_detail.JPG"/>


    - User detail:

     - User access:
     Body:
          ```json
          {
              "username":"rameshs@gmail.com",
              "password":"ramesh123"
          }
          ```
          <img src="Project_Screenshots/User_detail.JPG"/>

    - Manage Acc:

        <img src="Project_Screenshots/Manage_acc.JPG"/>      

    - Reports:
        
        <img src="Project_Screenshots/Report.JPG"/>

 

