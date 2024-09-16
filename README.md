# Midnight Commit 

## Automated Daily Commits with GitHub Actions - Overview

This GitHub Actions workflow performs a daily commit to the repository at midnight UTC. It updates a file with a commit number, starting from 1 and incrementing with each commit made on subsequent days.

## Workflow

The workflow is defined in `.github/workflows/commit.yml` and is scheduled to run daily at midnight UTC using a cron job. The main steps include:

1. **Checkout Repository**: Clones the repository to the runner. 
2. **Create File and Commit**:
   - Checks if the file `commit_number.md` exists in the root directory.
   - If the file does not exist, it creates it and writes an initial message and commit number.
   - If the file exists, it reads the current commit number, increments it, and updates the file.
   - Configures Git with the specified user name and email.
   - Adds the file to the Git index, commits the changes, and pushes the commit to the repository.

## File Structure

- `.github/workflows/commit.yml`: Defines the GitHub Actions workflow.
- `commit_number.md`: The file updated and committed by the workflow.

## Configuration

- **Schedule**: The workflow runs daily at midnight UTC (`0 0 * * *`).
- **GitHub Token**: The workflow uses the `GITHUB_TOKEN` secret to authenticate and push changes.

## Example `commit_number.md` Output

```markdown
Hello, my name is Bishwa Shah.
Commit number: 1
This is part of an **automated daily commit** performed by a **GitHub Actions workflow**.
```