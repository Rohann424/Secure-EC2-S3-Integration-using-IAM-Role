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

![Project Screenshot](step-3-ec2-instance-running.png)



Step 4 :
I **connected** to the **EC2 instance using SSH** from my local machine.
This allows me to configure the server and run commands inside it.

![Project Screenshot](step-4-ssh-connection-success.png)



Step 5 :
I installed **AWS CLI** inside the EC2 instance.
This tool is required so that the server can run commands to interact with AWS services like S3.

![Project Screenshot](step-5-aws-cli-installed.png)



Step 6 :
I tried to list S3 buckets from EC2 but it **Failed** with Access Denied error.
This shows that by default EC2 has no permission to access storage which is good security behaviour.

![Project Screenshot](step-6-s3-access-denied.png)



Step 7 :
I created an **IAM role** which will give **S3 access** permission to the **EC2 instance**.
Using role is safer than using access keys because credentials are managed automatically by AWS.


![Project Screenshot](step-7-iam-role-created.png)


Step 8 :
I **Attached** the IAM role to my EC2 instance so that it can securely communicate with S3 service.

![Project Screenshot](step-8-iam-role-attached-ec2.png)


Step 9 :
After attaching the role I **Tested S3 access again** and now the EC2 instance was able to list buckets successfully.

![Project Screenshot](step-9-s3-access-success.png)


Step 10 :
I **Downloaded** the test file from S3 bucket to the EC2 instance.
This confirms that the server **can read** data from storage.
Reason why we use --recursive :- You will see all objects list

![Project Screenshot](step-10-file-downloaded-from-s3.png)


Step 11 :
I created a **New file** inside EC2 and **Uploaded** it to the S3 bucket.
This confirms that the server can write data to storage.


![Project Screenshot](step-11-file-uploaded-to-s3.png)

Image show the output that the file is sucessfully uploaded in the S3


![Project Screenshot](Step-11-Result-output-of-uploaded-file-s3 (1).png)









