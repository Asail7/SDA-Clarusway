# SDA – Clarusway Bootcamp Web Deployment (Week 9)

This project is part of the Infrastructure Bootcamp – Week 9 assignment. The goal was to deploy a simple static website using various AWS services, ensuring high availability and scalability.

---

## 🚀 Project Objective

Deploy a static website (index.html + logos) using:

- **Amazon S3** for static asset hosting
- **EC2 Auto Scaling Group** for NGINX web servers
- **Application Load Balancer (ALB)** for distributing HTTP traffic
- **IAM Role** to grant EC2 access to S3
- **Health checks** to monitor instance availability


---

## 📂 Repository Structure

- `index.html` – Main web page
- `logo.png`, `sda.png` – Images displayed in the website
- `screenshots/` – Contains:
  - `s3-url.png` – S3 website hosting proof
  - `curl-s3.png` – `curl -I` to S3 endpoint
  - `ec2-running.png` – Two running EC2 instances
  - `alb-dns.png` – ALB DNS name
  - `curl-alb.png` – curl output showing traffic rotation

---

## ✅ Success Criteria (Confirmed)

- Website accessible via both:
  - **S3 static endpoint**
  - **ALB DNS name**
- ALB distributes requests across multiple EC2 instances
- EC2 instances replace automatically when terminated
- S3 content (HTML + images) loads correctly
- curl tests show round-robin behavior

---

## 🧪 Sample curl test to ALB

```bash
for i in {1..5}; do curl http://<your-alb-dns>; done


