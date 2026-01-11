# Git Lab 2 - Cloud Computing

**Student:** Arshia Jadoon  
**Registration:** BSE-2023-014  
**Repository:** arshiajadoon/lab-2

## Overview

Hands-on Git version control lab covering repository setup, branching strategies, pull requests, and team collaboration workflows.

---

## Tasks Completed

### Task 1: Private Repository Creation
✅ Created private GitHub repository  
✅ Configured repository settings  
✅ Set up basic repository structure  

### Task 2: SSH Authentication
✅ Generated SSH key pair with `ssh-keygen`  
✅ Added public key to GitHub  
✅ Cloned repository using SSH  
```bash
ssh-keygen -t rsa -b 4096
git clone git@github.com:arshiajadoon/lab-2.git
```

### Task 3: Git Configuration
✅ Set user name and email  
✅ Verified configuration  
```bash
git config --global user.name "Arshia Jadoon"
git config --global user.email "email@example.com"
git config --list
```

### Task 4: Repository Exploration
✅ Examined `.git` folder structure  
✅ Understood Git internal architecture  
✅ Reviewed configuration files  

### Task 5: Initialize & First Commit
✅ Deleted existing `.git` folder  
✅ Re-initialized repository  
✅ Created first commit  
✅ Pushed to remote  
```bash
rm -rf .git
git init
git add .
git commit -m "Initial commit"
git push origin main
```

### Task 6: Basic Git Workflow
✅ Made changes to files  
✅ Checked status  
✅ Committed changes with meaningful messages  
```bash
git status
git add <files>
git commit -m "Add notes"
```

### Task 7: Bugfix Branch
✅ Created `bugfix` branch  
✅ Made fixes on separate branch  
✅ Verified branch in GUI and locally  
```bash
git checkout -b bugfix
git branch
```

### Task 8: Feature Branch (Database)
✅ Created `feature-db` branch  
✅ Implemented database changes  
✅ Committed feature work  

### Task 9: Feature Development & Merge
✅ Created new feature branch  
✅ Made commits on feature branch  
✅ Merged feature to main  
✅ Pushed all branches  
```bash
git checkout -b feature-login
git commit -m "Add login feature"
git checkout main
git merge feature-login
git push --all
```

### Task 10: Pull Request Workflow
✅ Created pull request from branch  
✅ Reviewed PR in GitHub interface  
✅ Merged PR via GitHub  
✅ Deleted merged branch  

### Task 11: Final Branch Integration
✅ Merged all feature branches to main  
✅ Updated branch strategy documentation  
✅ Documented all merges  

### Task 12: Team Collaboration (Bonus)
✅ Created PR with detailed description  
✅ Assigned reviewer  
✅ **Reviewer actions:**
  - Approved PR
  - Requested changes
  - Added review comments
✅ **Author actions:**
  - Updated PR with new commits
  - Addressed review feedback
✅ Merged approved PR  
✅ Deleted feature branch after merge  
✅ Created `REVIEW_NOTES.md` documentation  

### Task 13: Branch Cleanup
✅ Deleted merged local branches  
✅ Deleted merged remote branches  
✅ Verified cleanup  
```bash
git branch -d feature-name
git push origin --delete feature-name
```

---

## Key Git Commands

### Basic Operations
```bash
git init                    # Initialize repository
git status                  # Check working directory status
git add <file>             # Stage changes
git commit -m "message"    # Commit staged changes
git push origin <branch>   # Push to remote
git pull origin <branch>   # Pull from remote
```

### Branching
```bash
git branch                 # List branches
git branch <name>          # Create branch
git checkout <name>        # Switch branch
git checkout -b <name>     # Create and switch
git merge <branch>         # Merge branch
git branch -d <name>       # Delete local branch
```

### Remote Operations
```bash
git remote -v              # Show remotes
git push --all             # Push all branches
git push origin --delete <branch>  # Delete remote branch
git fetch --prune          # Remove stale references
```

---

## Branch Strategy

### Main Branch (`main`)
- Production-ready code
- Protected branch
- Merge only via pull requests

### Feature Branches
- Format: `feature-<name>`
- Created from `main`
- One feature per branch
- Delete after merge

### Bugfix Branches
- Format: `bugfix-<issue>`
- Quick fixes
- Merge to `main` after testing

### Best Practices
✅ Descriptive branch names  
✅ Small, focused commits  
✅ Regular pushes to remote  
✅ Pull before pushing  
✅ Delete merged branches  
✅ Use pull requests for code review  

---

## Pull Request Process

### 1. Create PR
- Navigate to repository on GitHub
- Click "Pull requests" → "New pull request"
- Select base and compare branches
- Add title and description
- Assign reviewers

### 2. Review
- Reviewers examine code changes
- Add comments and suggestions
- Request changes if needed
- Approve when satisfied

### 3. Address Feedback
- Make requested changes
- Commit and push updates
- PR automatically updates

### 4. Merge
- Ensure all checks pass
- Click "Merge pull request"
- Confirm merge
- Delete branch after merge

---

## Common Workflows

### Starting New Feature
```bash
git checkout main
git pull origin main
git checkout -b feature-new-feature
# Make changes
git add .
git commit -m "Add new feature"
git push origin feature-new-feature
# Create PR on GitHub
```

### Fixing a Bug
```bash
git checkout main
git pull origin main
git checkout -b bugfix-issue-123
# Fix bug
git commit -am "Fix issue #123"
git push origin bugfix-issue-123
# Create PR
```

### Syncing with Remote
```bash
git checkout main
git pull origin main
git checkout feature-branch
git merge main  # or git rebase main
```

---

## Troubleshooting

**Merge Conflicts:**
```bash
# After conflict occurs
git status                 # See conflicted files
# Manually resolve conflicts in files
git add <resolved-files>
git commit -m "Resolve merge conflicts"
```

**Undo Last Commit (not pushed):**
```bash
git reset --soft HEAD~1    # Keep changes
git reset --hard HEAD~1    # Discard changes
```

**Update Commit Message:**
```bash
git commit --amend -m "New message"
```

**Recover Deleted Branch:**
```bash
git reflog                 # Find commit hash
git checkout -b branch-name <hash>
```

---

## Repository Structure

```
lab-2/
├── .git/                  # Git internal files
├── .gitignore            # Ignored files
├── README.md             # This file
├── REVIEW_NOTES.md       # PR review documentation
└── src/                  # Source code
```

---

## Learning Outcomes

✅ Create and manage Git repositories  
✅ Configure Git identity and SSH  
✅ Use branching for parallel development  
✅ Merge branches and resolve conflicts  
✅ Create and review pull requests  
✅ Collaborate using GitHub workflows  
✅ Clean up merged branches  
✅ Follow Git best practices  

---

## Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Pro Git Book](https://git-scm.com/book/en/v2)

---

## Author

**Arshia Jadoon**  
BSE-2023-014  
Semester VA

---

*Lab 2 - Cloud Computing Course*
