
Here's a step-by-step guide for setting up an S3 bucket to host a static website and uploading your project to GitHub. This document will include creating an S3 bucket, configuring it for static website hosting, setting up a bucket policy, and pushing your static website code to GitHub.

Step 1: Create and Configure an S3 Bucket
Log in to the AWS Management Console.

Navigate to the S3 service.

Create a new bucket:

Click on "Create bucket".
Enter a unique bucket name (e.g., my-website-bucket).
Choose a region.
Click "Create bucket".
Configure the bucket for static website hosting:

Go to the "Properties" tab of your bucket.
Scroll down to "Static website hosting".
Enable "Use this bucket to host a website".
Specify the "Index document" (e.g., index.html).
Specify the "Error document" (e.g., error.html).
Click "Save".
Step 2: Set Bucket Policy for Public Access
Go to the "Permissions" tab of your bucket.

Click on "Bucket Policy".

Add the following bucket policy to allow public read access:

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-website-bucket/*"
        }
    ]
}
