#  🌐 AWS S3 Static Website Hosting

![AWS](https://img.shields.io/badge/Built%20with-AWS-orange?style=flat&logo=amazonaws)
![Project Status](https://img.shields.io/badge/status-finished-green)


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

## Step 1: Create an S3 Bucket ( In the AWS Console)

- In the AWS console, go to the S3 Dashboard

- Click Create bucket

### 🪣 Bucket Settings  

| Setting                | Value / Instructions                                                                 |
|------------------------|---------------------------------------------------------------------------------------|
| **Bucket name**        | `your-static-website-name` (must be globally unique)                                 |
| **AWS Region**         | Choose your preferred region                                                         |
| **Block Public Access**| **Uncheck** “Block all public access” ⚠️                                             |
|                        |  Acknowledge the warning that your bucket will be public                           |
| **Bucket versioning**  | Leave as default (Disabled)                                                          |
| **Tags**               | Optional                                                                             |
| **Encryption**         | Leave as default (Disabled or S3-managed key)                                        |
| **Advanced settings**  | Leave as default                                                                     |


 ## Step 2: Upload Your Website Files 
- Click Create bucket at the bottom.
  Open the S3 bucket you created.

- Click “Upload”.

- Click “Add files” and select:

    - `index.html`

    - `styles.css`
    - (Optional) `script.js`
    - Click Upload.
- Click Next through the options (you don’t need to change permissions here, we’ll set public access via a bucket policy next).
  
 ## 🌐 Step 3: Enable Static Website Hosting
 #### In the AWS Console:

-  Go to your S3 bucket.

- Click the “Properties” tab.

- Scroll down to “Static website hosting”.

- Click “Edit.

| Setting                        | Value                         |
|-------------------------------|-------------------------------|
| **Enable**                    | Enable                      |
| **Hosting type**              | “Host a static website”       |
| **Index document**            | `index.html`                  |
| **Error document** (optional) | `index.html` or `error.html`  |
- Click “Save changes”.

##  Step 4: Add a Bucket Policy to Allow Public Access
#### In the AWS Console:
- Go to your S3 bucket.

- Click the “Permissions” tab.

- Scroll to Bucket policy and click “Edit”.

 #### 📜 Paste this Bucket Policy:
 
     {
     "Version": "2012-10-17",
     "Statement": [
    {
      "Sid": "PublicReadForStaticWebsite",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
    ]
    }

   ![image alt](https://github.com/Juniorklb/Static-website-S3-/blob/ea4bba780a589528d70209127eb0cb6b1767d8cc/images/buckets.PNG)
- 🔁Important: Replace ``your-bucket-name`` with your actual bucket name.

- Click “Save changes”.

-  Now, your static site should be publicly viewable via the website endpoint URL from Step 3.
  
  ![image alt](https://github.com/Juniorklb/Static-website-S3-/blob/ad3497387d37fda38ac88478513ac8654ea7dd47/images/s3static%20website.PNG)

## Conclusion: AWS Static Website Hosting with S3
You've successfully created and deployed a static website on AWS using S3 — congratulations! 🎉 Here's what you accomplished: 
#### 🔧 Steps You Completed

- Created an S3 Bucket with public access

- Uploaded your website files (index.html, styles.css, etc.)

- Enabled static website hosting in the bucket properties

- Configured a bucket policy to allow public access to your content

#### 🌐 Your Website is Live!
- You can now share the S3 Website Endpoint URL with anyone, and your site will be accessible globally.


## 📚 Author
![AWS](https://img.shields.io/badge/Built%20with-AWS-orange?style=flat&logo=amazonaws) by Junior Kalomba
**🔗 Feel free to contribute or suggest improvements!** 
<p align="right">
  <a href="https://www.linkedin.com/in/junior-kalomba-10002a18a/" target="_blank">
    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="junior-kalomba-10002a18a" height="30" width="40"/>  
   
