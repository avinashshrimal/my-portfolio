# Avinash — Portfolio Website
A responsive single-page portfolio hosted on AWS S3 and served via CloudFront (HTTPS).

## 🔗 Live URL
https://YOUR-CLOUDFRONT-DOMAIN.cloudfront.net

## 🛠️ Tech Stack
- HTML5 / CSS3
- AWS S3 (Static Website Hosting)
- AWS CloudFront (CDN + HTTPS)
- Git + GitHub (Version Control)

## 📁 Project Structure
my-portfolio/
├── index.html
├── styles.css
└── README.md

## 🚀 Steps Taken

### 1. Built the website locally
- Created index.html and styles.css
- Tested in browser locally

### 2. Pushed to GitHub
git init
git add .
git commit -m "Initial portfolio commit"
git push -u origin main

### 3. Created S3 Bucket
- Bucket name: avinash-portfolio-2025
- Region: ap-south-1 (Mumbai)
- Enabled Static Website Hosting
- Disabled Block Public Access
- Added bucket policy to allow s3:GetObject

### 4. Uploaded Files to S3
aws s3 sync . s3://avinash-portfolio-2025 --acl public-read

### 5. Created CloudFront Distribution
- Origin: avinash-portfolio-2025.s3-website.ap-south-1.amazonaws.com
- Viewer Protocol: Redirect HTTP to HTTPS
- WAF: Disabled (Free Tier)
- Default root object: index.html

### 6. Verified HTTPS
- Opened CloudFront URL in browser
- Confirmed HTTPS padlock visible

## 📸 Screenshots
- CloudFront distribution dashboard
- S3 bucket policy
- Live site on HTTPS

## ⚙️ AWS Free Tier Usage
| Service | Usage |
|---|---|
| S3 | Static file hosting |
| CloudFront | CDN + HTTPS |
| Cost | $0 (Free Tier) |