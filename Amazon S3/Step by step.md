## Step-by-Step Implementation

### Step 1: Create an Amazon S3 Bucket
- Open the AWS Management Console and navigate to **Amazon S3**
- Create a new bucket with a **globally unique name**
- Select the desired AWS region
- Keep default settings and create the bucket

---

### Step 2: Upload an Object (Image)
- Open the created S3 bucket
- Upload an image file to the bucket
- Attempt to access the object using the public URL
- Access is denied by default, confirming that the bucket is **private**

---

### Step 3: Disable Block Public Access
- Navigate to the **Permissions** tab of the bucket
- Edit **Block public access (bucket settings)**
- Disable all block public access options
- Save the changes and acknowledge the warning

**Reason:**  
S3 blocks public access by default to prevent accidental data exposure. Disabling this allows public permissions to be applied.

---

### Step 4: Generate a Bucket Policy
- Open **AWS Policy Generator**
- Select policy type: **S3 Bucket Policy**
- Set Effect to **Allow**
- Set Principal to `*` (public access)
- Set Actions to `s3:GetObject`
- Specify the bucket resource ARN:
  -  arn:aws:s3:::<bucket-name>/*




- Generate the policy

---

### Step 5: Apply the Bucket Policy
- Return to the S3 bucket **Permissions** tab
- Open **Bucket policy**
- Paste the generated policy JSON
- Save the policy

**Reason:**  
The bucket policy explicitly allows public read access to objects within the bucket.

---

### Step 6: Access Object via Public URL
- Copy the object’s public URL
- Open the URL in a browser

- Verify the image loads successfully

---

### Step 7: Validation
- Confirm that objects are accessible publicly
- Ensure only read (`GetObject`) permission is granted
- No write or delete permissions are exposed

---

### Security Note
- Public access was enabled **only for demonstration purposes**
- In production environments, public access should be tightly controlled
- Bucket policies are preferred over object-level ACLs

