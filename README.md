# Final AWS Cloud Deployment Project (Module 07)
**Prepared by:** Shreyash Sanjay Kamble

## 1. Project Overview
This project implements a fully automated, production-ready serverless REST API hosted on AWS. It demonstrates modern cloud architecture practices, infrastructure automation, and rigorous security management.

## 2. AWS Services Utilized (3+ Services)
* **AWS Lambda**: Executes core backend logic (Python/Node.js runtime) on-demand without managing underlying servers.
* **Amazon API Gateway**: Acts as the secure HTTP entry point, routing incoming web traffic directly to the backend Lambda functions.
* **AWS IAM (Identity and Access Management)**: Enforces the principle of least privilege using granular permissions and secure credentials.
* **GitHub Actions (CI/CD)**: Automates build, test, and deployment stages directly to the AWS cloud environment.

## 3. Architecture & Deployment Workflow
1. **Developer Push**: Code changes are committed and pushed to the `main` branch of the GitHub repository.
2. **CI/CD Automation**: GitHub Actions triggers an automated pipeline (`deploy.yml`) using a secure Ubuntu runner.
3. **Framework Deployment**: The Serverless Framework packages the application and interfaces with AWS APIs.
4. **Cloud Execution**: API Gateway and Lambda functions are provisioned/updated instantly, exposing a live public endpoint.

## 4. Security & Permissions Configuration
* **Encrypted Secrets**: AWS credentials (`AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`) are securely stored in GitHub Repository Secrets.
* **Access Control**: Configured IAM user permissions (`student-user`) to restrict resource modification and align with organizational compliance guidelines.
