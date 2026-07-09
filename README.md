Employee Portal CI/CD using GitHub Actions & AWS EC2
📌 Project Overview

This project demonstrates a Continuous Integration and Continuous Deployment (CI/CD) pipeline for an Employee Portal hosted on an AWS EC2 instance. Whenever a developer pushes changes to the GitHub repository, GitHub Actions automatically validates the HTML, connects securely to the EC2 instance using SSH, deploys the latest version to the Nginx web server, and restarts the service.

🚀 Features
Automated deployment using GitHub Actions
HTML validation before deployment
Secure SSH authentication using GitHub Secrets
Automatic deployment to AWS EC2
Nginx web server hosting
Automatic website refresh after deployment
🛠️ Tech Stack
HTML
Git & GitHub
GitHub Actions
AWS EC2 (Ubuntu)
Nginx
SSH
📂 Project Structure
Employee-Portal-CICD/
│
├── index.html
└── .github/
    └── workflows/
        └── deploy.yml
⚙️ CI/CD Workflow
Developer
     │
     │ git push
     ▼
GitHub Repository
     │
     ▼
GitHub Actions
     │
     ├── Checkout Repository
     ├── Validate HTML
     ├── Connect to EC2 via SSH
     ├── Copy index.html to /var/www/html
     └── Restart Nginx
              │
              ▼
      Employee Portal Website
🔄 Workflow Steps
Developer pushes code to the main branch.
GitHub Actions is triggered automatically.
The workflow checks out the latest source code.
HTML is validated using tidy.
GitHub Actions connects to the EC2 instance via SSH.
The latest index.html is copied to the Nginx web directory.
Nginx is restarted.
The updated website becomes live.
🔐 GitHub Secrets

The following repository secrets are required:

Secret Name	Description
EC2_HOST	EC2 Public IP Address
EC2_USER	Ubuntu Username (ubuntu)
EC2_SSH_KEY	Private SSH Key used for deployment
▶️ Deployment

Every push to the main branch automatically triggers deployment.

git add .
git commit -m "Updated Employee Portal"
git push origin main
🌐 Website

Access the deployed Employee Portal using your EC2 public IP:

http://<EC2-PUBLIC-IP>
📸 Screenshots

Add screenshots of:

GitHub Repository
GitHub Actions Workflow
AWS EC2 Instance
Employee Portal Website
🎯 Learning Outcomes
Continuous Integration (CI)
Continuous Deployment (CD)
GitHub Actions Workflows
AWS EC2 Deployment
SSH Authentication
GitHub Secrets Management
Nginx Configuration
Automated Website Deployment
👩‍💻 Author

Dipali Patil

AWS | DevOps | Cloud Computing Enthusiast
