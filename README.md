#  🌐 AWS S3 Static Website Hosting

![AWS](https://img.shields.io/badge/Built%20with-AWS-orange?style=flat&logo=amazonaws)
![Project Status](https://img.shields.io/badge/status-in--progress-yellow)


This project demonstrates how to host a static website using **Amazon S3**. It includes steps to upload HTML, CSS, and JavaScript files to an S3 bucket and configure it for public web access.

---

## Features

- 📂 Static website hosted on AWS S3
- 🌍 Publicly accessible via S3 website endpoint
- 🧾 Clean structure with `index.html`, `styles.css`, and optional `script.js`
- ⚙️ Bucket configured for website hosting

---

## 🚀 Deployment Steps

1. **Create an S3 bucket**
   - Unique name, e.g., `my-static-site-2025`
   - Disable “Block all public access”
   - Enable static website hosting

2. **Upload website files**
   - `index.html`, `styles.css`, and other assets

3. **Set permissions**
   - Add a bucket policy to allow public read access

4. **Access your site**
   - Use the S3 website endpoint provided in the bucket settings

---

## 🗂️ Project Structure

     aws-s3-static-website/ │
     ├── index.html # Main landing page 
     ├── styles.css # Stylesheet for the website 
     ├── script.js # (Optional) JavaScript functionality 
     └── README.md # Project documentation


## Step 1: Create an S3 Bucket ( In the AWS Console)

- In the AWS console, go to the S3 Dashboard

- Click Create bucket

### 🪣 Bucket Settings  

| Setting                | Value / Instructions                                                                 |
|------------------------|---------------------------------------------------------------------------------------|
| **Bucket name**        | `your-static-website-name` (must be globally unique)                                 |
| **AWS Region**         | Choose your preferred region                                                         |
| **Block Public Access**| **Uncheck** “Block all public access” ⚠️                                             |
|                        | ✅ Acknowledge the warning that your bucket will be public                           |
| **Bucket versioning**  | Leave as default (Disabled)                                                          |
| **Tags**               | Optional                                                                             |
| **Encryption**         | Leave as default (Disabled or S3-managed key)                                        |
| **Advanced settings**  | Leave as default                                                                     |


## 📚 Author
Built with ☁️ by [Junior Kalomba]
