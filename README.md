# ☁️ AWS S3 Static Website Hosting

<p align="center">
  <img src="https://img.shields.io/badge/AWS-Amazon%20S3-FF9900?style=for-the-badge&logo=amazons3&logoColor=white" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Deployment-Success-2EA44F?style=for-the-badge" />
</p>

<p align="center">
  <b>A cloud-based static website deployment project using Amazon S3.</b>
  <br />
  <i>Building, deploying, and hosting web applications using AWS cloud infrastructure.</i>
</p>

---

## 📌 Project Overview

This project demonstrates the deployment of a responsive static website using **Amazon Simple Storage Service (Amazon S3)**.

The website is developed using HTML, CSS, and JavaScript, and hosted directly through Amazon S3 Static Website Hosting.

The implementation demonstrates fundamental cloud engineering concepts, including object storage, static website deployment, bucket policies, and public access management.

## 🎯 Project Objectives

- Understand Amazon S3 and object storage.
- Deploy a static website without managing traditional web servers.
- Configure S3 Static Website Hosting.
- Implement bucket policies for controlled public read access.
- Understand AWS security and access management.
- Verify website availability through an S3 website endpoint.

## 🏗️ Architecture

<p align="center">
  <img src="https://raw.githubusercontent.com/aws-samples/aws-icons-for-plantuml/main/dist/Resource/Storage/AmazonS3.png" width="100" alt="Amazon S3" />
</p>

```text
           USER / WEB BROWSER
                   |
                   | HTTP Request
                   v
        AMAZON S3 WEBSITE ENDPOINT
                   |
                   v
             S3 BUCKET
                   |
          +--------+--------+
          |        |        |
          v        v        v
       index.html style.css script.js
          |        |        |
          +--------+--------+
                   |
                   v
          RENDERED WEBSITE
```

**Architecture explanation:**

1. A user accesses the website through the S3 static website endpoint.
2. Amazon S3 receives the HTTP request.
3. S3 serves the configured `index.html` file.
4. The browser loads the CSS and JavaScript assets.
5. The website is rendered for the user.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Amazon S3 | Object storage and website hosting |
| AWS IAM / Bucket Policy | Access control |
| HTML5 | Website structure |
| CSS3 | Styling and responsive layout |
| JavaScript | Client-side functionality |
| Git & GitHub | Version control and project hosting |

## ⚙️ Implementation Workflow

### Step 1 – Create an S3 Bucket

- Created a general-purpose S3 bucket.
- Selected the Asia Pacific (Mumbai) region.
- Configured default encryption using SSE-S3.
- Kept ACLs disabled.

### Step 2 – Develop Website Files

Created the following files:

- `index.html`
- `style.css`
- `script.js`

Tested the website locally before deploying it to AWS.

### Step 3 – Upload Website Files

Uploaded all three website files directly into the root of the S3 bucket.

### Step 4 – Enable Static Website Hosting

Configured the bucket under:

`S3 → Bucket → Properties → Static Website Hosting`

Set the index document to:

`index.html`

### Step 5 – Configure Public Access

Configured public access for the dedicated demonstration bucket and added a bucket policy granting public read-only access to website objects.

### Step 6 – Deploy and Verify

Accessed the generated S3 website endpoint and verified that the website loaded successfully.

## 📂 Project Structure

```text
aws-s3-static-hosting/
│
├── index.html
├── style.css
├── script.js
├── README.md
│
└── screenshots/
    ├── 01-s3-bucket.png
    ├── 02-uploaded-files.png
    ├── 03-static-hosting-config.png
    ├── 04-bucket-policy.png
    └── 05-live-website.png
```

## 📸 Project Screenshots

Add your actual AWS implementation screenshots in this section.

| Implementation | Screenshot |
|---|---|
| S3 Bucket Creation | `screenshots/01-s3-bucket.png` |
| Website File Upload | `screenshots/02-uploaded-files.png` |
| Static Hosting Configuration | `screenshots/03-static-hosting-config.png` |
| Bucket Policy | `screenshots/04-bucket-policy.png` |
| Live Website | `screenshots/05-live-website.png` |

## 🔐 Security Considerations

- Used bucket policies instead of enabling object ACLs.
- Granted only the `s3:GetObject` permission to public visitors.
- Did not grant public upload or delete permissions.
- Kept sensitive information out of the public bucket.
- Used a dedicated bucket for the static website demonstration.

**Production consideration:** The S3 static website endpoint uses HTTP. For production deployments requiring HTTPS, Amazon CloudFront with appropriate origin access controls is recommended.

## 🚀 Key Learning Outcomes

Through this implementation, I gained practical experience in:

- Amazon S3 bucket creation and configuration.
- Cloud-based static website deployment.
- S3 object storage and website endpoints.
- AWS bucket policies and public access settings.
- Basic cloud security and access management.
- Testing and validating AWS deployments.

## 🔮 Future Enhancements

- Integrate Amazon CloudFront for HTTPS delivery.
- Configure a custom domain using Amazon Route 53.
- Automate deployments through GitHub Actions.
- Implement infrastructure provisioning using AWS CloudFormation.
- Add monitoring and access logging.

## 👨‍💻 Project Information

| Detail | Description |
|---|---|
| Project | AWS S3 Static Website Hosting |
| Category | Cloud Computing / AWS |
| Training | HCLTech Cloud Engineering Training |
| Cloud Provider | Amazon Web Services |
| Status | Successfully Deployed |

---

<p align="center">
  <b>Built with ☁️ AWS and a passion for Cloud Engineering.</b>
  <br />
  <sub>Hands-on learning through practical cloud implementations.</sub>
</p>