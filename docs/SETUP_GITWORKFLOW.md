# Preliminaries — Hands-On Machine Learning

## Purpose
This section serves as a fixed reference for the project. It includes:
- initial setup
- essential Git commands
- repository structure
- workflow to follow for each chapter
- practical tips for notebooks and machine learning

---

## 1. What has been done so far

### Project creation
```bash
mkdir hands-on-ml        # create project folder
cd hands-on-ml           # enter the project folder
```

### Git initialization
```bash
git init                 # initialize Git repository and create hidden .git folder
```

### Initial files and folders
```bash
touch README.md          # create project overview file
touch .gitignore         # create ignore rules file
mkdir notebooks src data # create main project folders
```

### .gitignore
The `.gitignore` file contains files and folders that Git should ignore.

Example:
```bash
__pycache__/
*.py[cod]
.venv/
.ipynb_checkpoints/
.DS_Store
.env
```

### First Git commit
```bash
git status                             # check repository status
git add .                              # stage all files
git commit -m "Initial project setup"  # create first commit
```

### Connect to GitHub
```bash
git remote add origin URL_OF_REPO # connect local repository to GitHub
git push -u origin main           # push main branch and set upstream
```

---

## 2. Virtual environment

### Create the virtual environment
```bash
python3 -m venv .venv # create local virtual environment in .venv
```

### Activate the virtual environment
```bash
source .venv/bin/activate # activate the virtual environment
```

### Install core libraries
```bash
pip install jupyter ipykernel numpy pandas matplotlib scikit-learn
```

### Verify active Python
```bash
which python # check that Python comes from .venv
```

### Register Jupyter kernel
```bash
python -m ipykernel install --user --name hands-on-ml --display-name "Python (hands-on-ml)"
```

---

## 3. Repository structure

```text
hands-on-ml/
│
├── docs/
│   └── SETUP_GIT_WORKFLOW.md
│
├── notebooks/
│   ├── 00_setup/
│   ├── chapter_01/
│   ├── chapter_02/
│   └── ...
│
├── src/
├── data/
├── README.md
└── .gitignore
```

### Meaning of each folder
- `notebooks/` = notebooks for experiments, practice, and chapter notes
- `00_preliminaries/` = setup, environment checks, and reference material
- `src/` = reusable and clean Python code
- `data/` = datasets
- `README.md` = project overview

---

## 4. General workflow

For each chapter:
1. create chapter folder
2. create notebook
3. add title and objective
4. follow the book
5. make small and clear commits
6. move reusable code to `src/`

---

## 5. Creating a new chapter

```bash
mkdir -p notebooks/chapter_02                 # create chapter folder
touch notebooks/chapter_02/chapter_02.ipynb  # create notebook

git status                                    # check status
git add notebooks/chapter_02/chapter_02.ipynb
git commit -m "Add chapter 2 notebook"
git push
```
---

## 6. Standard workflow

```bash
git status
git add specific_file
git commit -m "Clear message"
git push
```
---

## 7. Useful Git commands

```bash
git status                         # show current state of the repository (modified, staged, untracked files)
git add .                          # stage all changes in the project
git add notebooks/chapter_01/chapter_01.ipynb  # stage only a specific file
git commit -m "Message"            # create a snapshot of staged changes with a message
git log --oneline                  # show commit history in compact format (one line per commit)
git push                           # upload local commits to the remote repository (GitHub)
git pull                           # fetch and merge updates from the remote repository
git remote -v                      # show configured remote repositories and their URLs
```
---

## 8. General advice

### Git
- make small commits
- push frequently
- always check `git status`
- prefer adding specific files

### Notebooks
- use notebooks for exploration
- avoid very large notebooks
- add Markdown explanations
- save frequently

### Code
- move reusable logic to `src/`
- avoid keeping everything in notebooks

---

## 9. Start-of-session checklist

```bash
cd ~/Projects/hands-on-ml
source .venv/bin/activate
git status
```

Then:
- open VS Code
- open the notebook
- check kernel
- start working

---

## 10. End-of-session checklist

```bash
git status
git add file_or_notebook
git commit -m "Clear message"
git push
```
---

## 12. Final rule

- notebooks = experimentation
- src = clean and reusable code
- git = project history
- github = portfolio
