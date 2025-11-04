# Repository mirroring (from GitLab to GitHub)

 This project demonstrates how to **mirror a GitLab repository to GitHub**, ensuring that both repositories remain in sync automatically.

 ---
 ##  Overview

Repository mirroring allows you to **keep two repositories synchronized** — for example, pushing code from **GitLab** to **GitHub** automatically whenever changes are made.

This is useful for:
- Backing up your GitLab repository to GitHub
- Collaborating across different platforms
- Maintaining public and private copies of the same project

---
### Step-1: Create Repository in GitHub
Create a repository with README.md file
![](./images/Screenshot%20(59).png)

### Step-2: Create Personal Access Token(classic)
* GitHub → **Settings → Developer settings → Personal access tokens → Generate new token**
* Grant all permissions/Scopes

![](./images/Screenshot%20(63).png)

**Copy the token**
![](./images/Screenshot%20(64).png)

### Step-3: Create Repository in GitLab
Create a Blank repository with README.md file
![](./images/Screenshot%20(60).png)

### Step-4: Create a mirroring Repository
Set up your project to automatically push or pull changes to/from another repository. Branches, tags, and commits will be synced automatically.

* Open your project → **Settings → Repository → Mirroring repositories**.
* Click ** mirror repository**.
* For **Git repository URL** use the HTTPS push URL in this form:
```
https://<GITHUB_USERNAME>@github.com/<GITHUB_USERNAME>/<GITHUB_REPO>.git
```
* When prompted for a password, paste the **GitHub access token** and save

![](./images/Screenshot%20(65).png)

### Step-5: Clone GitLab Repository in your machine, add files and push to server 

* Open git bash and Clone repository
```
git clone https://gitlab.com/<GITLAB_USERNAME>/<GITLAB_REPO>.git
```
* cd to repository
```
cd <REPO_NAME>
```
* Create a file(index.html)
```
nano index.html
```
* Add some lines
```
<h1>This file is pushed to GitLab</h1>
```
* **commit** and **push** to GitLab Server
```
git add index.html
git commit -m "message"
git push -u origin main
```
## Output
**In GITLAB:**
![](./images/Screenshot%20(73).png)

**In GITHUB:**

Automatically index.html file is synchronized to GitHub repository.
![](./images/Screenshot%20(74).png)

## Conclusion
By following these steps, you can easily mirror your GitLab repository to GitHub, ensuring that your codebase stays synchronized, backed up, and accessible across both platforms.

This setup helps maintain a reliable workflow, supports collaboration, and provides redundancy for your projects.

Using GitLab’s push mirror makes the process automated, secure, and efficient — so your repositories always stay up to date.

