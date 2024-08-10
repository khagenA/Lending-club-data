# Using Personal Access Tokens (PAT) with GitHub

Personal Access Tokens (PATs) provide a way to authenticate to GitHub. Here’s a general guide on how to generate and use a PAT:

---

## 1. Generating a Personal Access Token (PAT)

1. **Log in to GitHub**:
   - Go to [GitHub](https://github.com) and log in to your account.

2. **Navigate to Developer Settings**:
   - Click on your profile icon in the upper-right corner.
   - Select **Settings** from the dropdown menu.
   - In the left sidebar, click **Developer settings**.

3. **Create a New Token**:
   - Click on **Personal access tokens**.
   - Click **Generate new token**.

4. **Configure Your Token**:
   - **Note**: Enter a descriptive name for the token.
   - **Select Scopes**: Choose the appropriate scopes/permissions needed (e.g., `repo` for repository access).
   - **Expiration**: Set an expiration date if desired.
   - Click **Generate token**.

5. **Copy the Token**:
   - Copy the generated token and store it securely. It will not be visible again.

---

## 2. Using the PAT

1. **Clone a Repository Using HTTPS**:
   - Use the following format to clone a repository with your PAT:
     ```bash
     git clone https://<username>:<access_token>@github.com/username/repository.git
     ```
   - Replace `<username>` with your GitHub username and `<access_token>` with the token.

   **Example**:
     ```bash
     git clone https://your_username:your_personal_access_token@github.com/example/repo.git
     ```

2. **Use PAT in Scripts**:
   - If you need to use the PAT in scripts or applications, store it as an environment variable:
     ```bash
     export GITHUB_TOKEN=your_personal_access_token
     ```
   - Access it in your application:
     ```python
     import os
     token = os.getenv('GITHUB_TOKEN')
     ```



## 3. Example Usage

 **Cloning a Repository**:
   - Suppose your GitHub username is `johndoe` and your personal access token is `ghp_abc123xyz456`.
   - To clone a repository named `my-repo`, you would use:
     ```bash
     git clone https://johndoe:ghp_abc123xyz456@github.com/johndoe/my-repo.git
     ```

This guide provides a general overview of working with PATs for educational purposes. Always handle sensitive information securely and follow best practices to protect your credentials.
