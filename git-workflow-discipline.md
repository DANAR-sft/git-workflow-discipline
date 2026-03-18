# Git Workflow Discipline

## 1. Introduction
This workflow aims to ensure that collaboration on the project is structured, secure, and easy to follow by other developers or contributors.

## 2. Branching Strategy
We implement a **Feature Branching Workflow** to maintain the stability of the `main` branch, ensuring it is always ready for production. All new development should be done in dedicated branches instead of the `main` branch.

- **`main`**: The default and stable branch. Code here is always production-ready.
- **Feature Branches**: Used for developing new features.
- **Bugfix Branches**: Used for fixing bugs.

## 3. Branch Naming Conventions
To keep our branches organized, please use the following prefixes when creating a new branch:

- `feature/` - for new features (e.g., `feature/user-login`)
- `bugfix/` - for bug fixes (e.g., `bugfix/fix-header-style`)
- `hotfix/` - for urgent production fixes (e.g., `hotfix/crash-on-startup`)
- `docs/` - for documentation updates (e.g., `docs/update-readme`)

*All branch names should be in lowercase and use hyphens (-) to separate words.*

## 4. Commit Message Conventions
We follow a standardized commit message format to easily understand the history of our project. Start your commit message with one of these types:

- **`feat:`** A new feature
- **`fix:`** A bug fix
- **`docs:`** Documentation only changes
- **`style:`** Changes that do not affect the meaning of the code (formatting, missing semi-colons, etc.)
- **`refactor:`** A code change that neither fixes a bug nor adds a feature
- **`test:`** Adding missing tests or correcting existing tests
- **`chore:`** Changes to the build process or auxiliary tools and libraries

*Example: `feat: add user authentication endpoint`*

## 5. Development Workflow Steps
1. **Pull the latest changes:** Always start with an up-to-date main branch.
   ```bash
   git checkout main
   git pull origin main
   ```
2. **Create a new branch:**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes, then stage and commit them:**
   ```bash
   git add .
   git commit -m "feat: your descriptive message here"
   ```
4. **Push the branch to the remote repository:**
   ```bash
   git push origin feature/your-feature-name
   ```
5. **Create a Pull Request (PR):** Open a PR against the `main` branch and request a review from your team (if applicable).

## 6. Code Review & Merging
- Review your own code before opening a Pull Request.
- Make sure all automated tests pass before merging.
- Once the code is ready (and approved if you are working in a team), merge the Pull Request.
- Delete the feature branch after merging to keep the repository clean.
