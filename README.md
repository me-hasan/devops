# Git & GitHub Assignment

This project is part of Module 2 Assignment for DevOps course. It covers the fundamentals of Version Control using Git & GitHub, including repository setup, branching, merging, and deployment.

## Topics Covered
- Git repository initialization
- Basic Git commands (add, commit, status)
- Branching and merging
- GitHub integration 

## Assignment Steps

### Part 1: Set Up a Local Git Repository
1. Create a new folder for the assignment
2. Initialize a new Git repository
3. Create README.md file
4. Add project description
5. Stage and commit changes 
![Git Setup](Screenshot%202026-02-20%20at%205.28.55 AM.png)


### Part 2: Connect to GitHub
1. Create a new repository on GitHub
2. Link local repository to remote
3. Push changes to GitHub
![Git Setup](./Screenshot%202026-02-20%20at%205.33.55 AM.png)

### Part 3: Create and Work on a New Branch
1. Create `feature-update` branch
2. Switch to the new branch
3. Make changes to files
4. Stage and commit on the branch 
![Git Setup](./Screenshot%202026-02-20%20at%205.58.01 AM.png)

![Git Setup](./Screenshot%202026-02-20%20at%205.59.54 AM.png)

### Part 4: Push the Branch and Create a Pull Request 
![Git Setup](./Screenshot%202026-02-20%20at%205.59.54 AM.png)

### Part 5: Merge and Update Local Repository
![Git Setup](./Screenshot%202026-02-20%20at%205.46.16 AM.png)

## How to Run the Project Locally

Follow these steps to set up and run this project on your local machine:

### Prerequisites
- Git installed on your system
- A GitHub account
- Basic knowledge of terminal/command line
- Python 3.x installed
- pip (Python package manager)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/git-assignment.git
   cd git-assignment
   ```

2. **Verify the repository**
   ```bash
   git status
   git log
   ```

3. **View all branches**
   ```bash
   git branch -a
   ```

4. **Switch between branches**
   ```bash
   git checkout main
   git checkout feature-update
   ```

5. **Create a virtual environment (recommended)**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

6. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

7. **Run migrations**
   ```bash
   python manage.py migrate
   ```

8. **Create a superuser (optional, for admin access)**
   ```bash
   python manage.py createsuperuser
   ```

9. **Run the development server**
   ```bash
   python manage.py runserver
   ```

10. **Open your browser and navigate to**
    ```
    http://127.0.0.1:8000/
    ```

### Project Structure
```
git-assignment/
├── .git/
├── .gitignore
├── README.md
├── requirements.txt
├── manage.py
├── venv/
└── screenshots/
    ├── Screenshot 2026-02-20 at 5.28.55 AM.png
    ├── Screenshot 2026-02-20 at 5.33.55 AM.png
    ├── Screenshot 2026-02-20 at 5.58.01 AM.png
    ├── Screenshot 2026-02-20 at 5.59.54 AM.png
    └── Screenshot 2026-02-20 at 5.46.16 AM.png
```

## Batch Information
**Course:** DevOps with Git & GitHub
**Batch:** Ostad_batch-09