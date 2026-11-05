DevOps Lab 1 – CI/CD Pipeline Using Jenkins
Overview
This project demonstrates the implementation of a basic Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins. 
A simple Python application is used to demonstrate automated build, testing, and deployment stages.

Objectives
Understand the fundamentals of CI/CD.
Integrate a GitHub repository with Jenkins.
Automate application build and execution.
Create a deployment directory and copy application files.
Verify pipeline execution through Jenkins Console Output.
Technologies Used
Python 3.11 – Application development
Jenkins – CI/CD automation
Git & GitHub – Version control and source code management
Windows 11 – Jenkins execution environment
Ubuntu on WSL – Development environment
Project Structure
devops-lab1/
│
├── app.py
├── Jenkinsfile
├── deployment/
│   └── app.py
└── screenshots/
    ├── 01-jenkins-success.png
    ├── 02-console-output.png
    ├── 03-github-repository.png
    ├── 04-jenkinsfile.png
    └── 05-deployment.png
Application
The Python application prints a welcome message and confirms that it was built using Jenkins CI/CD.

Jenkins Pipeline Stages
The pipeline is defined in the Jenkinsfile and contains the following stages:

1. Build
Compiles app.py using Python's py_compile module.
Checks the application for syntax errors.
2. Test
Executes the Python application.
Verifies that the application runs successfully.
3. Deploy
Creates a directory named deployment.
Copies app.py into the deployment directory.
Post Actions
Displays a success message when all pipeline stages complete successfully.

Execution Result
The Jenkins pipeline executed successfully.

Application Output:

Hello Vartika!
Application built using Jenkins CI/CD.
Final Build Status:

CI/CD pipeline completed successfully!
Finished: SUCCESS
Screenshots
Execution evidence is available in the screenshots directory.

The screenshots demonstrate:

Successful Jenkins build
Pipeline Console Output
GitHub repository structure
Jenkinsfile configuration
Deployment directory containing app.py
Repository
GitHub – DevOps Lab 1

Status: Successfully implemented and tested.
