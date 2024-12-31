# GitHub Project Board and Issues Cloner

This repository contains a Jupyter Notebook designed to automate the process of cloning GitHub project boards, issues, and milestones. The script simplifies the migration or backup of project management data across GitHub repositories.

## Features

- Clone GitHub project boards, including columns and cards.
- Migrate issues and their metadata (e.g., labels, assignees).
- Copy milestones from one repository to another.
- Generate logs for tracking the cloning process and debugging.

## Requirements

Before using this notebook, ensure you have the following:

1. **Python Environment**: Python 3.8 or later is recommended.
2. **Required Libraries**: Install the dependencies listed in the `requirements.txt` file (see below).
3. **GitHub Personal Access Token**: Generate a token with the necessary permissions (e.g., `repo`, `project`, and `admin:org`).

### Clone the Repository


```bash
git clone https://github.com/ahsun-tariq/projectboard-cloner.git
cd projectboard-cloner
```

### Install Dependencies

The required libraries are specified in the `requirements.txt` file. Install them using:

```bash
pip install -r requirements.txt
```

### Set your GitHub username and token in the env.txt file
-  Replace the first line with your GitHub handle.
-  Replace the second line with your token.
-  Ensure that the token has permissions for repo, project, and admin:org


### Launch the Notebook
```bash
jupyter notebook
```

### Configure Project, Source and Destination Repositories
- Set your source repository to be cloned ```sourceRepo = "SOURCE-REPO" ```
- Set the organization or user who owns the source repository ```org = "ORG/USER```
- Set your destination repositories in the list: ```repoList = ["repo1", "repo2",...] ```. This corresponds to repos where items will be cloned.
- Set your projectboard name in the source repository to be cloned: ```projectBoard = "PROJECT-BOARD-NAME" ```

### Execute the Notebook
- Run all cells in the notebook sequentially.
- Monitor progress and review logs displayed in the output.
- Address any errors as indicated in the logs.

### Validate Results
Visit the target repository to confirm that projectboard and issues have been copied. 

## Notes
- Rate Limits: The GitHub API has rate limits. Ensure your token has sufficient permissions and consider enabling API pagination if necessary. You can set the time in the function ```sleep()``` to avoid failure.
- Security: Keep your GitHub token secure. Do not share it or hardcode it into the notebook.
