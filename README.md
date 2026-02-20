# Git & GitHub Assignment - Module 2

**Topic:** Version Control using Git & GitHub – Repository Setup, Branching, Merging, and Deployment

This repository demonstrates practical skills in Git version control, GitHub collaboration workflows, and application deployment. It includes both Git workflow exercises and a fully functional Django Todo application deployed to Heroku.

---

## Table of Contents

1. [Assignment Overview](#assignment-overview)
2. [Part 1: Local Git Repository Setup](#part-1-set-up-a-local-git-repository)
3. [Part 2: GitHub Repository Connection](#part-2-connect-to-github)
4. [Part 3: Branch Creation and Development](#part-3-create-and-work-on-a-new-branch)
5. [Part 4: Branch Push and Pull Request](#part-4-push-the-branch-and-create-a-pull-request)
6. [Part 5: Merge and Local Repository Update](#part-5-merge-and-update-local-repository)
7. [Part 6: Todo Application Deployment](#part-6-clone-run-and-deploy-a-todo-application)
8. [Deliverables Checklist](#deliverables-checklist)

---

## Assignment Overview

This assignment covers:
- Git repository initialization and basic commands
- Branching and merging workflows
- GitHub integration and Pull Request management
- Application deployment to cloud platforms
- Documentation and deployment best practices

---

## Part 1: Set Up a Local Git Repository

### Objective
Initialize a local Git repository and make the first commit.

### Steps Completed

1. **Created a new folder** for the assignment
2. **Initialized Git repository:**
   ```bash
   git init
   ```
3. **Created README.md** with project description
4. **Staged and committed:**
   ```bash
   git add README.md
   git commit -m "Initial commit: Add README with project description"
   ```

![Git Setup](./Screenshot%202026-02-20%20at%205.41.50 PM.png)

---

## Part 2: Connect to GitHub

### Objective
Connect the local repository to a remote GitHub repository.

### Steps Completed

1. **Created a new public repository** on GitHub
2. **Connected local to remote:**
   ```bash
   git remote add origin <repository-url>
   ```
3. **Pushed to GitHub:**
   ```bash
   git push -u origin main
   ```

![GitHub Connection](./Screenshot%202026-02-20%20at%205.28.55 AM.png)


---

## Part 3: Create and Work on a New Branch

### Objective
Create a feature branch and make changes.

### Steps Completed

1. **Created and switched to feature branch:**
   ```bash
   git checkout -b feature-update
   ```
2. **Made changes** - Updated README.md with additional details
3. **Committed on branch:**
   ```bash
   git add README.md
   git commit -m "Update readme file"
   ```

![Branch Creation](./Screenshot%202026-02-20%20at%205.58.01 AM.png)


---

## Part 4: Push the Branch and Create a Pull Request

### Objective
Push branch to GitHub and create a Pull Request.

### Steps Completed

1. **Pushed feature branch:**
   ```bash
   git push origin feature-update
   ```
2. **Created Pull Request** on GitHub from `feature-update` → `main`
3. **Added PR description** explaining the changes



---

## Part 5: Merge and Update Local Repository

### Objective
Merge PR and synchronize local repository.

### Steps Completed

1. **Merged Pull Request** on GitHub
2. **Updated local repository:**
   ```bash
   git checkout main
   git pull origin main
   ```

![Merge Complete](./Screenshot%202026-02-20%20at%205.59.54 AM.png)

![Merge Complete](./Screenshot%202026-02-20%20at%205.39.34 AM.png)

![Merge Complete](./Screenshot%202026-02-20%20at%205.46.16 AM.png)


---

## Part 6: Clone, Run, and Deploy a Todo Application

### Repository Used
[https://github.com/latifurrafi/Ostad_batch-09.git](https://github.com/latifurrafi/Ostad_batch-09.git)

### Application Overview

A Django-based Todo application with features for creating, managing, and tracking tasks. The application uses Django Templates with Tailwind CSS for a clean, responsive interface.

### Tech Stack

| Component | Technology |
|-----------|------------|
| **Backend** | Python + Django |
| **Frontend** | Django Templates + Tailwind CSS (via CDN) |
| **Database** | SQLite (local), PostgreSQL (Heroku) |
| **Deployment** | Heroku |
| **WSGI Server** | Gunicorn |

### Live Demo

| Environment | URL |
|-------------|-----|
| **Application** | [https://python-app-git-assignment-297318ca2d68.herokuapp.com](https://python-app-git-assignment-297318ca2d68.herokuapp.com) |
| **Admin Panel** | [https://python-app-git-assignment-297318ca2d68.herokuapp.com/admin/](https://python-app-git-assignment-297318ca2d68.herokuapp.com/admin/) |

---

## How to Run the Project Locally

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/latifurrafi/Ostad_batch-09.git
   cd Ostad_batch-09
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations:**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional, for admin access):**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

7. **Open your browser:**
   ```
   http://127.0.0.1:8000/
   ```

![Local Application Running](./Screenshot%202026-02-20%20at%206.29.56 AM.png)

---

## Project Structure

```
todo_project/
├── manage.py
├── requirements.txt
├── README.md
├── Procfile                  # Heroku deployment configuration
├── db.sqlite3               # SQLite database (local)
├── todo_project/            # Project settings
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── tasks/                   # Tasks app
│   ├── __init__.py
│   ├── models.py            # Task model
│   ├── views.py             # CRUD views
│   ├── forms.py             # Task form
│   ├── urls.py              # App URLs
│   ├── admin.py
│   ├── tests.py             # Unit tests
│   └── migrations/          # Database migrations
└── templates/               # HTML templates
    ├── base.html
    └── tasks/
        ├── task_list.html
        ├── task_form.html
        └── task_confirm_delete.html
```

---

## Application Features

### Creating a Task

1. Click the **"+ New Task"** button
2. Enter task title (required)
3. Optionally add description and due date
4. Click **"Create Task"**

### Managing Tasks

| Feature | Description |
|---------|-------------|
| **View Tasks** | All tasks displayed on home page |
| **Filter Tasks** | Tabs for All / Active / Completed |
| **Toggle Completion** | Click "Mark Complete" or "Mark Active" |
| **Edit Task** | Click "Edit" to modify |
| **Delete Task** | Click "Delete" and confirm |

### Admin Interface

Access the Django admin panel for advanced task management:

```
http://127.0.0.1:8000/admin/ 
user: hasan
pass: hasan
```

![Admin Panel](./Screenshot%202026-02-20%20at%206.37.49 AM.png)

---

## Running Tests

```bash
python manage.py test
```

---

## Deployment Guide

### Heroku Deployment

The application is deployed on Heroku with the following configuration:

#### Quick One-Line Deployment

```bash
# Login to Heroku
heroku login

# Create a new Heroku app
heroku create your-app-name

# Push to Heroku
git push heroku main

# Run migrations on Heroku
heroku run python manage.py migrate

# Open the live app
heroku open
```

#### Deployment Requirements

**Procfile** (in project root):
```
web: gunicorn todo_project.wsgi
```

**requirements.txt** must include:
```
gunicorn==21.2.0
whitenoise==6.6.0
dj-database-url==2.1.0
```

**settings.py** additions for production:
```python
import dj_database_url
DATABASES['default'] = dj_database_url.config()
```

---

## Development Notes

### Making Model Changes

After modifying `models.py`, run:
```bash
python manage.py makemigrations
python manage.py migrate
```

### Static Files

This project uses Tailwind CSS via CDN, so no static file collection is needed for development.

---

## Deliverables Checklist

| Requirement | Status |
|-------------|--------|
| Public GitHub repository | ✔ |
| Proper commit history | ✔ |
| Initial commit with README.md | ✔ |
| Feature branch (feature-update) | ✔ |
| Merged Pull Request | ✔ |
| Live deployment link | ✔ |
| Updated README with deployment details | ✔ |
| Application screenshots | ✔ |

---

## Submission

### GitHub Repository
[https://github.com/mdkhayrulhasan/git-assignment](https://github.com/mdkhayrulhasan/git-assignment)

### Live Application 
#### web:
[https://python-app-git-assignment-297318ca2d68.herokuapp.com](https://python-app-git-assignment-297318ca2d68.herokuapp.com)

#### admin:
[https://python-app-git-assignment-297318ca2d68.herokuapp.com](https://python-app-git-assignment-297318ca2d68.herokuapp.com)

```
user: hasan 
pass: hasan
```

---

## License

This project is open source and available for educational purposes.

---

*Completed for Module 2 DevOps Course Assignment*