# Secure-EC2-S3-Integration-using-IAM-Role


Step 1 :
I **CREATED** an Amazon S3 bucket which will be used as cloud storage for this project.
I kept block public access enabled because in real companies storage should be private by default for security reasons.
![Project Screenshot](step-1-s3-bucket-created.png)

Step 2 :
I **UPLOADED** a sample file inside the S3 bucket.
This file will be used later to test whether EC2 instance can download files from S3 storage.
![Project Screenshot](step-2-s3-object-uploaded.png)

Step 3 :
I **Launched an EC2 instance** which will act like an application server in this project.
This server will later connect with S3 storage securely.
