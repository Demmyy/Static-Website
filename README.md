# Hosting a Static Website with S3

This Project demonstrates how to host a static website using Amazon S3. By the end of this setup, a static website is publicly accessible through an S3 endpoint.

## Step-By-Step Setup

1. The first thing i did was to create an S3 Bucket. Here are the steps are took to create the bucket: 

- Logged into the AWS Management Console
- Searched for S3
- Clicked on Create Bucket
- Selected the bucket type
- Entered a unique bucket name
- Selected a region
- Disabled **Block all public access** (This enabled public access to the website over the internet.)
![Bucket](images/img1.png)
![Public Access](images/img4.png)

2. Uploading Website Files

I downloaded an HTML template and unzipped it. I then uploaded the unzipped folder to my Bucket.
![Website Upload](images/img2.png)

3. Enabling Static Website Hosting

After uploading my object in the bucket, it is now time to enable static website hosting.

 I scrolled down to **Static Website Hosting** in the **Properties** Section, I enabled it and 
  - Set: 
    - Index document: ````index.html```` (My HTML Document)
    - Error document: ````error.html```` (optional)

 ![Upload Static Website](images/img3.png)

4. Next, I added my Bucket Policy in the permissions section (To make files Public)  **[View Policy](Policy.txt)**.

![Bucket Policy](images/img5.png)

5. Now my website is set for viewing;

I copied the Endpoint URL ```` http://demo-demo-bucket.s3-website-us-east-1.amazonaws.com```` for my website and opened it in my browser.

![Website](images/img6.png)
