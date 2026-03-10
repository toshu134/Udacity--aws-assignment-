# AWS Static Website Hosting using S3 and CloudFront

## Project Overview

This project demonstrates how to deploy a **static website on Amazon S3** and distribute it globally using **Amazon CloudFront**.
The website consists of **HTML, CSS, and JavaScript files** and is hosted as a static website without any server-side processing.

The objective of this project is to understand how cloud services can be used to host and deliver web content efficiently and securely.

---

## Architecture

The architecture used in this project includes:

1. **Amazon S3**

   * Stores the static website files.
   * Configured for **Static Website Hosting**.

2. **Bucket Policy**

   * Allows public read access to the website files.

3. **Amazon CloudFront**

   * Content Delivery Network (CDN) used to distribute the website globally.
   * Improves performance and reduces latency.

---

## Technologies Used

* Amazon S3
* Amazon CloudFront
* HTML
* CSS
* JavaScript
* AWS IAM Policies

---

## Project Steps

### 1. Create an S3 Bucket

* Created a new S3 bucket named:

```
arnav-kumar-static-website
```

* Disabled **Block Public Access** settings.
* Enabled **Static Website Hosting**.

---

### 2. Upload Website Files

Uploaded the following files to the bucket:

```
index.html
style.css
script.js
```

These files form the structure, styling, and interactivity of the static website.

---

### 3. Configure Static Website Hosting

Configured the bucket with:

```
Index document: index.html
Error document: index.html
```

This allows the bucket to serve the website directly.

---

### 4. Configure Bucket Policy

Added a bucket policy to allow public access to the website files.

Example policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::arnav-kumar-static-website/*"
    }
  ]
}
```

---

### 5. Access Website via S3 Endpoint

The website is accessible through the S3 website endpoint:

```
http://arnav-kumar-static-website.s3-website-us-east-1.amazonaws.com/
```

---

### 6. CloudFront Distribution

A **CloudFront distribution** was created to improve content delivery speed and reliability.

CloudFront fetches website content from the S3 bucket and delivers it via a global CDN network.

CloudFront URL example:

```
https://dxxxxx.cloudfront.net
```

---

## Screenshots

The repository includes screenshots demonstrating the following steps:

* S3 Bucket Creation
* Files Uploaded to S3
* Static Website Hosting Enabled
* Bucket Policy Configuration
* Website Access via S3 Endpoint
* CloudFront Distribution Configuration
* Website Access via CloudFront

---

## Key Learnings

Through this project, I learned:

* How **static websites can be hosted on AWS S3**
* How **IAM bucket policies control public access**
* How **CloudFront CDN improves website performance**
* Basic **cloud architecture for scalable web hosting**

---

## Author

**Arnav Kumar Singh**

B.Tech Computer Science Engineering
Amity University

---

## License

This project is for **educational and learning purposes**.
