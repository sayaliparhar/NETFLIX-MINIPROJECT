# Netflix Static Website on AWS S3

This project is a **secure and scalable static Netflix-style website** for hosting trailers, deployed using **AWS S3**.  
It demonstrates the use of S3 features like **static website hosting, versioning, replication, and transfer acceleration** to deliver content globally with high availability and performance.

---

## 🌐 Project Overview
The goal of this project was to create a **resilient and fast static website** using AWS S3.  
Key objectives:  
- Host trailers as static content.  
- Make content publicly accessible worldwide.  
- Implement features like versioning, cross-region replication, and transfer acceleration.  
- Ensure disaster recovery and fast uploads from global contributors.  

---

## 🚀 Architecture

- **S3 Buckets** → Store static content (HTML, CSS, JS, images).  
- **Static Website Hosting** → Serve content through a public endpoint.  
- **Versioning** → Maintain multiple versions of objects for recovery.  
- **Replication** → Cross-region backup for disaster recovery.  
- **Transfer Acceleration** → Fast uploads and downloads from global locations.  

### Project Directory Structure
```text
NETFLIX-PROJECT/
│-- index.html         # Home Page
│-- trailers.html      # Trailers Page
│-- contact.html       # Contact Page
│-- error.html         # Custom 404 Error Page
│
│-- css/
│   └-- style.css      # Main Stylesheet
│
└-- Images/
    ├-- Tv shows/     # Images for TV shows
    ├-- Series/       # Images for series
```


## ⚙️ Implementation Steps
### Step 1: Create S3 Bucket

Created an S3 bucket with a unique name.

Enabled Static Website Hosting.

Configured index.html as the default document and added a custom error page.

### Step 2: Upload Website Files

Uploaded HTML, CSS, JS, and image files to the bucket.

Verified all files are in the root directory for proper hosting.

### Step 3: Configure Permissions

Enabled public read access for the bucket (or added a bucket policy).

Confirmed the website is accessible via the S3 static website URL.

<p align="center"> <img width="700" alt="static website hosting" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/static%20website%20hosting.PNG?raw=true" /> </p>

### Step 4: Enable Advanced S3 Features
Versioning → Enabled to track object changes and recover deleted or overwritten files.
<p align="center"> <img width="700" alt="Versioning" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/versioning.PNG?raw=true" /> </p>

<br><br>

Replication → Configured cross-region replication for disaster recovery.

<p align="center"> <img width="700" alt="Replication" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/replication.PNG?raw=true" /> </p>

<br><br>

Transfer Acceleration → Enabled for fast uploads and downloads globally.
<p align="center"> <img width="700" alt="Transfer Acceleration" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/Transfer%20Accelaration.PNG?raw=true" /> </p>

<br><br>

Cross-Region Replication (CRR) → Ensures data is automatically copied to another AWS region for disaster recovery and global availability.

<p align="center"> <img width="700" alt="Cross-region-replication" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/cross%20region%20replication.PNG?raw=true" /> </p>




### Step 5: Test Website

Verified Home Page, Trailer Page, Contact Page, and Error Page.

Confirmed all images and trailers load correctly.

Checked S3 endpoint and accelerated transfers.

<p align="center"> <img width="700" alt="Home Page" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/index%20page%20(1).png?raw=true" /> </p>

<br><br>

<p align="center"> <img width="700" alt="Trailers Page" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/Trailer%20Page.png?raw=true" /> </p>

<br><br>

<p align="center"> <img width="700" alt="Error Page" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/Error%20page.png?raw=true" /> </p>

<br><br>

<p align="center"> <img width="700" alt="Contact Page" src="https://github.com/sayaliparhar/NETFLIX-MINIPROJECT/blob/main/TestCases/Contact%20page.png?raw=true" /> </p>

## 🔧 Challenges & Lessons Learned

**Learned to configure S3 static website hosting and custom error pages.**

**Enabled versioning and tested object recovery.**

**Set up cross-region replication for disaster recovery.**

**Configured Transfer Acceleration for improved performance.**

## 💰 Cost Optimization

**Only AWS S3 was used → minimal cost, fully compatible with AWS Free Tier.**

**No EC2 or other paid services were used.**

## 🔗 Demo

**🌐 Website Access:** http://miniprojectfors3.s3-website.ap-south-1.amazonaws.com

 **Note:** The S3 bucket used for this static website has been deleted after the demo.  

**📂 Project Code: All HTML, CSS, JS, and image files are included in this repository.**


## 🚀 Future Enhancements

**Integrate CloudFront for faster content delivery and HTTPS.**

**Add a custom domain via Route 53.**

**Improve responsive design for mobile and tablet users.**

**Implement CI/CD pipeline for automated updates to S3.**