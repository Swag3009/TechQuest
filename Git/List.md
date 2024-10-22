# Git Topic List to Learn
## 1. Git Basics (Revisit Concepts)
  - [ ] What is version control?
    - [ ] Definition and importance
    - [ ] Difference between local and remote repositories
  - [ ] Git vs. other version control systems
    - [ ] Git advantages
    - [ ] Centralized vs. distributed version control
  - [ ] Git configurations (name, email, aliases)
    - [ ] Setting up username and email
    - [ ] Configuring default text editor
    - [ ] Creating aliases for commands
  - [ ] Working with repositories
    - [ ] Creating a new repository (`git init`)
    - [ ] Cloning an existing repo=sitory (`git clone`)
    - [ ] Checking the status of your repository (`git status`)

## 2. Core Git Commands
  - [ ] Adding files to the staging area (`git add`)
    - [ ] Adding individual files
    - [ ] Adding all changes at once
  - [ ] Committing changes (`git commit`)
    - [ ] Writing good commit messages
    - [ ] Making atomic commits (one change per commit)
  - [ ] Viewing the history of commits (`git log`)
    - [ ] Viewing a concise commit history (`git log --oneline`)
    - [ ] Viewing detailed commit information
  - [ ] Comparing changes (`git diff`)
    - [ ] Comparing working directory to staged area
    - [ ] Comparing staged area to last commit
  - [ ] Working with `.gitignore`
    - [ ] Creating a `.gitignore` file
    - [ ] Common patterns to ignore

## 3. Branching and Merging
  - [ ] What is branching in Git?
    - [ ] Concept of branches
    - [ ] Purpose of branches in development
  - [ ] Creating and managing branches
    - [ ] Creating a new branch (`git branch`)
    - [ ] Switching branches (`git checkout` or `git switch`)
  - [ ] Merging branches
    - [ ] Merging feature branches into main (`git merge`)
    - [ ] Fast-forward merge vs. three-way merge
  - [ ] Handling merge conflicts
    - [ ] Understanding a merge conflict
    - [ ] Resolving conflicts manually
    - [ ] Aborting a merge (`git merge --abort`)

## 4. Git Rebase and Stashing
  - [ ] Understanding rebase vs. merge
    - [ ] When to use rebase instead of merge
  - [ ] Rebasing branches (`git rebase`)
    - [ ] Basic rebase
    - [ ] Interactive rebase (`git rebase -i`)
  - [ ] Stashing changes (`git stash`)
    - [ ] Stashing changes and applying later
    - [ ] Viewing stash list and applying stashes
    - [ ] Dropping stashes

## 5. Undoing in Git
  - [ ] Undoing changes in the working directory
    - [ ] Discarding changes (`git checkout`)
    - [ ] Resetting to a previous commit (`git reset`)
  - [ ] Undoing a commit with `git revert`
    - [ ] Difference between `revert` and `reset`
  - [ ] Working with the reflog (`git reflog`)
    - [ ] Understanding reflog and recovering from mistakes

## 6. Collaboration with GitHub
  - [ ] Setting up a GitHub repository
    - [ ] Creating a repository on GitHub
    - [ ] Linking a local repo to GitHub (`git remote add origin`)
  - [ ] Pushing changes to GitHub (`git push`)
    - [ ] Pushing to a remote branch
  - [ ] Pulling changes from GitHub (`git pull`)
    - [ ] Fetching and integrating changes
  - [ ] Forking repositories and submitting pull requests
    - [ ] Forking an open-source project
    - [ ] Creating a pull request (PR)
  - [ ] Collaboration workflows
    - [ ] Using feature branches for PRs
    - [ ] Keeping branches in sync (`git fetch`)

## 7. Advanced GitHub Features
  - [ ] Managing issues on GitHub
    - [ ] Creating and assigning issues
  - [ ] Setting up GitHub Actions for CI/CD
    - [ ] Understanding GitHub Actions basics
    - [ ] Creating a simple CI pipeline
  - [ ] Working with GitHub Pages
    - [ ] Hosting a site with GitHub Pages
  - [ ] Using GitHub with SSH
    - [ ] Setting up SSH keys for authentication

## 8. Git Workflows
  - [ ] Centralized workflow
  - [ ] Feature branching workflow
    - [ ] Creating feature branches for specific tasks
  - [ ] Gitflow workflow
    - [ ] Managing releases and hotfixes
  - [ ] Forking workflow
    - [ ] Working with forks and upstream repos

## 9. Git Hooks and Automation
  - [ ] Client-side hooks
    - [ ] Setting up a `pre-commit` hook
    - [ ] Setting up a `post-commit` hook
  - [ ] Server-side hooks
    - [ ] Understanding the difference between client and server hooks
  - [ ] Automating with hooks for CI processes

## 10. Git Internals
  - [ ] Git object model (commits, trees, blobs)
  - [ ] Understanding Packfiles
    - [ ] What are packfiles?
  - [ ] Compression and garbage collection (`git gc`)
    - [ ] Running garbage collection to optimize repositories
