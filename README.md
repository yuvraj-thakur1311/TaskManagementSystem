# Task Management System

🌟 Objective: 


Develop a feature-rich Task Management System that demonstrates proficiency in software development, problem-solving, and understanding of real-world scenarios. The system should allow users to create, assign, track, and manage tasks efficiently. 


 Core Requirements:

 
✅ User Authentication:


 - Secure user registration and login functionalities.

 - Industry-standard practices for password storage and session management (e.g., bcrypt for hashing passwords, JWT for session management).

✅ Task Management:

- Create tasks with attributes: title, description, due date, priority, and status.

- Implement full CRUD operations (Create, Read, Update, Delete) for tasks.

✅ Team Collaboration:


- Allow users to assign tasks to other registered users.

- Implement a notification system to alert users when a task is assigned.
- 

✅ Dashboard:


- Display tasks that are:

- Assigned to the user.

- Created by the user.

- Overdue tasks.

✅ Search and Filter:
Search by task title or description.

Filter based on status, priority, and due date.


# Technical Specifications:


 - Frontend: Next.js (React framework for SSR and optimized performance).

 - Backend: Node.js with Express (for building the REST API).

 - Database: MongoDB (for storing task and user data).

 - Version Control: Host the code on a public Git repository (GitHub/GitLab) with clear and meaningful commit messages.


 # Setup Instructions:
 
Clone the repository:


 - git clone <repository-url>
 
- cd task-management-system


Install dependencies:

- For the frontend:

    - cd frontend
     - npm install
 
  
- For the backend:

    - cd backend
    - npm install
 

- Environment Setup:

Create a .env file in both the frontend and backend directories and add the required environment variables. For example:

  -  Frontend (frontend/.env):

        - NEXT_PUBLIC_API_URL=http://localhost:5000/api
   
    
 - Backend (backend/.env):

    
    PORT=5000
    DB_URI=mongodb://localhost:27017/task_manager
    JWT_SECRET=your_jwt_secret

   
- Run the application:

For the frontend:

    cd frontend
    npm run dev

    
For the backend:


    cd backend
    npm run dev

    
 - Access the app:

      Open your browser and navigate to http://localhost:3000 for the frontend.
      
      The backend API will be accessible at http://localhost:5000.

