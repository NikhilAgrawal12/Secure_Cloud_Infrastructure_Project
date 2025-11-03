# Secure Cloud Infrastructure Project – AWS, Docker, and EC2

This project demonstrates the design and deployment of a secure, cloud-based architecture for managing and storing user-uploaded images using **AWS services**. The solution highlights **secure cloud design**, **automation**, and **role-based access control**, aligning with modern **cloud engineering and cybersecurity** best practices.

---

## 🏗️ Architecture Overview

The application is deployed using **Amazon EC2** and integrates with **AWS S3** and **RDS** for scalable data and storage management. Security and automation are implemented through **IAM roles**, **Docker**, and **SDK-based uploads**.


![image alt](https://github.com/NikhilAgrawal12/AwsJavaProject/blob/c0e5b5e948d13a3013222f9847442ada7f69e203/Image1.png)

### Key Flow

1. **EC2 Role Authorization** – Grants the EC2 instance permission to upload files securely to S3 using an attached IAM role (`aws-elasticbeanstalk-ec2-role`).
2. **Image Upload via S3Client** – Application uploads images to the S3 bucket path `/images/user-id/image-id` using AWS SDK (S3Client).
3. **Metadata Storage in RDS** – Image identifiers and metadata are securely stored in an Amazon RDS database, associated with the respective user.
4. **Local Testing** – Conducted through IntelliJ with a local S3 SDK mock for isolated testing and validation.
5. **Dockerized Deployment** – Application containerized and deployed via Docker for portability and consistent runtime environments.

---

## ☁️ Technologies Used

* **Amazon Web Services (AWS)** – EC2, S3, RDS, IAM
* **Docker** – Containerization for deployment
* **Java / Spring Boot** – Backend API implementation
* **AWS SDK (S3Client)** – For secure uploads and data exchange
* **PostgreSQL** – Managed via Amazon RDS
* **IntelliJ IDEA** – Development and testing environment

---
![image alt](https://github.com/NikhilAgrawal12/AwsJavaProject/blob/f4589b3debe72f4908df1a90de67e980ba83ca7e/Image2.png)

![image alt](https://github.com/NikhilAgrawal12/AwsJavaProject/blob/a564dfc0f930bc03ab028af45b5be9b493c3f885/Image3.png)

## 🔐 Security Highlights

* **IAM Role-Based Access Control (RBAC):** EC2 instances use IAM roles to interact securely with S3 without embedding credentials.
* **Network Isolation:** Only authorized network paths between EC2, S3, and RDS.
* **Data Protection:** Image data stored in S3 with private access policies; metadata encrypted at rest in RDS.
* **Local Testing with Mock Services:** Reduces cloud exposure and simulates secure upload workflows locally.
* **Docker Isolation:** Each application instance runs in a secure, isolated container.

---



## 📎 Author

**Nikhil Agrawal**

Software & Cloud Engineer | Cybersecurity Enthusiast




