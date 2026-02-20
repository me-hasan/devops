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

## Tech Stack

- **Backend**: Python + Django
- **Frontend**: Django Templates + Tailwind CSS (via CDN)
- **Database**: SQLite (for local development)
- **JavaScript**: Minimal JS for enhanced UX (toggle completion)

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone or navigate to the project directory:**
   ```bash
   cd /path/to/todo_project
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

7. **Open your browser and navigate to:**
   ```
   http://127.0.0.1:8000/
   ```
   ![Git Setup](./Screenshot%202026-02-20%20at%206.29.56 AM.png)


## Project Structure

```
todo_project/
├── manage.py
├── requirements.txt
├── README.md
├── db.sqlite3          # SQLite database (created after migrate)
├── todo_project/       # Project settings
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── tasks/              # Tasks app
│   ├── __init__.py
│   ├── models.py       # Task model
│   ├── views.py        # CRUD views
│   ├── forms.py        # Task form
│   ├── urls.py         # App URLs
│   ├── admin.py
│   ├── tests.py        # Unit tests
│   └── migrations/     # Database migrations
└── templates/          # HTML templates
    ├── base.html
    └── tasks/
        ├── task_list.html
        ├── task_form.html
        └── task_confirm_delete.html
```

## Usage

### Creating a Task

1. Click the "+ New Task" button on the task list page
2. Fill in the task title (required)
3. Optionally add a description and due date
4. Click "Create Task"

### Managing Tasks

- **View Tasks**: All tasks are displayed on the home page
- **Filter Tasks**: Use the tabs (All/Active/Completed) to filter tasks
- **Toggle Completion**: Click "Mark Complete" or "Mark Active" to toggle task status
- **Edit Task**: Click the "Edit" button to modify a task
- **Delete Task**: Click the "Delete" button and confirm deletion

### Admin Interface

Access the Django admin panel at `http://127.0.0.1:8000/admin/` (requires superuser account).
![Git Setup](./Screenshot%202026-02-20%20at%206.37.49 AM.png)


## Running Tests

```bash
python manage.py test
```

## Development

### Making Changes

1. **Model Changes**: After modifying `models.py`, run:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

2. **Static Files**: This project uses Tailwind CSS via CDN, so no static file collection is needed for development.

## License

This project is open source and available for educational purposes.


## Heroku live project host. 
