
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

Check this JSON code file in Backet-policy-file.


Replace my-website-bucket with the name of your bucket.

Save the policy.

Step 3: Upload Your Static Website to S3
Go to the "Objects" tab of your bucket.
Click on "Upload".
Add files:
Click "Add files" and select your static website files (e.g., index.html, error.html, CSS, JS, etc.).
Click "Upload".

http://YOUR_BUCKET_NAME.s3-website-REGION.amazonaws.com
Example: How to Check and Configure Settings
Enable Static Website Hosting:

Go to your S3 bucket in the AWS console.
Navigate to "Properties".
Click "Edit" under "Static website hosting".
Enable it and set index.html as the index document.
Set Bucket Policy:

Go to the "Permissions" tab.
Click "Bucket Policy" and paste the policy provided above, replacing YOUR_BUCKET_NAME with your bucket name.
Save the changes.
Check File Permissions:

Navigate to the "Objects" tab.
Select index.html and ensure it is publicly accessible.
If you still face issues, double-check the file paths and names, as any discrepancies can lead to a 404 error.

