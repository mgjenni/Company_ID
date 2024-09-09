# Static Webpage on AWS S3

This project involves creating a static webpage hosted on AWS S3. The webpage displays companies in six different sectors and provides an interactive experience when a company is clicked. Below are the steps to set up the project:

## Steps to Create the Static Webpage

### Step 1: Create S3 Bucket

- Log in to the AWS Management Console.
- Navigate to the S3 service.
- Click on "Create bucket."
- Choose a unique bucket name and select the appropriate region.
- Leave the default settings as they are or adjust as needed.
- Click "Create bucket."

<img src="https://i.imgur.com/YS3qwa5.png" height="80%" width="80%" alt="Create Bucket"/>

### Step 2: Upload All Files

- Once the bucket is created, click on the bucket name to enter it.
- Select "Upload" and choose all the files (HTML, CSS, images, etc.) from your local system.
- Click "Upload" to transfer the files to your S3 bucket.

- <img src="https://i.imgur.com/VUN70jp.png" height="80%" width="80%" alt="Upload Files"/>

### Step 3: Ensure Public Accessibility of the Site

#### 3.1 Enable Static Website Hosting

- In the S3 bucket, go to the "Properties" tab.
- Scroll down to "Static website hosting."
- Select "Enable" and choose the "Index document" (e.g., `index.html`).
- Save the changes.

<img src="https://i.imgur.com/YfGNn5b.png" height="80%" width="80%" alt="Enable Static Website Hosting"/>

#### 3.2 Disable Block All Public Access

- Go to the "Permissions" tab of your S3 bucket.
- Scroll down to "Block public access (bucket settings)."
- Click "Edit" and uncheck the "Block all public access" option.
- Save the changes.

<img src="https://i.imgur.com/BoHIXx0.png" height="80%" width="80%" alt="Disable Block All Public Access"/>

#### 3.3 Make Every Object Public Using ACL

- Still in the "Permissions" tab, scroll down to "Bucket Policy" and click "Edit."
- Scroll down to the "Access control list (ACL)" section.
- In the "Objects" section, select "Everyone (public access)" and allow reading access.
- Save the changes.

<img src="https://i.imgur.com/DYJtgju.png" height="80%" width="80%" alt="Disable Block All Public Access"/>

## Conclusion

After completing these steps, your static webpage should be publicly accessible via the S3 URL. Users can interact with the webpage and view company profiles, including photos of the CEO and company logos.
