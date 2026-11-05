# DevOps Lab 1 – CI/CD Pipeline Using Jenkins

## Overview

This project demonstrates the implementation of a basic **Continuous Integration and Continuous Deployment (CI/CD) pipeline** using Jenkins.

A simple Python application is used to demonstrate automated build, testing, and deployment stages through a Jenkins pipeline.

## Objectives

- Understand the fundamentals of CI/CD.
- Integrate a GitHub repository with Jenkins.
- Automate application build and execution.
- Create a deployment directory and copy application files.
- Verify pipeline execution through Jenkins Console Output.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.11 | Application development |
| Jenkins | CI/CD automation |
| Git & GitHub | Version control and source code management |
| Windows 11 | Jenkins execution environment |
| Ubuntu on WSL | Development environment |

## Project Structure

```text
devops-lab1/
│
├── app.py
├── Jenkinsfile
│
├── deployment/
│   └── app.py
│
└── screenshots/
    ├── 01-jenkins-success.png
    ├── 02-console-output.png
    ├── 03-github-repository.png
    ├── 04-jenkinsfile.png
    └── 05-deployment.png
```

## Application

The Python application prints a welcome message and confirms that it was built using Jenkins CI/CD.

**Application Output:**

```text
Hello Vartika!
Application built using Jenkins CI/CD.
```

## Jenkins Pipeline Stages

The pipeline is defined in the `Jenkinsfile` and consists of three stages:

### 1. Build

- Compiles `app.py` using Python's `py_compile` module.
- Checks the application for syntax errors.
- Ensures the application is ready for execution.

### 2. Test

- Executes the Python application.
- Verifies that the application runs successfully.
- Displays the application output in Jenkins Console Output.

### 3. Deploy

- Creates a directory named `deployment`.
- Copies `app.py` into the deployment directory.
- Verifies the deployment structure.

## Post Actions

Jenkins executes post-build actions after the pipeline finishes.

- Displays a success message when all stages complete successfully.
- Confirms the final pipeline execution status.

## Execution Steps

1. Create a Python application (`app.py`).
2. Configure the Jenkins pipeline using a `Jenkinsfile`.
3. Push the project files to a GitHub repository.
4. Create a Pipeline job in Jenkins.
5. Connect the Jenkins job with the GitHub repository.
6. Execute the pipeline using **Build Now**.
7. Verify Build, Test, and Deploy stages.
8. Check the Jenkins Console Output.
9. Verify that `deployment/app.py` has been created.

## Execution Result

The Jenkins pipeline executed successfully.

**Final Build Output:**

```text
Hello Vartika!
Application built using Jenkins CI/CD.

CI/CD pipeline completed successfully!
Finished: SUCCESS
```

<details>
<summary><strong>Pipeline Execution Flow</strong></summary>

```text
       GitHub Repository
               |
               v
        Jenkins Pipeline
               |
               v
          Build Stage
       (Compile Python)
               |
               v
           Test Stage
       (Run app.py)
               |
               v
          Deploy Stage
    (Copy app.py to deployment/)
               |
               v
        Pipeline Success
```

</details>

## Screenshots

Execution evidence is available in the `screenshots/` directory.

| Screenshot | Description |
|---|---|
| `01-jenkins-success.png` | Successful Jenkins build |
| `02-console-output.png` | Jenkins pipeline Console Output |
| `03-github-repository.png` | GitHub repository structure |
| `04-jenkinsfile.png` | Jenkins pipeline configuration |
| `05-deployment.png` | Deployment directory containing app.py |

## Repository

**GitHub Repository:** [DevOps Lab 1 – CI/CD Pipeline Using Jenkins](YOUR_GITHUB_REPOSITORY_LINK)

## Conclusion

This lab successfully demonstrates a basic CI/CD workflow using Jenkins and GitHub. The Python application was compiled, executed, and deployed automatically through different pipeline stages.

It provides practical experience with automation, version control, continuous integration, and deployment.

---

**Status:** Successfully Implemented and Tested

**Lab:** 01 – DevOps Foundations & Continuous Integration
