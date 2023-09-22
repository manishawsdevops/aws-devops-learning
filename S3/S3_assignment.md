# Building a Static Website Hosting Solution with AWS S3, Versioning, and Lifecycle Policies


## Steps

1. Navigating to S3 Console and Creating a S3 Bucket with unique name

![S3 Bucket](s3Bucket.png)

2. Give the Public Access the objects by clicking bucket name and navigating to permissions tab

![Public Access the objects](bucketPermission.png)
![Bucket](bucket.png)

3. Navigate to Objects Tab and upload the HTML and CSS files.

![Objects](objects.png)

4. Enable the Bucket Version by navigating to properties tab

![Enabling the Bucket Version](bucketVersion.png)
![Objects with Version ID](objectPage.png)

5. Enable the Static Website Hosting by navigating to Properties Tab

![Enable the Static Website Hosting](enableStatic.png)

6. Implement an S3 bucket policy to restrict access to the website only from specific IP addresses.

![Bucket Policy](bucketPolicy.png)

7. We can give LifeCycle Rules to transition to another storage class and delete the objects after the period.
   Where LifeCyle1 is transition to S3 Glacier Deep Archive after 30 days and
   LifeCycle2 is to delete the objects after 90 days

![Lifecycle Rules](lifecycles.png)

8. Checking the Static Website either by navigating to properties tab or by clicking on first object url.

![Website Method 1](enableStatic.png)
![Website Method 2](objectUrL.png)
![Website](website.png)

9. Checking the website by modyfying the main.html and uploading the new html file

![new file](newfile.png)

10. Check the website again.

![Website](website1.png)

11. I have created with IAM user with S3 readonlyaccess.

![IAM user](IAMuser.png)

12. Enabled Server Access Logging

![Server Access Logging](serveraccess.png)
