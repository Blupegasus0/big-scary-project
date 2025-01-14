# Git Collaboration Guide
# [Fork Me](CONTRIBUTION.md)

Welcome to the **Big Scary Project** Git collaboration guide! This guide will help you learn how to collaborate effectively using Git and GitHub.

## Repository Info
- **Git Repository HTTPS URL (easier)**: `https://github.com/<your-username>/big-scary-project.git`
- **Git Repository SSH URL (safer)**: `git@github.com:<your-username>/big-scary-project.git`
- **Branches**: `main`, `dev`

## Branch Naming Scheme
Use the following format for creating branches:

```
<user alias>/<feature|bug|hotfix>/<issue item ID>_<title>
```

### Examples:
- `kiara/feature/271_add_more_cowbell`
- `amir/bug/270_fix_leakage`

- **User Alias**: Your email address minus the `@domain`.
- **Issue Item ID**: Optional if there is no related issue.
- **Type**: Indicate if it is a `feature`, `bug`, or `hotfix`.

---

## Git Workflow

### 1. Cloning the Repository

```bash
# Clone the repository to your local machine
git clone https://github.com/<your-username>/big-scary-project.git
git clone git@github.com:<your-username>/big-scary-project.git
```

### 2. Creating a New Branch

#### Step 1: Switch to the `dev` Branch
```bash
# Navigate to the dev branch
git checkout dev
```

#### Step 2: Create and Switch to Your New Branch
```bash
# Replace <user alias> and <branch type/details> appropriately
git checkout -b <user alias>/<branch type>/<issue item ID>_<title>
```

#### Example:
```bash
git checkout -b aneesa/feature/add_navbar
```

### 3. Making Changes

1. Add your HTML, CSS, or JavaScript code to the project.
2. Use meaningful commit messages to describe what you have done.

#### Example:
```bash
git add index.html
git commit -m "feat: Add navbar with responsive design"
```

#### Recommended Commit Structure:
`<type>: <description>`
[More info](https://www.conventionalcommits.org/en/v1.0.0/#summary)

**Common Types include**
+ fix 
+ feat 
+ docs 
+ test 
+ chore

### 4. Pushing Your Branch

Push your branch to the remote repository:
```bash
git push -u origin <user alias>/<branch type>/<issue item ID>_<title>
```

#### Example:
```bash
git push -u origin aneesa/feature/add_navbar
```

---

## Merging Your Changes

### 1. Create a Pull Request (PR)
1. Navigate to the repository on GitHub.
2. Go to **Pull Requests** > **New Pull Request**.
3. Select:
   - **Base Branch**: `dev`
   - **Compare Branch**: Your branch
4. Add a meaningful title and description.
5. Assign reviewers (at least one team member).
6. Submit the PR.

### 2. Review and Approve
- Reviewers should check the PR, suggest changes if necessary, and approve it.

### 3. Merge the Branch
- After approval, merge the branch into `dev`.

---

## Resolving Conflicts

1. GitHub will notify you if there are conflicts.
2. Pull the latest `dev` branch:
   ```bash
   git pull origin dev
   ```
3. Resolve conflicts in your local editor.
4. Commit the resolved changes:
   ```bash
   git add .
   git commit -m "Resolved merge conflicts"
   ```
5. Push the updates:
   ```bash
   git push
   ```

---

## Keeping Your Branch Updated
Regularly update your branch with the latest changes from `dev` to minimize conflicts:

```bash
git checkout dev
git pull origin dev
git checkout <your-branch>
git merge dev
```

---

## Best Practices

- **Small, Atomic Commits**: Make frequent commits with clear messages.
- **Branch Clean-Up**: After merging, delete your branch to keep the repository clean.
- **Code Reviews**: Always have at least one teammate review your code before merging.
- **Communicate**: Discuss with the team to avoid overlapping work.

---

## Practice Task

1. Each team member creates a new branch following the naming scheme.
2. Build a simple website using `lorem ipsum` text for placeholder content:
   - Create an "About Us" section in `about.html`.
   - Add a "Contact Us" section in `contact.html` with a basic form.
   - Design a "Services" section in `services.html` listing mock services.
   - Create a "Portfolio" section in `portfolio.html` with sample project descriptions.
   - Add a shared `styles.css` file and style the navigation bar and general layout.
   - Add simple animations in `animations.css` for a hover effect on the nav bar.
   - Implement responsive design using media queries in `responsive.css`.
3. Push your branch and submit a PR to `dev`.
4. Review at least one teammate’s PR to ensure quality and consistency.

---

Happy coding! 🎉
