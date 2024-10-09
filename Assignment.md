# Setting Up Branch Rules in Repository

To ensure proper code management and control over your main branch, follow these steps to create and enable branch rules.

## Steps to Create Branch Rules

1. **Navigate to Repository Settings:**
   - Go to your repository on GitHub.
   - Click on the `Settings` tab at the top right.

2. **Access Branch Rules:**
   - In the sidebar, find and click on `Branches`.
   - Under "Branch protection rules," click the `Add branch protection rule` button.

3. **Create a Branch Rule:**
   - In the **Branch name pattern** field, enter the branch name you want to apply the rule to.
     - If you want to apply the rule to the main branch, select `Default (main)` in the dropdown.
     - To target a specific branch, select `Include by pattern` and enter the branch name (e.g., `main` or `develop`).

4. **Bypass Permissions (Admin Only):**
   - Scroll down to the **Bypass permissions** section.
   - Enable the `Allow specified actors to bypass required pull requests` option.
   - In the dropdown, select `Organization Admin Role`. This ensures that only admins can push code directly to the branch without a pull request.

5. **Set Branch Protection Rules:**
   - In the **Branch protection rules**, enable the following options:
     - `Restrict deletions`: This prevents accidental deletion of the branch.
     - `Require a pull request before merging`: This ensures all code is reviewed before being merged.

6. **Additional Settings:**
   - Click on `Show additional settings` to reveal more options.
   - Under **Require approvals**, set the number of required approvals to `1`. This ensures that at least one team member reviews the code before merging.
   - Enable the `Block force pushes` option to prevent forced changes to the branch.

7. **Save Changes:**
   - After selecting your rules and settings, scroll down and click the `Create` or `Save changes` button to apply the branch rules.

---

# Assignment Submission Process

In order to distribute assignments and receive submissions effectively, follow the process outlined below. This will ensure that assignments are tracked properly and students can submit them via GitHub.

## How to Provide Assignments

1. **Push Code to the Main Branch:**
   - As an organization member, you will push the assignment code directly to the `main` branch of the repository.
   - This allows all members of the organization to see the assignment code.
   - Share the repository URL with the members.

2. **Inform Members:**
   - Let the members know when a new assignment is available.
   - They can copy the repository URL to access the code.

## How Students Can Complete the Assignment

### 1. **Clone the Repository:**
   - Students need to clone the repository to their local machines using the repository URL:
     ```bash
     git clone <repo-url>
     ```

### 2. **Create a Branch:**
   - **First-time assignment:** If it’s the student’s first assignment, they need to create an individual branch where they will work on all future assignments:
     ```bash
     git checkout -b <student-branch>
     ```

   - **Subsequent assignments:** For future assignments, students will continue working on the same individual branch they created for their first assignment. There’s no need to create a new branch for each assignment:
     - Switch to their individual branch:
       ```bash
       git checkout <student-branch>
       ```
   
   - Add or modify the required files for the new assignment on this branch.

### 3. **Complete the Assignment:**
   - Add or modify the required files in the new assignment branch.

### 4. **Commit and Push the Changes:**
   - After completing the assignment, students should commit their changes:
     ```bash
     git add .
     git commit -m "Completed Assignment <student-branch>"
     ```
   - Push the changes to GitHub:
     ```bash
     git push origin <student-branch>
     ```

### 5. **Raise a Pull Request (PR):**
   - Once the changes are pushed, students need to raise a Pull Request (PR) from their assignment branch to the main repository.
   - In the PR description, they should include details of what has been done.

---

## Reviewing and Providing Feedback

1. **Review the PR:**
   - As the reviewer, you will review the student's PR to check the assignment for accuracy and quality.

2. **Give Feedback:**
   - Use GitHub's PR review features to give feedback on the code or ask for improvements.
   - You can approve the PR if the assignment is complete or request changes if necessary.
