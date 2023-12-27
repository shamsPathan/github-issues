# Problem and Solution

## Problem Description

When attempting to connect to GitHub via SSH, the following error is encountered:

```bash
ssh: connect to host github.com port 22: Network is unreachable
fatal: Could not read from remote repository
```

## Solution

To resolve the connectivity issue, modify the SSH configuration as follows:

1. Open the SSH configuration file using a text editor:

    ```bash
    nano ~/.ssh/config
    ```

2. Add the following configuration to the file:

    ```bash
    Host github.com
        Hostname ssh.github.com
        Port 443
    ```

    This change switches the SSH connection to use port 443, which might bypass certain network restrictions.

After modifying the SSH configuration, attempt to connect to GitHub using SSH again.

---

## GitHub README

### Overview

This repository aims to address the issue of connecting to GitHub via SSH and provides a solution to overcome the encountered error.

### Usage

1. Clone the repository:

    ```bash
    git clone <repository_url>
    cd repository_name
    ```

2. Follow the steps outlined in the Problem and Solution section to update the SSH configuration.

3. Create or modify the `README.md` file:

    ```bash
    nano README.md
    ```

    Add content to the README file to provide instructions or details about your project.

4. Commit and push changes to your GitHub repository:

    ```bash
    git add README.md
    git commit -m "Add README file"
    git push origin main
    ```

### Contributing

Contributions to enhance this solution are welcome! Please feel free to create pull requests or raise issues for improvements or additional details.
