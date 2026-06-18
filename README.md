# React + Vite + Tailwind CSS Setup Guide

This guide explains how to create a React project using Vite, install Tailwind CSS, and use common Git/GitHub commands with their purpose and usage.

---

# 1. Create a React Project with Vite

## Create a New React Application

### Command

```bash
npm create vite@latest my-app -- --template react
```

### What it does

Creates a new React project using Vite.

### Why we use it

Vite provides a fast development environment with instant hot reloading and optimized builds.

---

## Navigate to the Project Folder

### Command

```bash
cd my-app
```

### What it does

Moves the terminal into the newly created project directory.

### Why we use it

All project-related commands must be run from inside the project folder.

---

## Install Dependencies

### Command

```bash
npm install
```

### What it does

Downloads and installs all packages listed in `package.json`.

### Why we use it

The project cannot run without its required dependencies.

---

## Start Development Server

### Command

```bash
npm run dev
```

### What it does

Starts the Vite development server.

### Why we use it

Allows us to develop and test the application locally.

---

# 2. Install Tailwind CSS

## Install Tailwind CSS

### Command

```bash
npm install tailwindcss @tailwindcss/vite
```

### What it does

Installs Tailwind CSS and its Vite integration.

### Why we use it

Tailwind provides utility-first CSS classes for building modern UIs quickly.

---

## Configure Vite

Update `vite.config.js`

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [react(), tailwindcss()],
})
```

### What it does

Registers the Tailwind plugin with Vite.

### Why we use it

Allows Vite to process Tailwind CSS during development and production builds.

---

## Import Tailwind CSS

Add to `src/index.css`

```css
@import "tailwindcss";
```

### What it does

Loads Tailwind's utility classes into your application.

### Why we use it

Without importing Tailwind, its classes will not work.

---

# 3. Git Basics

Git is a version control system used to track code changes.

---

## Initialize a Git Repository

### Command

```bash
git init
```

### What it does

Creates a new Git repository in the current project.

### Why we use it

Allows Git to start tracking project files and changes.

---

## Check Repository Status

### Command

```bash
git status
```

### What it does

Shows modified, added, deleted, and untracked files.

### Why we use it

Helps understand what changes are ready to be committed.

---

## Add All Files to Staging Area

### Command

```bash
git add .
```

### What it does

Stages all current changes.

### Why we use it

Git commits only include staged files.

---

## Add a Specific File

### Command

```bash
git add filename.js
```

### What it does

Stages only the specified file.

### Why we use it

Useful when you want to commit selected changes.

---

## Create a Commit

### Command

```bash
git commit -m "Initial commit"
```

### What it does

Saves a snapshot of staged changes.

### Why we use it

Creates a checkpoint in project history that can be reviewed or restored later.

---

# 4. Connect Project to GitHub

## Add Remote Repository

### Command

```bash
git remote add origin https://github.com/username/repository-name.git
```

### What it does

Connects your local repository to a GitHub repository.

### Why we use it

Allows pushing and pulling code between local machine and GitHub.

---

## Check Connected Repository

### Command

```bash
git remote -v
```

### What it does

Displays all remote repositories linked to the project.

### Why we use it

Verifies where code will be pushed or pulled from.

---

## Display Remote URL

### Command

```bash
git remote get-url origin
```

### What it does

Shows the exact URL of the connected GitHub repository.

### Why we use it

Confirms the repository destination before pushing code.

---

# 5. Push Code to GitHub

## Rename Branch to Main

### Command

```bash
git branch -M main
```

### What it does

Renames the current branch to `main`.

### Why we use it

Most GitHub repositories use `main` as the default branch.

---

## Push Code First Time

### Command

```bash
git push -u origin main
```

### What it does

Uploads local commits to GitHub and links the local branch to the remote branch.

### Why we use it

Required the first time a branch is pushed.

---

## Push Future Changes

### Command

```bash
git push
```

### What it does

Uploads new commits to GitHub.

### Why we use it

Keeps the remote repository updated with local changes.

---

# 6. Pull Code from GitHub

## Pull Latest Changes

### Command

```bash
git pull origin main
```

### What it does

Downloads and merges changes from GitHub into the local project.

### Why we use it

Keeps your local code synchronized with the remote repository.

---

# 7. Clone Existing Repository

## Clone a Repository

### Command

```bash
git clone https://github.com/username/repository-name.git
```

### What it does

Downloads an existing GitHub repository.

### Why we use it

Allows working on projects already stored on GitHub.

---

# 8. Branch Management

## List Branches

### Command

```bash
git branch
```

### What it does

Shows all local branches.

### Why we use it

Helps identify the current working branch.

---

## Create New Branch

### Command

```bash
git checkout -b feature-login
```

### What it does

Creates and switches to a new branch.

### Why we use it

Allows development of new features without affecting the main branch.

---

## Switch Branch

### Command

```bash
git checkout main
```

### What it does

Moves to another branch.

### Why we use it

Useful for working on different features or versions.

---

## Delete Branch

### Command

```bash
git branch -d feature-login
```

### What it does

Deletes a local branch.

### Why we use it

Removes branches that are no longer needed.

---

# 9. View Git History

## Show Commit History

### Command

```bash
git log
```

### What it does

Displays detailed commit history.

### Why we use it

Allows tracking project changes over time.

---

## Show Short Commit History

### Command

```bash
git log --oneline
```

### What it does

Displays commit history in a compact format.

### Why we use it

Makes reviewing commits easier.

---

# 10. Build for Production

## Create Production Build

### Command

```bash
npm run build
```

### What it does

Generates optimized production files.

### Why we use it

Prepares the application for deployment.

---

## Preview Production Build

### Command

```bash
npm run preview
```

### What it does

Runs a local server with the production build.

### Why we use it

Allows testing the production version before deployment.

---

# Complete Git Workflow Example

```bash
# Initialize repository
git init

# Add files
git add .

# Create commit
git commit -m "Initial commit"

# Connect GitHub repository
git remote add origin https://github.com/username/repository-name.git

# Rename branch
git branch -M main

# Push code
git push -u origin main
```

This workflow is typically used when creating a new project and uploading it to GitHub for the first time.
