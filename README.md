# GitHub Commands & Shortcuts Reference

A comprehensive guide to Git commands and GitHub shortcuts for efficient development workflow.

## 📋 Project Description

This repository serves as a complete reference guide for developers who want to master Git version control and GitHub workflows. Whether you're a beginner learning your first Git commands or an experienced developer looking for a quick reference, this guide has everything you need.

### 🎯 Purpose

The main goal of this project is to provide a centralized, well-organized resource that covers:
- **Essential Git commands** for daily development tasks
- **GitHub-specific features** and shortcuts
- **Best practices** for version control workflows
- **Advanced techniques** for complex scenarios
- **Quick reference** for both command-line and web interface operations

### 🚀 Who This Is For

- **New developers** learning Git and GitHub for the first time
- **Experienced developers** who need a quick command reference
- **Development teams** establishing consistent Git workflows
- **Students** studying version control systems
- **Anyone** who works with Git repositories regularly

### ✨ Features

- **Comprehensive coverage** of Git commands from basic to advanced
- **GitHub CLI integration** for streamlined workflows
- **Web interface shortcuts** for faster GitHub navigation
- **Real-world examples** and common use cases
- **Best practices** and workflow recommendations
- **Easy-to-navigate structure** with clear categorization
- **Copy-paste ready** commands with explanations

### 📚 What You'll Learn

By using this reference guide, you'll be able to:
- Navigate Git repositories with confidence
- Manage branches and merges effectively
- Handle remote repositories and collaboration
- Resolve conflicts and undo changes safely
- Use GitHub's web interface efficiently
- Implement proper Git workflows in your projects
- Troubleshoot common Git issues

### 🔧 How to Use This Guide

This reference is designed for quick lookups and learning:
1. **Browse by category** using the table of contents
2. **Search for specific commands** using Ctrl+F
3. **Copy commands directly** into your terminal
4. **Follow the workflows** for common development scenarios
5. **Bookmark** for quick access during development

### 🎨 Why This Guide Exists

While Git documentation is comprehensive, it can be overwhelming for daily use. This guide distills the most important and frequently used commands into an accessible format, making it easier to:
- Find the right command quickly
- Understand common workflows
- Avoid dangerous operations
- Learn best practices organically

