# Task Management System

# Objective: 


Develop a feature-rich Task Management System that demonstrates proficiency in software development, problem-solving, and understanding of real-world scenarios. The system should allow users to create, assign, track, and manage tasks efficiently. 


 # Core Requirements:

 
✅ User Authentication:


 - Secure user registration and login functionalities.

 - Industry-standard practices for password storage and session management (e.g., bcrypt for hashing passwords, JWT for session management).

✅ Task Management:

- Create tasks with attributes: title, description, due date, priority, and status.

- Implement full CRUD operations (Create, Read, Update, Delete) for tasks.

✅ Team Collaboration:


- Allow users to assign tasks to other registered users.

- Implement a notification system to alert users when a task is assigned.
  

✅ Dashboard:


- Display tasks that are:

- Assigned to the user.

- Created by the user.

- Overdue tasks.
  

✅ Search and Filter:

 - Search by task title or description.

 - Filter based on status, priority, and due date.
   


# Technical Specifications:


 - Frontend: Next.js (React framework for SSR and optimized performance).

 - Backend: Node.js with Express (for building the REST API).

 - Database: MongoDB (for storing task and user data).

 - Version Control: Host the code on a public Git repository (GitHub/GitLab) with clear and meaningful commit messages.


 # Setup Instructions:
 
- Clone the repository:

      git clone <repository-url>
      cd task-management-system


- Install dependencies:

   - For the frontend:

          cd frontend
          npm install
 
  
   - For the backend:

         cd backend
         npm install
 

 - Environment Setup:

   Create a .env file in both the frontend and backend directories and add the required environment variables. For example:

      -  Frontend (frontend/.env):

              NEXT_PUBLIC_API_URL=http://localhost:5000/api
   
    
      - Backend (backend/.env):

             
             PORT=5000
             DB_URI=mongodb://localhost:27017/task_manager
             JWT_SECRET=your_jwt_secret

   
- Run the application:

     - For the frontend:

              cd frontend
              npm run dev

    
     - For the backend:


             cd backend
             npm run dev

    
 - Access the app:

       Open your browser and navigate to http://localhost:3000 for the frontend.
       The backend API will be accessible at http://localhost:5000.
   

# Approach Explanation:


- Frontend (Next.js):

The frontend was built using Next.js to take advantage of its server-side rendering (SSR) and static site generation (SSG) capabilities, ensuring fast load times and SEO optimization. Components are modularized for ease of maintenance, with dynamic routes for task CRUD operations and user authentication.

- Backend (Node.js with Express):
  
The backend API follows RESTful principles and exposes endpoints for task management, user authentication, and notifications. It uses JWT for stateless authentication and bcrypt for password hashing. Task and user data are stored in MongoDB (or PostgreSQL, depending on choice) for scalability and efficiency.

- Database (MongoDB):

MongoDB was chosen for its flexibility with JSON-like data structures, which suits task data with varying attributes. 

- Authentication & Authorization:

User authentication is handled through JWT (JSON Web Tokens). Users must authenticate via the login process before accessing protected routes. Role-based access control (RBAC) can be implemented for different user roles (Admin, Manager, Regular User).

- Task Management:
  
The system supports the full lifecycle of task management, allowing users to create, update, delete, and view tasks. Filtering and searching are enabled for users to efficiently manage their tasks.

- Notifications:

A basic notification system can be implemented to alert users when a task is assigned to them. This can be expanded to include real-time notifications using Socket.io.


# Assumptions / Trade-offs:


- Assumptions:

   - The user base is relatively small, so a simple JWT-based authentication mechanism is sufficient.

   - MongoDB was chosen as the default database for flexibility, but PostgreSQL is also supported for those preferring relational databases.

   - Task assignments are only performed by authenticated users.
     

- Trade-offs:

  - The notification system is currently basic; real-time notifications could be added using WebSockets for a more advanced experience.
  
  - Although role-based access control is not part of the core requirements, it can be added as an optional feature.

