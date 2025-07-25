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

Here are the some screenshots of this project

<img width="1821" height="736" alt="Screenshot from 2025-07-25 11-10-08" src="https://github.com/user-attachments/assets/cae291eb-4dce-4fc2-8fe9-daee76cd422a" />

<img width="1821" height="832" alt="Screenshot from 2025-07-25 11-10-41" src="https://github.com/user-attachments/assets/cd39d6ee-5de5-4d5a-bc2d-01196fa546a4" />

<img width="2944" height="1664" alt="Screenshot from 2025-07-25 11-06-41" src="https://github.com/user-attachments/assets/d78db19b-640e-4644-8d74-ab3c1c011328" />

<img width="997" height="580" alt="Screenshot from 2025-07-25 10-59-57" src="https://github.com/user-attachments/assets/19fdfc4c-e10a-4ad1-9baf-c481f885e71c" />
