## Steps to Implement the Changes

### 1. **User Management**
- Added the user `softservedata` to the repository:
  1. Navigate to **Settings** > **Collaborators and teams** in the GitHub repository.
  2. Add `softservedata` as a collaborator with the appropriate permissions.

---

### 2. **Branch Management**
- **Created the `develop` branch and set it as the default branch**:
  1. Run the following commands in your terminal:
     ```bash
     git checkout main
     git branch develop
     git push origin develop
     ```
  2. Go to **Settings** > **Branches** in GitHub.
  3. Under "Default branch," click **Change default branch** and select `develop`.

- **Protected the `main` and `develop` branches**:
  1. Navigate to **Settings** > **Branches** > **Add rule**.
  2. For the `main` branch:
     - Require pull requests before merging.
     - Require approval from the repository owner.
  3. For the `develop` branch:
     - Require pull requests before merging.
     - Require at least 2 approvals.

---

### 3. **Code Ownership**
- Added a `CODEOWNERS` file:
  1. Created a [CODEOWNERS](http://_vscodecontentref_/0) file with the following content:
     ```plaintext
     * @softservedata
     ```
  2. Committed and pushed the file:
     ```bash
     git add .github/CODEOWNERS
     git commit -m "Add CODEOWNERS file"
     git push origin main
     ```

---

### 4. **Pull Request Template**
- Added a pull request template:
  1. Created a [pull_request_template.md](http://_vscodecontentref_/1) file.
  2. Committed and pushed the file:
     ```bash
     git add .github/pull_request_template.md
     git commit -m "Add pull request template"
     git push origin main
     ```

---

### 5. **Repository Enhancements**
- **Created a project**:
  1. Navigate to **Projects** in the GitHub repository.
  2. Create a new project and configure it as needed.

- **Added a deploy key**:
  1. Generated an SSH key pair:
     ```bash
     ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
     ```
  2. Added the public key as a deploy key in **Settings** > **Deploy keys**.

---

### 6. **Notifications**
- Set up a Discord server and integrated GitHub notifications:
  1. Created a Discord server.
  2. Generated a webhook in **Server Settings** > **Integrations** > **Webhooks**.
  3. Added the webhook URL to the repository in **Settings** > **Webhooks**.

---

### 7. **GitHub Actions**
- **Created a Personal Access Token (PAT)**:
  1. Navigated to **Developer settings** > **Personal access tokens** > **Generate new token** in GitHub.
  2. Selected the required scopes:
     - Full control of private repositories.
     - Full control of orgs and teams, read and write org projects.

- **Added the PAT to repository secrets**:
  1. Navigated to **Settings** > **Secrets and variables** > **Actions**.
  2. Added a new secret with the name `PAT` and the value of the token.

---
