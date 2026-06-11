# AWS Serverless Contact Form

A fully serverless contact form built using AWS services. Users can submit messages through a frontend hosted on AWS Amplify, which are processed via API Gateway and Lambda, and delivered as emails using Amazon SES. The project includes logging and monitoring via CloudWatch and follows least-privilege IAM principles.

---

## Architecture

```
Frontend (AWS Amplify)
        ↓
API Gateway (HTTP API)
        ↓
AWS Lambda
        ↓
Amazon SES
        ↓
Email Inbox

CloudWatch Logs (Lambda Observability)
```

---

## Features

* Fully serverless architecture (no backend servers)
* Form submission from static frontend
* Email delivery via AWS SES
* Input validation and error handling
* Secure IAM permissions (least privilege)
* Logging and monitoring with CloudWatch
* CORS-enabled API for frontend integration

---

## AWS Services Used

* AWS Amplify – Frontend hosting
* API Gateway (HTTP API) – REST endpoint
* AWS Lambda – Backend processing logic
* Amazon SES – Email delivery service
* AWS IAM – Permissions and security
* Amazon CloudWatch – Logging and debugging

---

## How It Works

1. User submits a contact form from the frontend
2. Amplify sends a POST request to API Gateway
3. API Gateway triggers a Lambda function
4. Lambda validates input and sends email via SES
5. CloudWatch logs execution details for debugging and monitoring

---

## API Endpoint

```
POST /contact
https://YOUR_API_ID.execute-api.ap-southeast-2.amazonaws.com/contact
```

---

## Environment / Configuration

* SES must be configured in sandbox mode (or production access required for external emails)
* Verified sender and receiver emails required in SES sandbox
* CORS enabled on API Gateway

---

## Key Learnings

* Building serverless architectures using AWS services
* Integrating API Gateway with Lambda functions
* Handling IAM permissions with least privilege
* Working with AWS SES for transactional email delivery
* Debugging and monitoring using CloudWatch logs
* Connecting frontend applications to backend cloud services

---

## Future Improvements

* Add CAPTCHA to prevent spam submissions
* Store messages in DynamoDB for persistence
* Add authentication (AWS Cognito)
* Improve frontend UI/UX with form validation and animations
* Add rate limiting at API Gateway

---

## Tech Stack

* AWS Amplify
* AWS API Gateway (HTTP API)
* AWS Lambda (Python)
* Amazon SES
* AWS IAM
* Amazon CloudWatch
* HTML / CSS / JavaScript

---

## Notes

This project was built as a learning exercise to understand modern serverless architectures and AWS cloud fundamentals.
