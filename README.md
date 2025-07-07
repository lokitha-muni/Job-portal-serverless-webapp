# 💼 Job Application Serverless Web Application using AWS

## 📌 Overview  
A serverless job application portal built with:

- **Frontend**: HTML, CSS, JavaScript (static hosting on S3)  
- **Backend**: AWS Lambda (Python), API Gateway, DynamoDB, S3  

## ✨ Features

- Applicants can submit their details and upload resumes.  
- Recruiters can view all applications and open resumes directly from the portal.  
- Resume files are stored in **Amazon S3**; application data is stored in **DynamoDB**.  
- Fully serverless architecture ensures scalability and cost-efficiency.  

## 🧩 Architecture Diagram  

![Screenshot 2025-07-07 235827](https://github.com/user-attachments/assets/e6f80c19-5440-4d32-812f-a237809b812a)


## ⚙️ How it Works

### 👤 Applicant Portal:
- Users fill out a form and upload their resume.
- The form sends data to an **API Gateway** endpoint, triggering a **Lambda function**.
- Lambda function:
  - Uploads the resume to **S3**
  - Stores applicant data in **DynamoDB**

## Screenshot:

![Screenshot 2025-07-08 002820](https://github.com/user-attachments/assets/5e6410f3-1dde-4c93-8e62-15d802690731)


### 👥 Recruiter Portal:
- Recruiters access a protected page to view all applications.
- The page sends a GET request to another **Lambda function** via **API Gateway**.
- Application details are retrieved from **DynamoDB**.
- Resume links are fetched from **S3** and can be opened directly.

## Screenshot:

![recruiter-portal](https://github.com/user-attachments/assets/311ad1f0-a2c0-4e13-8561-023f6307b903)


## 🛠 Configuration

- Update the API endpoint URLs in the frontend JavaScript.
- To change the resume S3 bucket, update the `bucketName` variable in the recruiter portal JS.

## 🚀 Deployment

- Deploy Lambda functions via **AWS Console**, **SAM**, or **Serverless Framework**.
- Upload static frontend files to an **S3 bucket** with static website hosting enabled.
- Enable **CORS** on API Gateway for your frontend domain.

---

🔗 *Built using AWS Services for an efficient, scalable, and modern job application experience.*