## Table of Contents
- [Basic Git Commands](#basic-git-commands)
- [Branch Management](#branch-management)
- [Remote Repository Operations](#remote-repository-operations)
- [Staging and Committing](#staging-and-committing)
- [Viewing History and Changes](#viewing-history-and-changes)
- [Undoing Changes](#undoing-changes)
- [GitHub CLI Commands](#github-cli-commands)
- [GitHub Web Interface Shortcuts](#github-web-interface-shortcuts)
- [Git Configuration](#git-configuration)
- [Advanced Git Commands](#advanced-git-commands)

## Basic Git Commands

### Repository Initialization
```bash
git init                    # Initialize a new Git repository
git clone <url>            # Clone a repository from remote
git clone <url> <folder>   # Clone into specific folder
```

### Repository Status
```bash
git status                 # Show working tree status
git status -s             # Short status format
git status --porcelain    # Machine-readable status
```

## Branch Management

### Creating and Switching Branches
```bash
git branch                    # List all branches
git branch <branch-name>      # Create new branch
git checkout <branch-name>    # Switch to branch
git checkout -b <branch-name> # Create and switch to new branch
git switch <branch-name>      # Switch to branch (newer command)
git switch -c <branch-name>   # Create and switch to new branch
```

### Branch Operations
```bash
git branch -d <branch-name>   # Delete branch (safe)
git branch -D <branch-name>   # Force delete branch
git branch -m <old> <new>     # Rename branch
git branch -r                 # List remote branches
git branch -a                 # List all branches (local + remote)
```

### Merging
```bash
git merge <branch-name>       # Merge branch into current branch
git merge --no-ff <branch>    # Merge without fast-forward
git merge --squash <branch>   # Squash merge
```

## Remote Repository Operations

### Remote Management
```bash
git remote                    # List remotes
git remote -v                # List remotes with URLs
git remote add <name> <url>   # Add remote repository
git remote remove <name>      # Remove remote
git remote rename <old> <new> # Rename remote
```

### Fetching and Pulling
```bash
git fetch                     # Fetch from all remotes
git fetch <remote>           # Fetch from specific remote
git pull                     # Fetch and merge from remote
git pull --rebase           # Fetch and rebase instead of merge
git pull origin <branch>    # Pull specific branch
```

### Pushing
```bash
git push                     # Push to default remote/branch
git push origin <branch>     # Push to specific branch
git push -u origin <branch>  # Push and set upstream
git push --force            # Force push (dangerous!)
git push --force-with-lease # Safer force push
git push --tags             # Push tags
```

## Staging and Committing

### Staging Files
```bash
git add <file>              # Stage specific file
git add .                   # Stage all changes in current directory
git add -A                  # Stage all changes in repository
git add -u                  # Stage modified and deleted files
git add -p                  # Interactive staging (patch mode)
```

### Committing
```bash
git commit                  # Commit with editor for message
git commit -m "message"     # Commit with inline message
git commit -am "message"    # Stage and commit modified files
git commit --amend          # Amend last commit
git commit --amend -m "msg" # Amend with new message
```

## Viewing History and Changes

### Log and History
```bash
git log                     # Show commit history
git log --oneline          # Compact log format
git log --graph            # Show branch graph
git log --stat             # Show file statistics
git log -p                 # Show patch/diff for each commit
git log --since="2 weeks"  # Show commits from last 2 weeks
git log --author="name"    # Show commits by author
```

### Viewing Changes
```bash
git diff                   # Show unstaged changes
git diff --staged         # Show staged changes
git diff HEAD             # Show all changes since last commit
git diff <branch1> <branch2> # Compare branches
git show <commit-hash>    # Show specific commit details
```

## Undoing Changes

### Unstaging and Reverting
```bash
git reset <file>           # Unstage file
git reset --soft HEAD~1   # Undo last commit (keep changes staged)
git reset --mixed HEAD~1  # Undo last commit (keep changes unstaged)
git reset --hard HEAD~1   # Undo last commit (discard changes)
git checkout -- <file>    # Discard unstaged changes in file
git restore <file>         # Restore file (newer command)
git restore --staged <file> # Unstage file (newer command)
```

### Reverting Commits
```bash
git revert <commit-hash>   # Create new commit that undoes changes
git revert HEAD           # Revert last commit
git revert --no-commit <hash> # Revert without committing
```

## GitHub CLI Commands

### Installation
```bash
# Install GitHub CLI
# macOS: brew install gh
# Windows: winget install GitHub.cli
# Linux: Check GitHub CLI documentation
```

### Authentication
```bash
gh auth login             # Login to GitHub account
gh auth status           # Check authentication status
gh auth logout           # Logout from GitHub
```

### Repository Operations
```bash
gh repo create           # Create new repository
gh repo clone <repo>     # Clone repository
gh repo fork <repo>      # Fork repository
gh repo view             # View repository details
gh repo delete          # Delete repository
```

### Issues and Pull Requests
```bash
gh issue create          # Create new issue
gh issue list           # List issues
gh issue view <number>  # View specific issue
gh issue close <number> # Close issue

gh pr create            # Create pull request
gh pr list             # List pull requests
gh pr view <number>    # View pull request
gh pr merge <number>   # Merge pull request
gh pr checkout <number> # Checkout PR locally
```

## GitHub Web Interface Shortcuts

### Navigation
- `g` + `c` → Go to Code tab
- `g` + `i` → Go to Issues tab
- `g` + `p` → Go to Pull requests tab
- `g` + `a` → Go to Actions tab
- `g` + `w` → Go to Wiki tab

### General Shortcuts
- `s` or `/` → Focus search bar
- `?` → Show keyboard shortcuts help
- `Ctrl/Cmd + K` → Command palette
- `t` → File finder
- `w` → Switch branch or tag
- `y` → Get permalink to file

### Code Navigation
- `b` → Open blame view
- `l` → Jump to line
- `Ctrl/Cmd + F` → Find in file
- `Ctrl/Cmd + Shift + F` → Find in repository

### Issues and Pull Requests
- `c` → Create issue
- `Ctrl/Cmd + Enter` → Submit comment
- `r` → Quote reply
- `e` → Edit comment

## Git Configuration

### User Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --global init.defaultBranch main
```

### Useful Configuration
```bash
git config --global core.editor "code --wait"  # Use VS Code as editor
git config --global merge.tool vimdiff         # Set merge tool
git config --global alias.st status           # Create alias
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
```

### View Configuration
```bash
git config --list          # Show all configuration
git config user.name       # Show specific config value
git config --global --edit # Edit global config file
```

## Advanced Git Commands

### Stashing
```bash
git stash                  # Stash current changes
git stash save "message"   # Stash with message
git stash list            # List all stashes
git stash pop             # Apply and remove latest stash
git stash apply           # Apply latest stash (keep in stash)
git stash drop            # Delete latest stash
git stash clear           # Delete all stashes
```

### Rebasing
```bash
git rebase <branch>        # Rebase current branch onto another
git rebase -i HEAD~3      # Interactive rebase (last 3 commits)
git rebase --continue     # Continue rebase after resolving conflicts
git rebase --abort        # Abort rebase operation
```

### Tagging
```bash
git tag                   # List all tags
git tag <tag-name>        # Create lightweight tag
git tag -a <tag> -m "msg" # Create annotated tag
git tag -d <tag-name>     # Delete tag locally
git push origin --tags    # Push all tags
git push origin <tag>     # Push specific tag
```

### Cherry-picking
```bash
git cherry-pick <commit-hash>  # Apply specific commit to current branch
git cherry-pick --no-commit <hash> # Cherry-pick without committing
```

## Useful Git Aliases

Add these to your `.gitconfig` file:
```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
git config --global alias.s "status -s"
git config --global alias.unstage "reset HEAD --"
git config --global alias.last "log -1 HEAD"
git config --global alias.visual "!gitk"
```

## Best Practices

### Commit Messages
- Use present tense ("Add feature" not "Added feature")
- Keep first line under 50 characters
- Use imperative mood
- Add detailed description after blank line if needed

### Workflow Tips
- Pull before pushing
- Use branches for features
- Write meaningful commit messages
- Review changes before committing
- Use `.gitignore` to exclude unnecessary files
- Keep commits small and focused

## Common Workflows

### Feature Branch Workflow
```bash
git checkout main
git pull origin main
git checkout -b feature/new-feature
# Make changes and commits
git push -u origin feature/new-feature
# Create pull request on GitHub
# After merge, delete branch
git checkout main
git pull origin main
git branch -d feature/new-feature
```

### Hotfix Workflow
```bash
git checkout main
git pull origin main
git checkout -b hotfix/urgent-fix
# Make quick fix and commit
git push -u origin hotfix/urgent-fix
# Create pull request for immediate merge
```

---

🙏 Thank You
To the Community
Thank you to all developers who use this reference guide in their daily work. Your feedback and suggestions help make this resource more valuable for everyone in the development community.

To the Git & GitHub Teams
Appreciation to the creators and maintainers of Git and GitHub for building the tools that make modern software development collaboration possible.

Support This Project
If this reference guide has been helpful to you:

⭐ Star this repository to show your support
🍴 Fork it to create your own customized version
📢 Share it with fellow developers who might find it useful
💡 Contribute by suggesting improvements or reporting issues

Stay Connected

Found this helpful? Consider following for more developer resources
Have questions? Feel free to open an issue for discussion
Want to collaborate? Check out the contributing guidelines above

Happy coding! 🚀

"The best way to learn Git is to use it every day. This guide is here to help you along the journey."
