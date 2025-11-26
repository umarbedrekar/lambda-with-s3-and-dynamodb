# AWS Lambda with S3 and DynamoDB (Serverless Media Upload Hub)

This project outlines a **serverless media upload hub** built using **AWS Lambda**, **Amazon S3**, and **Amazon DynamoDB**. It enables users to upload media files through a web interface, storing the files in S3 and their associated metadata in DynamoDB.

---

## ⭐ Features

* **Serverless Backend:** Uses AWS Lambda for scalable request handling without managing servers.
* **Object Storage:** Media files are stored in an S3 bucket.
* **Data Management:** Metadata (name, caption, file URL, ID) is stored in DynamoDB.
* **User-Friendly Interface:** Simple web form for uploading media.

---

## 🏗️ Project Architecture Diagram

"C:\aws lamda screenshot\Untitled Diagram.drawio (1).svg"


---

## 📸 Project Walkthrough & Components

Below are the main components of the project, each supported by screenshots.

### 1. Upload Interface

A web form where users enter **name**, **caption**, and upload a media file.

![screenshot (217)](https://github.com/user-attachments/assets/17140a8c-7981-414c-a963-4a6989f85b5d)


### 2. IAM Role Permissions

Shows permissions attached to the Lambda execution role.

<img width="1920" height="924" alt="Screenshot (219)" src="https://github.com/user-attachments/assets/32fd6d62-84e0-430e-84d4-09fa3e87a89d" />


### 3. Lambda Function Code

Python Lambda handler that uploads the file to S3 and stores metadata in DynamoDB.

<img width="1920" height="929" alt="Screenshot (220)" src="https://github.com/user-attachments/assets/534db3d5-e5bf-4fbb-ac09-2fefee31f347" />


### 4. Lambda Layer Configuration

Configuration details of the custom Lambda layer for dependencies.

<img width="1920" height="927" alt="Screenshot (222)" src="https://github.com/user-attachments/assets/e7eeca94-2148-4da5-be87-3ff4a9cae014" />


### 5. S3 Bucket Overview

The bucket where media files are stored.

* *Bucket Name:* `lamdawithdynadb`
<img width="1920" height="923" alt="Screenshot (223)" src="https://github.com/user-attachments/assets/c49833ba-3a88-47f5-8492-fc45494ef1bc" />


### 6. DynamoDB Table Entries

Shows uploaded metadata rows in the DynamoDB table.

* *Table Name:* `reels`
<img width="1920" height="912" alt="Screenshot (224)" src="https://github.com/user-attachments/assets/8407251e-9ccd-456e-90ec-4025ac8a930c" />


### 7. Successful Upload Confirmation

Confirmation message shown after upload, including media details and file URL.

![Screenshot (225)](https://github.com/user-attachments/assets/01b143f4-cee7-4646-b12a-29f42a54ac33)


---

## 🚀 High-Level Deployment Steps

1. Create an **S3 bucket** to store uploaded media files.
2. Create a **DynamoDB table** (e.g., `reels`) to store metadata.
3. Create an **IAM role** for Lambda with S3 + DynamoDB permissions.
4. Deploy the **AWS Lambda function**.
5. (Optional) Create a **Lambda Layer** for external dependencies.
6. Configure **API Gateway** → Lambda integration.
7. Build a basic **frontend upload form**.

---

