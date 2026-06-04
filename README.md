# \# ElevateLabs DevOps Internship — Task 4

# 

# \## Git Version Control with Branching \& CI/CD

# 

# \---

# 

# \## Project Overview

# 

# This project demonstrates Git best practices applied to a Flask-based CI/CD application.

# It covers branching strategy, pull requests, commit conventions, tagging, and documentation

# as part of the ElevateLabs DevOps Internship Task 4.

# 

# \---

# 

# \## Tech Stack

# 

# \- Git \& GitHub

# \- Python 3.11

# \- Flask

# \- Docker

# \- Jenkins

# \- Pytest

# 

# \---

# 

# \## Branch Strategy

# main

# └── dev

# └── feature/add-project-files

# 

# | Branch | Purpose |

# |---|---|

# | `main` | Production-ready code |

# | `dev` | Integration branch for testing |

# | `feature/add-project-files` | Feature development |

# 

# \---

# 

# \## Git Workflow Followed

# 

# 1\. Created `dev` branch from `main`

# 2\. Created `feature/add-project-files` branch from `dev`

# 3\. Made all changes on feature branch with meaningful commits

# 4\. Opened Pull Request: `feature` → `dev`

# 5\. Opened Pull Request: `dev` → `main`

# 6\. Tagged final release as `v1.0`

# 

# \---

# 

# \## Project Structure

# ElevateLabs-DevOps-Task4/

# ├── app.py               # Flask application

# ├── test\_app.py          # Pytest test cases

# ├── requirements.txt     # Python dependencies

# ├── Dockerfile           # Container configuration

# ├── Jenkinsfile          # CI/CD pipeline definition

# ├── .gitignore           # Git ignore rules

# └── README.md            # Project documentation

# 

# \---

# 

# \## Application Endpoints

# 

# | Endpoint | Method | Response |

# |---|---|---|

# | `/` | GET | `{"message": "Hello", "status": "running", "version": "1.0.0"}` |

# | `/health` | GET | `{"status": "healthy"}` |

# 

# \---

# 

# \## CI/CD Pipeline Stages

# 

# 1\. \*\*Checkout\*\* — Pull latest code from GitHub

# 2\. \*\*Build\*\* — Build Docker image

# 3\. \*\*Test\*\* — Run Pytest inside container

# 4\. \*\*Deploy\*\* — Start Docker container

# 5\. \*\*Health Check\*\* — Verify app is running

# 

# \---

# 

# \## How to Run Locally

# 

# \### Install dependencies

# ```bash

# pip install -r requirements.txt

# ```

# 

# \### Run the app

# ```bash

# python app.py

# ```

# 

# \### Run tests

# ```bash

# pytest test\_app.py -v

# ```

# 

# \### Build Docker image

# ```bash

# docker build -t flask-cicd-app .

# ```

# 

# \### Run Docker container

# ```bash

# docker run -d -p 5000:5000 --name flask-app flask-cicd-app

# ```

# 

# \---

# 

# \## Git Commands Used

# 

# ```bash

# git init

# git checkout -b dev

# git checkout -b feature/add-project-files

# git add <file>

# git commit -m "message"

# git push origin <branch>

# git tag -a v1.0 -m "Release v1.0"

# git push origin v1.0

# git merge

# ```

# 

# \---

# 

# \## Git Interview Q\&A

# 

# \*\*1. What is Git?\*\*

# Distributed version control system for tracking code changes across a team.

# 

# \*\*2. Merge vs Rebase?\*\*

# Merge preserves full history with a merge commit. Rebase rewrites history linearly onto the target branch.

# 

# \*\*3. What is a Pull Request?\*\*

# A request to merge one branch into another, allowing code review before merging.

# 

# \*\*4. How to resolve merge conflicts?\*\*

# Edit the conflicting file manually, remove conflict markers, then `git add` and `git commit`.

# 

# \*\*5. What are Git tags?\*\*

# Immutable markers on specific commits used to label release versions like `v1.0`.

# 

# \*\*6. What is Git workflow?\*\*

# A branching strategy — typically `feature → dev → main` via pull requests.

# 

# \*\*7. What is git stash?\*\*

# Temporarily saves uncommitted changes so you can switch branches without losing work.

# 

# \*\*8. What is .gitignore?\*\*

# A file that tells Git which files and folders to not track (e.g. `\_\_pycache\_\_`, `.env`).

# 

# \---

# 

# \## Release

# 

# \- \*\*v1.0\*\* — Initial release with Flask app, Docker, and Jenkins pipeline

# 

# \---

# 

# \## Author

# 

# \*\*Ashish Vijaybhai Shakoriya\*\*

# DevOps Internship — ElevateLabs

# Task 4: Git Version Control Best Practices

