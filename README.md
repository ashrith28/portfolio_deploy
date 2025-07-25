# 🚀 Deploy Portfolio to AWS S3 using GitHub Actions

This project automates the deployment of a personal portfolio website to an AWS S3 bucket using **GitHub Actions**. Every time you push changes to the `main` branch, your website is automatically built (if required) and deployed to your S3 bucket.

---

## 📁 Project Structure


├── .github/

│ └── workflows/

│ └── main.yml

├── portfolio_deploy/

│  └── assets/

│  └──css/

│  └── javascript/

│  └──index.html

├── README.md
---

## ⚙️ Features

- 🔁 **Automatic deployment** on every push to `main`
- ☁️ **Amazon S3** for static website hosting
- 🔒 Uses **GitHub Actions** for CI/CD
- ❌ Optional CloudFront cache invalidation support

---

## 🚧 Prerequisites

- An AWS account
- A pre-created S3 bucket (enable static website hosting)
- Either:
  - IAM role with OIDC trust and permissions (recommended)
  - Or IAM user with access keys and S3 permissions

---

## 📦 Deployment Workflow

The GitHub Actions workflow file is located at:

```
.github/workflows/main.yml
```

✅ What it does:
Checks out the code

Installs dependencies and builds the project (if needed)

Configures AWS credentials

Syncs the dist (or build) folder to the S3 bucket

Access Keys (Simpler)
Store the following GitHub secrets:

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

And modify the workflow to use them directly.

# CI/CD using GitHub Actions → AWS S3

This GitHub Action builds (if needed) and deploys the portfolio to an AWS S3 bucket.  
It uses secure OIDC-based authentication to assume an IAM role with just enough permissions.  
Automatically syncs files and cleans up old assets on every push to `main`.

## Setup
1. Create an IAM role (or user) with S3 access.
2. If using OIDC, configure trust policy for your repo and branch.
3. Add AWS-related secrets (or just S3 bucket and region if using keys).
4. Push to `main` to trigger deployment.



👨‍💻 Author
Ashrith
GitHub: ashrith28

