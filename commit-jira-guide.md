# Commit Guide for Proper Integration with Jira

This guide provides best practices for committing changes to ensure they are properly linked with Jira tasks in the **Climate AI Engine** project. Following this structure will allow seamless integration and tracking of tasks in Jira.

---

## 1. Commit Message Structure

To ensure that Jira recognizes your commits and links them to the appropriate tasks, follow this format:

```plaintext
[JIRA-ISSUE-ID] Descriptive message about the changes

Optional detailed description of the changes made.
```

### Example:
```plaintext
[CLIM-123] Add support for rainfall probability calculations

- Integrated rainfall prediction logic using AI module.
- Added unit tests for prediction accuracy.
- Updated the README to include documentation about the new feature.
```

---

## 2. Steps to Commit Changes

1. **Fetch the Latest Changes:**
   Always ensure your local repository is up-to-date before starting.
   ```bash
   git pull origin main
   ```

2. **Create a New Branch:**
   Use a branch naming convention that includes the Jira issue ID.
   ```bash
   git checkout -b feature/CLIM-123-rainfall-calculation
   ```

3. **Make Changes:**
   Implement the required changes, ensuring that your work aligns with the Jira issue.

4. **Stage Changes:**
   Add the changes to the staging area.
   ```bash
   git add .
   ```

5. **Commit Changes:**
   Use the proper format for the commit message.
   ```bash
   git commit -m "[CLIM-123] Add support for rainfall probability calculations"
   ```

6. **Push Changes to the Remote Repository:**
   Push your branch to GitHub.
   ```bash
   git push origin feature/CLIM-123-rainfall-calculation
   ```

7. **Create a Pull Request:**
   Open a pull request in GitHub and include the Jira issue ID in the title or description:
   ```plaintext
   Title: [CLIM-123] Add rainfall probability calculations
   Description: Implements the logic for rainfall predictions. See details in CLIM-123.
   ```

---

## 3. Best Practices

### Include Relevant Details:
- Always mention the Jira issue ID (`[CLIM-123]`) at the beginning of your commit message.
- Provide a clear and concise description of the changes.

### Commit Frequently:
- Commit small, logical chunks of work instead of large changes.

### Link Pull Requests:
- Ensure the Jira issue is mentioned in the pull request description to establish a connection.

### Test Before Committing:
- Run all tests and verify that your changes do not introduce new issues.

---

## 4. Automations in Jira

When you follow the correct format, Jira will automatically:
- Link the commit to the respective Jira issue.
- Display the commit, branch, and pull request in the **Development** section of the Jira issue.
- Optionally update the issue status based on GitHub events (e.g., moving to "In Progress" when a commit is made).

---

By adhering to this guide, you ensure that all changes are properly tracked and integrated with the Jira project, facilitating better collaboration and project management. 🚀
