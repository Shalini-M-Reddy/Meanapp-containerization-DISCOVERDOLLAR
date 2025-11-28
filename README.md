# MEAN Stack Application
A Full-stack MEAN(MongoDB, Express.js, Angular, Node.js) application built with scalable architecture and production-ready practices. This project follows modular coding standards, secure API design, and clean UI patterns suitable for real-world deployment.

1.Repository Setup
-Create a new GitHub repository for this project
-Push the complete code to the repository.

## Features
### **Frontend (Angular)**
- Responsive & modular component-based UI  
- Form validation using Angular Reactive Forms  
- Service-based API handling  
- Reusable shared modules  
- Clean routing and lazy loading structure  

### **Backend (Node.js + Express)**
- RESTful APIs with proper routing  
- Centralized error handling  
- Environment variable support  
- MongoDB integration using Mongoose  
- Authentication-ready folder structure  

### **Database (MongoDB)**
- Schema-based models  
- Indexing-ready structure  
- Data validation through Mongoose

### **Techstack**
- Angular
- Node.js, Express.js
- MongoDB

2.Containerization & Deployment
-Create Docker files for both the frontend and backend.
-Build and push Docker images to your Docker Hub account.
-Set up a new Ubuntu virtual machine on any cloud platform 
-Use Docker Compose to deploy the application on this VM.
-the official MongoDB Docker image as part of your Docker Compose setup.
mean-app/
│
├── backend/
│   ├── Dockerfile
│   └── (Node.js/Express app files)
│
├── frontend/
│   ├── Dockerfile
│   └── (Angular/React app files)
│
└── docker-compose.yml(with database set up)

3.CI/CD Pipeline Configuration
