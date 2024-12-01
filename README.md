Objectives
The goal of this project is to:

Set up a full-stack microservices architecture using Docker.
Deploy an API that connects to an MS SQL Server database.
Set up a CI/CD pipeline using Jenkins to automate builds and deployment.
Provide proper documentation for setup and usage.
Technology Stack
Frontend: Not included (focus on the backend microservices architecture).
Backend:
ASP.NET Core Web API for the RESTful service.
Entity Framework Core for database interaction.
Database: MS SQL Server.
Containerization: Docker for containerizing the microservices.
CI/CD: Jenkins for continuous integration and deployment.
Project Setup
Prerequisites
Git – For version control.
Docker Desktop – For containerization of the microservices and database.
Jenkins – For CI/CD pipeline automation.
Visual Studio – For .NET Core development.
Steps Completed in this Assignment
Step 1: Version Control & Project Setup
Created a GitHub repository for the project and added a README.md with detailed project information.
Cloned the repository to a local machine and initialized Git.
Created a .gitignore file to exclude unnecessary files like build artifacts and logs.
Step 2: Database Integration
Installed MS SQL Server and attached the AdventureWorks sample database.
Set up a connection string in the appsettings.json file of the ASP.NET Core Web API project to connect to the database.
Implemented CRUD operations using Entity Framework Core to interact with the AdventureWorks database.
Step 3: Microservices Architecture with Docker
Dockerized the ASP.NET Core Web API by creating a Dockerfile for the API project.
Set up Docker Compose to manage multi-container applications, linking the API container and SQL Server container together.
Built and ran the containers using docker-compose.
Step 4: CI/CD Pipeline with Jenkins
Installed Jenkins and configured the necessary plugins for integration with GitHub.
Created a Jenkinsfile to automate the build, Docker build, and deployment stages.
Set up GitHub Webhooks to trigger Jenkins builds upon new commits.
Architecture Overview
The project follows a microservices architecture where:

The ASP.NET Core Web API serves as a backend for interacting with the database.
The MS SQL Server is used to store data.
Both the API and SQL Server are containerized using Docker for better scalability and environment consistency.
CI/CD Pipeline
Jenkins Pipeline Overview
The Jenkins pipeline consists of the following stages:

Build: Compile the .NET Core application using dotnet build.
Docker Build: Build the Docker images for the API and database.
Deploy to Staging: Deploy the containers to a staging environment using docker-compose.
How to Run the Project Locally
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/AdventureWorksMicroservices.git
cd AdventureWorksMicroservices
Run Docker Compose:

Make sure Docker is installed and running on your machine.
Use the following command to build and run the containers:
bash
Copy code
docker-compose up --build
This will start the API on port 8080 and SQL Server on port 1433.
API Documentation
The API can be accessed at http://localhost:8080/. The API endpoints include CRUD operations for the AdventureWorks database.

Example Endpoints:
GET /api/products – Get a list of all products.
POST /api/products – Create a new product.
PUT /api/products/{id} – Update an existing product.
DELETE /api/products/{id} – Delete a product.
You can interact with the API using Swagger or Postman.

Future Improvements
API Versioning: Implement versioning in the API to ensure backward compatibility.
Production Deployment: Set up the pipeline to deploy to a production environment (e.g., AWS, Azure).
Monitoring & Logging: Add tools like Prometheus and Grafana for monitoring and centralized logging.
License
This project is licensed under the MIT License.

