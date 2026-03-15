<strong>Hosting portfolio </strong>

Instead of hosting a website on a traditional server, I explored how Amazon S3 can be used for scalable and cost-effective static website hosting, and how Amazon CloudFront can improve performance and security by providing a global Content Delivery Network (CDN) with HTTPS support.

⚙️ Deployment Steps
1️⃣ Create an S3 Bucket

Go to AWS Console → S3

Click Create bucket

Give the bucket a unique name

Example:

mayank-portfolio-site

Disable Block Public Access

2️⃣ Upload Website Files

Upload all static files:

index.html
style.css
images

to the S3 bucket.

3️⃣ Enable Static Website Hosting

Go to:

Bucket → Properties → Static Website Hosting

Enable it and set:

Index document: index.html
4️⃣ Configure Bucket Policy

To allow public access to the website files, add the following policy:

{
 "Version": "2012-10-17",
 "Statement": [
  {
   "Effect": "Allow",
   "Principal": "*",
   "Action": "s3:GetObject",
   "Resource": "arn:aws:s3:::mayank-portfolio-site/*"
  }
 ]
}
5️⃣ Create CloudFront Distribution

Go to:

AWS Console → CloudFront

Steps:

Click Create Distribution

Select your S3 bucket as origin

Enable HTTPS

Set Default root object

index.html

CloudFront provides a domain like:

https://d28o0kd50nnu1n.cloudfront.net

🔒 HTTPS Access:

CloudFront automatically provides SSL encryption, allowing the website to be accessed securely via:

https://d28o0kd50nnu1n.cloudfront.net

📌 Live Website
https://d28o0kd50nnu1n.cloudfront.net

<img width="1920" height="1200" alt="Image" src="https://github.com/user-attachments/assets/232c0601-ce20-4614-8c37-f435d0d67c6e" />

<img width="1920" height="1200" alt="Image" src="https://github.com/user-attachments/assets/af37cb90-3596-45d6-baf0-bb1a9ebd2181" />

<img width="1920" height="1200" alt="Image" src="https://github.com/user-attachments/assets/46d41af3-adfb-45ce-8839-8b5626b6d19e" />

<img width="1920" height="1200" alt="Image" src="https://github.com/user-attachments/assets/f79d7b49-85b9-4944-8c2f-9322a6b5428c" />

<img width="1920" height="1200" alt="Image" src="https://github.com/user-attachments/assets/3b8b8acf-88cd-40a7-9fc5-2180bf74039d" />
