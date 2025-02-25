# Git, GitHub, Pipelines, Commands, and VS Environments

## Git Commands

```
$ git config                      # Configuring Git
$ git init                        # Create a repository (repository = project or structure of different files)
$ git clone <path>                # Creates a clone of a repository on GitHub and saves a local cloned copy
$ git add <file_name>             # Adds a file to the staging area
$ git commit                      # Commits changes to the local repository
$ git status                      # Shows the status of the repository
$ git remote                      # Manages remote repositories
$ git checkout <branch_name>      # Switches to a different branch or commit
$ git branch                      # Lists all branches
$ git push                        # Pushes committed changes to the remote repository
$ git pull                        # Pulls the latest changes from the remote repository
$ git merge <branch_name>         # Merges changes from another branch
$ git diff                        # Shows differences between commits or branches
$ git reset                       # Resets changes
$ git revert                      # Reverts a commit
$ git tag                         # Creates tags for specific commits
$ git log                         # Displays commit history
```

## Git Pipeline Stages

1. **Working Directory** (This is where changes are made)
    - `git add <file_name>` → Moves changes to the Staging Area
2. **Staging Area** (Files are prepared for commit)
    - `git commit -m "message"` → Saves changes to the local repository
3. **Local Repository** (Stores commits locally)
    - `git push` → Pushes changes to the remote repository
    - `<-- git fetch` → Retrieves updates from the remote repository
4. **Remote Repository** (Stores the latest version of the project)
    - `git checkout` → Fetches changes from the remote repository

## Common Command Line Commands

| Command | Purpose |
|---------|---------|
| `cd <directory>` | Navigate into a directory |
| `cd ..` | Navigate out of a directory |
| `mkdir <directory>` | Create a new directory |
| `rmdir <directory>` | Delete an empty directory |
| `rmdir /s <directory>` | Delete a directory and its contents |
| `git init` | Initialize an empty repository |
| `git status` | Show the current repository status |
| `git remote add origin "<git repo URL>"` | Add a remote origin |
| `dir` | Check directory structure |
| `git log --oneline` | Display commit history in a compact format |
| `git branch` | List all branches |
| `git remote remove origin` | Remove an existing remote |
| `git remote add origin <new URL>` | Add a new remote |

### Pushing an Existing Repository to GitHub

```
git remote add origin <repository URL>
git branch -M main
git push -u origin main
```

### Creating a New Repository from the Command Line

```
echo "# Project-Name" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <repository URL>
git push -u origin main
```

### Moving Local Files into a Remote Repository

1. Create a new repository on GitHub.
2. Open Git Bash and navigate to your local project folder.
3. Initialize the local directory as a Git repository:
   ```
   git init
   ```
4. Add all files to the repository:
   ```
   git add .
   ```
5. Commit the changes:
   ```
   git commit -m "First commit"
   ```
6. Add the remote repository:
   ```
   git remote add origin <repository URL>
   git remote -v
   ```
7. Push the changes:
   ```
   git push origin main
   ```

**Note:** When referencing a directory with spaces in its name, enclose it in quotes: `"<directory name>"`

## Setting Up a Virtual Environment in VS Code

### **Creating and Activating a Virtual Environment**

1. Navigate to your project folder and run:
   ```
   python -m venv myenv
   ```
2. Activate the virtual environment:
   ```
   myenv\Scripts\activate  # Windows
   source myenv/bin/activate  # macOS/Linux
   ```

### **Choosing a Specific Python Version**

- **Python 3.13:**
  ```
  python3.13 -m venv myenv
  ```
- **Python 3.12:**
  ```
  python3.12 -m venv myenv
  ```
- **Python 3.10:**
  ```
  python3.10 -m venv myenv
  ```

### **Installing Packages in the Virtual Environment**

- Install a package (e.g., `nltk`):
  ```
  pip install nltk
  ```

### **Deactivating the Virtual Environment**

- To deactivate the environment when done:
  ```
  deactivate
  ```

