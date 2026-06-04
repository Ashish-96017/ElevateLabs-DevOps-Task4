# ElevateLabs DevOps Internship – Task 4

## Git Version Control with Branching Strategy and CI/CD

### Project Overview

This project demonstrates Git version control best practices using a Flask-based CI/CD application.

The objective of this task is to understand Git workflows used in real software development environments, including branch management, pull requests, commits, tagging, and integration with a CI/CD pipeline.

---

## Technologies Used

* Git
* GitHub
* Python 3.11
* Flask
* Docker
* Jenkins
* Pytest

---

## Branching Strategy

```text
main
 └── dev
      └── feature/add-project-files
```

| Branch                    | Purpose                        |
| ------------------------- | ------------------------------ |
| main                      | Production-ready code          |
| dev                       | Integration and testing branch |
| feature/add-project-files | Feature development branch     |

---

## Git Workflow Implemented

### Step 1

Created repository and initialized Git.

### Step 2

Created development branch:

```bash
git checkout -b dev
```

### Step 3

Created feature branch:

```bash
git checkout -b feature/add-project-files
```

### Step 4

Added project files and committed changes.

### Step 5

Created Pull Request:

```text
feature/add-project-files → dev
```

### Step 6

Merged development branch into main:

```text
dev → main
```

### Step 7

Created release tag:

```bash
git tag -a v1.0 -m "Release v1.0"
git push origin v1.0
```

---

## Project Structure

```text
ElevateLabs-DevOps-Task4/
│
├── app.py
├── test_app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
├── .gitignore
└── README.md
```

---

## Application Endpoints

### Home Endpoint

```http
GET /
```

Response:

```json
{
  "message": "Hello from Jenkins CI/CD Pipeline!",
  "status": "running",
  "version": "1.0.0"
}
```

### Health Endpoint

```http
GET /health
```

Response:

```json
{
  "status": "healthy"
}
```

---

## CI/CD Pipeline Workflow

```text
Developer
    ↓
GitHub Repository
    ↓
Jenkins Pipeline
    ↓
Build Docker Image
    ↓
Run Automated Tests
    ↓
Deploy Container
    ↓
Health Check
    ↓
Successful Deployment
```

---

## Jenkins Pipeline Stages

### Checkout

Pull latest source code from GitHub.

### Build

Build Docker image using Dockerfile.

### Test

Run automated Pytest test cases.

### Deploy

Deploy Docker container.

### Health Check

Verify application availability using the health endpoint.

---

## Running the Project Locally

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Application

```bash
python app.py
```

### Run Tests

```bash
pytest test_app.py -v
```

### Build Docker Image

```bash
docker build -t flask-cicd-app .
```

### Run Docker Container

```bash
docker run -d -p 5000:5000 --name flask-app flask-cicd-app
```

---

## Git Commands Used

```bash
git init

git checkout -b dev

git checkout -b feature/add-project-files

git add .

git commit -m "Add project files"

git push origin feature/add-project-files

git checkout dev

git merge feature/add-project-files

git checkout main

git merge dev

git tag -a v1.0 -m "Release v1.0"

git push origin v1.0
```

---

## Git Interview Questions and Answers

### What is Git?

Git is a distributed version control system used to track source code changes and collaborate with other developers.

### What is a Pull Request?

A Pull Request is a request to merge changes from one branch into another while allowing code review and discussion.

### Merge vs Rebase?

* Merge preserves branch history.
* Rebase creates a linear commit history.

### What are Git Tags?

Tags are references to specific commits, typically used to mark software releases.

### What is Git Stash?

Git Stash temporarily stores uncommitted changes so developers can switch branches safely.

### What is .gitignore?

A configuration file used to exclude files and directories from Git tracking.

### How are Merge Conflicts Resolved?

By manually editing conflicting files, removing conflict markers, and committing the resolved changes.

### Why Use Branching?

Branching allows independent development without affecting stable production code.

---

## Release Information

### Version 1.0

Initial release containing:

* Flask application
* Docker containerization
* Jenkins CI/CD pipeline
* Automated testing
* Git branching workflow

---

## Learning Outcomes

Through this project, I learned:

* Git branching strategies
* Feature branch workflow
* Pull Requests and code reviews
* Merge and release management
* Git tagging
* Version control best practices
* CI/CD integration with Git
* Collaborative development workflows

---

## Author

**Ashish Vijaybhai Shakoriya**

DevOps Internship – Elevate Labs

Task 4: Git Version Control with Branching and CI/CD
