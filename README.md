Employee Portal CI/CD Pipeline using GitHub Actions & AWS EC2
📖 Project Overview

The Employee Portal CI/CD Pipeline is a beginner-friendly DevOps project that demonstrates how to automate website deployment using GitHub Actions and Amazon EC2.

In this project, an Employee Portal is hosted on an AWS EC2 Ubuntu instance running Nginx. Whenever a developer pushes changes to the GitHub repository, GitHub Actions automatically validates the HTML file, securely connects to the EC2 instance using SSH, deploys the latest version of the website, and restarts the Nginx service.

This eliminates manual deployment, reduces deployment time, and ensures the server always hosts the latest version of the application.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🚀 Project Objectives
Automate website deployment using GitHub Actions.
Validate HTML before deployment.
Deploy the latest source code to an EC2 instance.
Securely connect to EC2 using SSH keys.
Automatically restart Nginx after deployment.
Implement a simple CI/CD workflow.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🛠️ Technologies Used
Technology	Purpose

HTML : Employee Portal Web Page

Git	: Version Control

GitHub	: Source Code Repository

GitHub Actions :	CI/CD Automation

AWS EC2 (Ubuntu) : Hosting Server

Nginx : Web Server

SSH	: Secure Remote Deployment

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📂 Project Structure

    Employee-Portal-CICD
    │
    ├── index.html
    │
    └── .github
        └── workflows
           └── deploy.yml
        
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
⚙️ Workflow Architecture

                Developer
                    │
              git push (main)
                    │
                    ▼
          GitHub Repository
                    │
                    ▼
          GitHub Actions Workflow
                    │
     ┌──────────────┼──────────────┐
     │              │              │
     ▼              ▼              ▼
    Checkout Code   Validate HTML   SSH Authentication
                                    │
                                    ▼
                           Connect to EC2 Instance
                                    │
                                    ▼
                     Copy index.html to /var/www/html
                                    │
                                    ▼
                           Restart Nginx Service
                                    │
                                    ▼
                        Updated Employee Portal
                        
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                        
🔄 CI/CD Workflow

The deployment process follows these steps:

A developer pushes code to the main branch.

GitHub Actions automatically triggers the workflow.

The latest source code is checked out from GitHub.

HTML validation is performed using tidy.

GitHub Actions establishes a secure SSH connection to the EC2 instance.

The updated index.html file is copied to the Nginx web directory (/var/www/html).

Nginx is restarted to apply the latest changes.

The updated Employee Portal becomes available through the EC2 public IP.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔐 GitHub Secrets
The following repository secrets are configured for secure deployment.

Secret Name	Description

EC2_HOST :	EC2 Public IPv4 Address

EC2_USER : Ubuntu Login User

EC2_SSH_KEY	" Private SSH Key for Authentication

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📄 GitHub Actions Workflow

The workflow performs the following tasks:

Checkout the latest source code.
Validate the HTML file.
Connect to the EC2 instance via SSH.
Copy the website files to the Nginx directory.
Restart the Nginx service.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📥 Deployment Process

Whenever changes are made:
git add .
git commit -m "Updated Employee Portal"
git push origin main

GitHub Actions automatically:

Downloads the latest source code.

Validates the HTML.

Deploys the website to EC2.

Restarts Nginx.

Publishes the updated website.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🌐 Website Access

After successful deployment, open the application using:

http://<EC2-PUBLIC-IP>

Example:

http://13.xxx.xxx.xxx
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📈 Project Outcomes

After completing this project, you will understand:

Continuous Integration (CI)

Continuous Deployment (CD)

GitHub Actions Workflow

SSH-based Deployment

GitHub Secrets Management

AWS EC2 Hosting

Nginx Web Server Configuration

Automated Website Deployment

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

💡 Future Enhancements

Deploy a Flask or Node.js application.

Add Docker support.

Integrate Docker Hub for container deployment.

Configure HTTPS using Let's Encrypt.

Add deployment notifications using Amazon SNS or Slack.

Implement rollback support for failed deployments.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
👩‍💻 Author
Dipali Patil

Cloud Computing | AWS | DevOps | GitHub Actions | CI/CD Enthusiast
