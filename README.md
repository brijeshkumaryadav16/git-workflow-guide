# Git Workflow Guide  

A structured guide on commit message types, branching strategies, and best practices for maintaining a clean Git history.

![GitHub stars](https://img.shields.io/github/stars/your-username/git-workflow-guide?style=flat-square)

---

## 📌 Table of Contents  
- [Commit Types](#commit-types)  
- [Commit Message Format](#commit-message-format)  
- [Git Branching Workflow](#git-branching-workflow)  
- [Branch Naming Convention](#branch-naming-convention)  
- [Key Points](#key-points)  

---

## 🚀 Commit Types  

- **feat**: Introduces new features  
    *Examples*: Adding a new component, implementing a new API endpoint.  
- **fix**: Bug fixes  
    *Examples*: Resolving UI bugs, fixing broken links.  
- **hotfix**: Critical fixes in production  
    *Examples*: Quick fixes for urgent production issues.  
- **docs**: Documentation updates  
    *Examples*: Updating the README, adding JSDoc comments.  
- **style**: Code style changes  
    *Examples*: Adjusting spaces, commas, or formatting without altering functionality.  
- **refactor**: Refactoring code  
    *Examples*: Improving code readability or maintainability without changing behavior.  
- **perf**: Performance improvements  
    *Examples*: Optimizing code for better performance, reducing bundle size.  
- **test**: Test-related changes  
    *Examples*: Adding or updating tests, adding test logs.  
- **infra**: Infrastructure changes  
    *Examples*: Modifying Webpack configuration, updating CI/CD pipelines.  
- **chore**: Routine maintenance  
    *Examples*: Updating dependencies, minor housekeeping tasks.  
- **revert**: Reverts a previous commit  
    *Examples*: Undoing a commit that caused issues or wasn’t needed.  

---

## 📜 Commit Message Format  

**Structure:**  
```md
<type>: <subject>

<body> (optional)

<footer> (optional)
```

**Examples:**  
```md
feat: Add new navigation bar

- Added links to Home, About, and Contact pages
- Implemented dropdown for user profile
```
```md
fix: Correct button alignment

- Fixed misalignment of the submit button on the form
```
```md
docs: Update installation instructions

- Added steps for setting up the project locally
```
```md
style: Improve CSS formatting

- Reformatted CSS for better readability
```
```md
test: Add header component tests

- Added unit tests for navigation bar
- Ensured edge case coverage
```
```md
infra: Update Webpack configuration

- Changed output directory for better organization
```

---

## 🔥 Git Branching Workflow  

### **Branch Strategy**  

- **`main`**: Production-ready code.  
- **`dev`**: Active development.  

### **Workflow Steps**  

1. **Create a Feature Branch**  
    Start from `dev`:  
    ```bash
    git checkout dev
    git checkout -b feature/<name>
    ```

2. **Commit Your Work**  
    Commit changes as you progress:  
    ```bash
    git commit -m "feat: Add login form"
    ```

3. **Push the Branch**  
    Push your changes to the remote repository:  
    ```bash
    git push origin feature/<name>
    ```

4. **Open a Pull Request (PR)**  
    Open a PR to merge your feature branch into `dev`.  

5. **Squash and Merge**  
    Choose **Squash and Merge** to consolidate all commits into one clean commit.  

6. **Merge into `dev`**  
    Once approved, merge the PR into `dev`.  

7. **Merge `dev` into `main`**  
    After testing, merge `dev` into `main` for production release.  

---

## 🏷️ Branch Naming Convention  

- **Feature**: `feature/<name>`  
- **Bugfix**: `bugfix/<description>`  
- **Hotfix**: `hotfix/<description>`  

---

## ✅ Key Points  

✅ Always work on feature branches (`feature/<name>`) from `dev`.  
✅ Use **Squash and Merge** to keep history clean.  
✅ Merge into `dev` first, then `main` for production.  
