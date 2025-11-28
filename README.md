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
<img width="3200" height="2000" alt="Screenshot (591)" src="https://github.com/user-attachments/assets/18d24728-a925-4048-9d28-b7775088767c" />
<img width="3200" height="2000" alt="Screenshot (590)" src="https://github.com/user-attachments/assets/6bfd5bdf-e8ee-4479-b2f5-71c11ae411a5" />
<img width="3200" height="2000" alt="Screenshot (597)" src="https://github.com/user-attachments/assets/c4496ebb-6515-47a1-a05a-06901c754856" />
<img width="3200" height="2000" alt="Screenshot (596)" src="https://github.com/user-attachments/assets/d8004732-f0f5-4429-a103-a257fe6d6951" />

-Build and push Docker images to your Docker Hub account.  
<img width="3200" height="2000" alt="Screenshot (595)" src="https://github.com/user-attachments/assets/8cdff907-c84b-4682-ad0b-30db446664cc" />

-Set up a new Ubuntu virtual machine on any cloud platform.                                                                                                                                                                   
-Use Docker Compose to deploy the application on this VM.    

-the official MongoDB Docker image as part of your Docker Compose setup.  
<img width="3200" height="2000" alt="Screenshot (601)" src="https://github.com/user-attachments/assets/4977c18a-5576-488c-9b4f-3bace0fcf3b5" />
<img width="3200" height="2000" alt="Screenshot (600)" src="https://github.com/user-attachments/assets/605d0720-ddb5-40e9-8483-9451e32f9c91" />
<img width="3200" height="2000" alt="Screenshot (599)" src="https://github.com/user-attachments/assets/3f20f004-cb50-4c95-bfad-c44bf9214393" />
<img width="3200" height="2000" alt="Screenshot (598)" src="https://github.com/user-attachments/assets/1f0e3d8c-3d52-4dfc-ad30-87ce680025ee" />

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
